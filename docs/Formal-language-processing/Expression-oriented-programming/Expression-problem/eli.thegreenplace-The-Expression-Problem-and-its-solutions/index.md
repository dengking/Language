# eli.thegreenplace [The Expression Problem and its solutions](https://eli.thegreenplace.net/2016/the-expression-problem-and-its-solutions/)

The craft(技巧) of programming is almost universally concerned with different types of data and operations/algorithms that act on this data [[1\]](https://eli.thegreenplace.net/2016/the-expression-problem-and-its-solutions/#id7). Therefore, it's hardly surprising that designing **abstractions** for data types and operations has been on the mind of software engineers and programming-language designers since... forever.

## Problem statement

> NOTE: 问题描述: 
>
> 1 添加new type
>
> 2 添加new operation
>
> 3 without changing existing code

Here is a quick **problem statement**.

Imagine that we have a set of **data types** and a set of **operations** that act on these types. Sometimes we need to add more **operations** and make sure they work properly on all types; sometimes we need to add more **types** and make sure all operations work properly on them. Sometimes, however, we need to add both - and herein lies the problem. Most of the mainstream programming languages don't provide good tools to **add both new types and new operations to an existing system without having to change existing code**. This is called the "**expression problem**". Studying the problem and its possible solutions gives great insight into the fundamental differences between **object-oriented** and **functional programming** and well as concepts like **interfaces** and **multiple dispatch**.

## A motivating example

As is my wont, my example comes from the world of compilers and interpreters. 

Imagine we're designing a simple expression evaluator. Following the standard [interpreter design pattern](http://eli.thegreenplace.net/2016/on-the-composite-and-interpreter-design-patterns), we have a tree structure consisting of expressions, with some operations we can do on such trees. In C++ we'd have an interface every node in the expression tree would have to implement:

### `class Expr`

```C++
#include <string>
class Expr
{
public:
	virtual std::string ToString() const = 0;
	virtual double Eval() const = 0;
};

```

This interface shows that we currently have two operations we can do on expression trees - evaluate them and query for their string representations. A typical leaf node expression:

### `class Constant`

```C++
class Constant: public Expr
{
public:
	Constant(double value) :
					value_(value)
	{
	}

	std::string ToString() const
	{
		std::ostringstream ss;
		ss << value_;
		return ss.str();
	}

	double Eval() const
	{
		return value_;
	}

private:
	double value_;
};

```

And a typical composite expression:

### `class BinaryPlus`

```C++
class BinaryPlus: public Expr
{
public:
	BinaryPlus(const Expr &lhs, const Expr &rhs) :
					lhs_(lhs), rhs_(rhs)
	{
	}

	std::string ToString() const
	{
		return lhs_.ToString() + " + " + rhs_.ToString();
	}

	double Eval() const
	{
		return lhs_.Eval() + rhs_.Eval();
	}

private:
	const Expr &lhs_;
	const Expr &rhs_;
};
```

Until now, it's all fairly basic stuff. How extensible is this design? Let's see... if we want to add new expression types ("variable reference", "function call" etc.), that's pretty easy. We just define additional classes inheriting from `Expr` and implement the `Expr` interface (`ToString` and `Eval`).

### Adding new operations

However, what happens if we want to add new *operations* that can be applied to **expression trees**? Right now we have `Eval` and `ToString`, but we may want additional operations like "type check" or "serialize" or "compile to machine code" or whatever.

It turns out that adding new operations isn't as easy as adding new types. We'd have to change the `Expr` interface, and consequently change every existing expression type to support the new method(s). If we don't control the original code or it's hard to change it for other reasons, we're in trouble.

### Expression problem in OOP 

In other words, we'd have to violate the venerable(珍贵的) *open-closed principle*, one of the [main principles of object-oriented design](https://en.wikipedia.org/wiki/SOLID_(object-oriented_design)), defined as:

> software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification

The problem we're hitting here is called the *expression problem*, and the example above shows how it applies to object-oriented programming.

Interestingly, the expression problem bites(咬伤) **functional programming** languages as well. Let's see how.

## The expression problem in functional programming

**Update 2018-02-05:** [a new post](http://eli.thegreenplace.net/2018/more-thoughts-on-the-expression-problem-in-haskell/) discusses the problem and its solutions in Haskell in more depth.

### OOP VS FP

Object-oriented approaches tend to collect functionality in **objects** (types). Functional languages cut the cake from a different angle, usually preferring types as thin data containers, collecting most functionality in **functions** (operations) that act upon them. Functional languages don't escape the expression problem - it just manifests there in a different way.

> NOTE: 上面这一段描述了OOP 和 FP之间的差异

To demonstrate this, let's see how the expression evaluator / stringifier looks in Haskell. Haskell is a good poster child for functional programming since its pattern matching on types makes such code especially succinct:

```haskell
module Expressions where

data Expr = Constant Double
          | BinaryPlus Expr Expr

stringify :: Expr -> String
stringify (Constant c) = show c
stringify (BinaryPlus lhs rhs) = stringify lhs
                                ++ " + "
                                ++ stringify rhs

evaluate :: Expr -> Double
evaluate (Constant c) = c
evaluate (BinaryPlus lhs rhs) = evaluate lhs + evaluate rhs
```

### Adding new operations

Now let's say we want to add a **new operation** - type checking. We simply have to add a new function `typecheck` and define how it behaves for all known kinds of expressions. No need to modify existing code.

### Add a new type 

On the other hand, if we want to add a **new type** (like "function call"), we get into trouble. We now have to modify all existing functions to handle this new type. So we hit exactly the same problem, albeit(尽管) from a different angle.

## The expression problem matrix

A visual representation of the **expression problem** can be helpful to appreciate how it applies to OOP and FP in different ways, and how a potential solution would look.

The following 2-D table (a "matrix") has types in its rows and operations in its columns. A matrix cell `row, col` is checked when the operation `col` is implemented for type `row`:

![](./expr-problem-matrix.png)

In object-oriented languages, it's easy to add new types but difficult to add new operations:

![](./expr-problem-oop.png)



Whereas in functional languages, it's easy to add new operations but difficult to add new types:

![](./expr-problem-fp.png)

## A historical perspective

The expression problem isn't new, and has likely been with us since the early days; it pops its head as soon as programs reach some not-too-high level of complexity.

It's fairly certain that the name *expression problem* comes from [an email](http://homepages.inf.ed.ac.uk/wadler/papers/expression/expression.txt) sent by [Philip Wadler](https://en.wikipedia.org/wiki/Philip_Wadler) to a mailing list deailing with adding generics to Java (this was back in the 1990s).

In that email, Wadler points to the paper ["Synthesizing Object-Oriented and Functional Design to Promote Re-Use"](https://cs.brown.edu/~sk/Publications/Papers/Published/kff-synth-fp-oo/) by Krishnamurthi, Felleisen and Friedman as an earlier work describing the problem and proposed solutions. This is a great paper and I highly recommend reading it. Krishnamurthi et.al., in their references, point to papers from as early as 1975 describing variations of the problem in Algol.

> NOTE: 这篇论文收录在了 `Expression-oriented-programming\Expression-problem\Synthesizing-Object-Oriented-and-Functional-Design-to-Promote-Re-Use` 章节中。

## Flipping(翻转) the matrix with the visitor pattern

It's possible to kinda(一点儿) solve (read on to understand why I say "kinda") the **expression problem** in **object-oriented languages**; first, we have to look at how we can flip the problem on its side using the **visitor pattern**. The **visitor pattern** is very common for this kind of problems, and for a good reason. It lets us reformulate(再形式化表示) our code in a way that makes it easier to change in some dimensions (though harder in others).

For the C++ sample shown above, rewriting it using the visitor pattern means adding a new "visitor" interface:

```C++
class ExprVisitor
{
public:
	virtual void VisitConstant(const Constant &c) = 0;
	virtual void VisitBinaryPlus(const BinaryPlus &bp) = 0;
};

```

And changing the `Expr` interface to be:

```C++
class Expr
{
public:
	virtual void Accept(ExprVisitor *visitor) const = 0;
};

```

Now expression types defer(推迟) the actual computation to the visitor, as follows:

```C++
class Constant: public Expr
{
public:
	Constant(double value) :
					value_(value)
	{
	}

	void Accept(ExprVisitor *visitor) const
	{
		visitor->VisitConstant(*this);
	}

	double GetValue() const
	{
		return value_;
	}

private:
	double value_;
};

// ... similarly, BinaryPlus would have
//
//    void Accept(ExprVisitor* visitor) const {
//      visitor->VisitBinaryPlus(*this);
//    }
//
// ... etc.

```

### Evaluator visitor

A sample visitor for evaluation would be [[2\]](https://eli.thegreenplace.net/2016/the-expression-problem-and-its-solutions/#id8):

```C++
class Evaluator: public ExprVisitor
{
public:
	double GetValueForExpr(const Expr &e)
	{
		return value_map_[&e];
	}

	void VisitConstant(const Constant &c)
	{
		value_map_[&c] = c.GetValue();
	}

	void VisitBinaryPlus(const BinaryPlus &bp)
	{
		bp.GetLhs().Accept(this);
		bp.GetRhs().Accept(this);
		value_map_[&bp] = value_map_[&(bp.GetLhs())] + value_map_[&(bp.GetRhs())];
	}

private:
	std::map<const Expr*, double> value_map_;
};

```

### Problem

It should be obvious that for a given set of data types, adding new visitors is easy and doesn't require modifying any other code. On the other hand, adding new types is problematic since it means we have to update the `ExprVisitor` interface with a new abstract method, and consequently update all the visitors to implement it.

So it seems that we've just turned the expression problem on its side: we're using an OOP language, but now it's hard to add types and easy to add ops, just like in the functional approach. I find it extremely interesting that we can do this. In my eyes this highlights the power of different abstractions and paradigms, and how they enable us to rethink a problem in a completely different light.

So we haven't solved anything yet; we've just changed the nature of the problem we're facing. Worry not - this is just a stepping stone to an actual solution.

## Extending the visitor pattern

The following is code excerpts from a C++ solution that follows the **extended visitor pattern** proposed by Krishnamurthi et. al. in their paper; I strongly suggest reading the paper (particularly section 3) if you want to understand this code on a deep level. A complete code sample in C++ that compiles and runs is [available here](https://github.com/eliben/code-for-blog/blob/master/2016/expression-problem/c%2B%2B/visitor-extended.cpp).

Adding new **visitors** (ops) with the **visitor pattern** is easy. Our challenge is to add a new *type* without upheaving too much existing code. Let's see how it's done.

### Evaluator visitor

One small design change that we should make to the original visitor pattern is use `virtual` inheritance for `Evaluator`, for reasons that will soon become obvious:

```C++
class Evaluator: virtual public ExprVisitor
{
	// .. the rest is the same
};

```

### Add a new type 

Now we're going to add a new type - `FunctionCall`:

```c++
// This is the new ("extended") expression we're adding.
class FunctionCall: public Expr
{
public:
	FunctionCall(const std::string &name, const Expr &argument) :
					name_(name), argument_(argument)
	{
	}

	void Accept(ExprVisitor *visitor) const
	{
		ExprVisitorWithFunctionCall *v = dynamic_cast<ExprVisitorWithFunctionCall*>(visitor);
		if (v == nullptr)
		{
			std::cerr << "Fatal: visitor is not ExprVisitorWithFunctionCall\n";
			exit(1);
		}
		v->VisitFunctionCall(*this);
	}

private:
	std::string name_;
	const Expr &argument_;
};

```

### New evaluator visitor

Since we don't want to modify the existing visitors, we create a new one, extending `Evaluator` for function calls. But first, we need to extend the `ExprVisitor` interface to support the new type:

```C++
class ExprVisitorWithFunctionCall: virtual public ExprVisitor
{
public:
	virtual void VisitFunctionCall(const FunctionCall &fc) = 0;
};

```

Finally, we write the new evaluator, which extends `Evaluator` and supports the new type:

```c++
class EvaluatorWithFunctionCall: public ExprVisitorWithFunctionCall, public Evaluator
{
public:
	void VisitFunctionCall(const FunctionCall &fc)
	{
		std::cout << "Visiting FunctionCall!!\n";
	}
};

```

> NOTE: 
>
> 继承 `Evaluator` 的目的是: inherits all functionality from `Evaluator`
>
> 继承 `ExprVisitorWithFunctionCall` 的目的是: implements the `ExprVisitorWithFunctionCall` interface

**Multiple inheritance**, **virtual inheritance**, **dynamic type checking**... that's pretty hard-core C++ we have to use here, but there's no choice. Unfortunately, **multiple inheritance** is the only way C++ lets us express the idea that a class implements some interface while at the same time deriving functionality from another class. What we want to have here is an evaluator (`EvaluatorWithFunctionCall`) that inherits all functionality from `Evaluator`, and also implements the `ExprVisitorWithFunctionCall` interface. In Java, we could say something like:

```java
class EvaluatorWithFunctionCall extends Evaluator implements ExprVisitor {
  // ...
}
```

But in C++ **virtual multiple inheritance** is the tool we have. The virtual part of the inheritance is essential here for the compiler to figure out that the `ExprVisitor` base underlying both `Evaluator` and `ExprVisitorWithFunctionCall` is the same and should only appear once in `EvaluatorWithFunctionCall`. Without virtual, the compiler would complain that `EvaluatorWithFunctionCall` doesn't implement the `ExprVisitor` interface.

This is a solution, alright. We kinda added a new type `FunctionCall` and can now visit it without changing existing code (assuming the virtual inheritance was built into the design from the start to anticipate this approach). Here I am using this "kinda" word again... it's time to explain why.

This approach has multiple flaws, in my opinion:

1 Note the `dynamic_cast` in `FunctionCall::Accept`. It's fairly ugly that we're forced to mix in dynamic checks into this code, which should supposedly rely on static typing and the compiler. But it's just a sign of a larger problem.

2 If we have an instance of an `Evaluator`, it will no longer work on the whole extended expression tree since it has no understanding of `FunctionCall`. It's easy to say that all new evaluators should rather be `EvaluatorWithFunctionCall`, but we don't always control this. What about code that was already written? What about `Evaluator`s created in third-party or library code which we have no control of?

3 The virtual inheritance is not the only provision we have to build into the design to support this pattern. Some visitors would need to create new, recursive visitors to process complex expressions. But we can't anticipate in advance which dynamic type of visitor needs to be created. Therefore, the visitor interface should also accept a "visitor factory" which extended visitors will supply. I know this sounds complicated, and I don't want to spend more time on this here - but the Krishnamurthi paper addresses this issue extensively in section 3.4

4 Finally, the solution is unwieldy for realistic applications. Adding one new type looks manageable; what about adding 15 new types, gradually over time? Imagine the horrible zoo of `ExprVisitor` extensions and dynamic checks this would lead to.

Yeah, programming is hard. I could go on and on about the limitations of classical OOP and how they surface in this example [[3\]](https://eli.thegreenplace.net/2016/the-expression-problem-and-its-solutions/#id9). Instead, I'll just present how the expression problem can be solved in a language that supports multiple dispatch and separates the defintion of methods from the bodies of types they act upon.

## Solving the expression problem in Clojure

There are a number of ways the expression problem as displayed in this article can be solved in Clojure using the language's built-in features. Let's start with the simplest one - multi-methods.

## Is multiple dispatch necessary to cleanly solve the expression problem?

## Another Clojure solution - using protocols

## Small interfaces are extensibility-friendly