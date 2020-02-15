# [Mathematical logic](https://en.wikipedia.org/wiki/Mathematical_logic)

快速学习该理论的一些笔记。首先学习一些基础概念，然后在去学习复杂一些的概念。



## [Axiom](https://en.wikipedia.org/wiki/Axiom) and [Rule of inference](https://en.wikipedia.org/wiki/Rule_of_inference) and [Theorem](https://en.wikipedia.org/wiki/Theorem)

[Axiom](https://en.wikipedia.org/wiki/Axiom) 可以作为 [Rule of inference](https://en.wikipedia.org/wiki/Rule_of_inference) 的  [premise](https://en.wikipedia.org/wiki/Premise)（前置条件），结果推导，从而得到 [Theorem](https://en.wikipedia.org/wiki/Theorem)

### [Axiom](https://en.wikipedia.org/wiki/Axiom)

公理，总是为True

An **axiom** or **postulate** is a statement that is taken to be [true](https://en.wikipedia.org/wiki/Truth), to serve as a [premise](https://en.wikipedia.org/wiki/Premise)（前置条件） or starting point for further reasoning and arguments. 



### [Rule of inference](https://en.wikipedia.org/wiki/Rule_of_inference)

In [logic](https://en.wikipedia.org/wiki/Logic), a **rule of inference**, **inference rule** or **transformation rule** is a [logical form](https://en.wikipedia.org/wiki/Logical_form) consisting of a function which takes premises, analyzes their [syntax](https://en.wikipedia.org/wiki/Syntax_(logic)), and returns a conclusion (or [conclusions](https://en.wikipedia.org/wiki/Multiple-conclusion_logic)). For example, the rule of inference called *[modus ponens](https://en.wikipedia.org/wiki/Modus_ponens)* takes two premises, one in the form "If p then q" and another in the form "p", and returns the conclusion "q". The rule is valid with respect to the semantics of [classical logic](https://en.wikipedia.org/wiki/Classical_logic) (as well as the semantics of many other [non-classical logics](https://en.wikipedia.org/wiki/Non-classical_logic)), in the sense that if the premises are true (under an interpretation), then so is the conclusion.

推导规则。“premise"的中文意思是”前提“。对它的简单理解：如果前提条件都满足，则可以得出结论。

在原文的[The standard form of rules of inference](https://en.wikipedia.org/wiki/Rule_of_inference)段给出的形式是非常任意理解的。

### [Theorem](https://en.wikipedia.org/wiki/Theorem)

In [mathematics](https://en.wikipedia.org/wiki/Mathematics), a **theorem** is a non-self-evident [statement](https://en.wikipedia.org/wiki/Statement_(logic)) that has been [proven](https://en.wikipedia.org/wiki/Mathematical_proof) to be true, either on the basis of generally accepted statements such as [axioms](https://en.wikipedia.org/wiki/Axiom) or on the basis previously established statements such as other theorems. A theorem is hence a [logical consequence](https://en.wikipedia.org/wiki/Logical_consequence) of the axioms, with a [proof](https://en.wikipedia.org/wiki/Mathematical_proof) of the theorem being a logical argument which establishes its truth through the **inference rules** of a [deductive system](https://en.wikipedia.org/wiki/Deductive_system). 

定理。

上面这段话中的**inference rules**就是[Rule of inference](https://en.wikipedia.org/wiki/Rule_of_inference)。



## [Well-formed formula](https://en.wikipedia.org/wiki/Well-formed_formula)

“formula”的中文意思是“公式”，“well-formed”即良构的，也就是符合grammar的意思（如果有一定的formal language的基础，理解well-formed是比较容易的）。

关于formula的例子是很多的：

- Newton-Leibniz formula

- grammar rule就是formula。

比如在原文的[Propositional calculus](http://en.wikipedia.org/wiki/Propositional_calculus)。

## [Proof theory](https://en.wikipedia.org/wiki/Proof_theory)

**Proof theory** is a major branch  of [mathematical logic](https://en.wikipedia.org/wiki/Mathematical_logic) that represents [proofs](https://en.wikipedia.org/wiki/Mathematical_proof) as formal [mathematical objects](https://en.wikipedia.org/wiki/Mathematical_object), facilitating their analysis by mathematical techniques. Proofs are typically presented as inductively-defined [data structures](https://en.wikipedia.org/wiki/Data_structures) such as plain lists, boxed lists, or [trees](https://en.wikipedia.org/wiki/Tree_(data_structure)), which are constructed according to the [axioms](https://en.wikipedia.org/wiki/Axiom) and [rules of inference](https://en.wikipedia.org/wiki/Rule_of_inference) of the logical system. As such, proof theory is [syntactic](https://en.wikipedia.org/wiki/Syntax_(logic)) in nature, in contrast to [model theory](https://en.wikipedia.org/wiki/Model_theory), which is [semantic](https://en.wikipedia.org/wiki/Formal_semantics_(logic)) in nature.

证明理论，描述如何来进行证明，按照上述描述，就是不断地使用[axioms](https://en.wikipedia.org/wiki/Axiom) and [rules of inference](https://en.wikipedia.org/wiki/Rule_of_inference) 进行推导的过程 ，这个过程推导过程是可以展示为一种数据结构，比如列表、树。[Parse tree](http://en.wikipedia.org/wiki/Parse_tree)就是一个典型的例子，在自顶向下[parsing](https://en.wikipedia.org/wiki/Parsing)的过程中，parser不断地使用production进行推导（expand），最终生成了一棵parse tree。

注意，上面这段话中的“inductively-defined”所指为[recursive definition](https://en.wikipedia.org/wiki/Recursive_definition)，即递归定义。



### [Formal proof](https://en.wikipedia.org/wiki/Formal_proof)

有了前面的这些铺垫，现在理解[Formal proof](https://en.wikipedia.org/wiki/Formal_proof)就不难了。

In [logic](https://en.wikipedia.org/wiki/Logic) and [mathematics](https://en.wikipedia.org/wiki/Mathematics), a **formal proof** or **derivation** is a finite sequence of [sentences](https://en.wikipedia.org/wiki/Proposition_(philosophy)) (called [well-formed formulas](https://en.wikipedia.org/wiki/Well-formed_formula) in the case of a [formal language](https://en.wikipedia.org/wiki/Formal_language)), each of which is an [axiom](https://en.wikipedia.org/wiki/Axiom), an assumption, or follows from the preceding sentences in the sequence by a [rule of inference](https://en.wikipedia.org/wiki/Rule_of_inference).

上面这段话中的“each of which”是修饰 “sentences” 的定语从句。

It differs from a natural language argument in that it is rigorous, unambiguous and mechanically checkable.

这段话所描述的是formal的优势所在。

The theorem is a [syntactic consequence](https://en.wikipedia.org/wiki/Syntactic_consequence) of all the well-formed formulas preceding it in the proof. 

证明的目的是得到theorem？

Checking formal proofs is usually simple, while the problem of *finding* proofs ([automated theorem proving](https://en.wikipedia.org/wiki/Automated_theorem_proving)) is usually [computationally intractable](https://en.wikipedia.org/wiki/Computationally_intractable#Intractability) and/or only [semi-decidable](https://en.wikipedia.org/wiki/Semi-decidable), depending upon the formal system in use.

上面这段话中的“finding proof”所指的应该是给定theorem ，取寻找得到这个theorem的proof，这非常类似于[parsing](http://en.wikipedia.org/wiki/Parsing)。

## 思考：proof VS inference

证明和推理的差异？证明的过程是不断地进行infer，即不断地使用[Rule of inference](https://en.wikipedia.org/wiki/Rule_of_inference)。

## [Formal system](https://en.wikipedia.org/wiki/Formal_system)

A **formal system** is used for inferring theorems from axioms according to a set of rules. These rules, which are used for carrying out the inference of theorems from axioms, are the **logical calculus** of the formal system. A formal system is essentially an "[axiomatic system](https://en.wikipedia.org/wiki/Axiomatic_system)". In 1921, David Hilbert proposed to use such system as the foundation for the knowledge in [mathematics](https://en.wikipedia.org/wiki/Mathematics). A formal system may represent a well-defined [system of abstract thought](https://en.wikipedia.org/wiki/Abstraction).

The term *formalism* is sometimes a rough synonym for *formal system*, but is also refers to a given style of [notation](https://en.wikipedia.org/wiki/Notation), for example, [Paul Dirac](https://en.wikipedia.org/wiki/Paul_Dirac)'s [bra–ket notation](https://en.wikipedia.org/wiki/Bra–ket_notation).

有了前面的理论基础， 现在来看formal system应该不难理解它了。如果将一个formal system看做是一个机器的话，它需要有如下配置：

- [Deductive inference（deductive apparatus）](https://en.wikipedia.org/wiki/Formal_system#Deductive_inference)

那这个机器可以用来做什么呢？

- proof

### 使用formal system来描述formal grammar

通过上面的描述，可以得知：一个语言的formal grammar其实可以看做是一个formal system，formal grammar generate sentence的过程其实就是formal system进行formal proof的过程；parsing的过程其实是find proof的过程。更多关于此的内容，在Formal-language章节中会进行描述。

### 提及formal system的文章

[Formal proof](https://en.wikipedia.org/wiki/Formal_proof)的[Formal systems](https://en.wikipedia.org/wiki/Formal_proof#Formal_systems)

> A formal system is used to [derive](https://en.wikipedia.org/wiki/Proof_theory) one expression from one or more other expressions.

### [List of formal systems](https://en.wikipedia.org/wiki/List_of_formal_systems)

- [Lambda calculus](https://en.wikipedia.org/wiki/Lambda_calculus)

## [Mathematical logic](https://en.wikipedia.org/wiki/Mathematical_logic) and [formal language](https://en.wikipedia.org/wiki/Formal_language)

维基百科将[formal language](https://en.wikipedia.org/wiki/Formal_language)也归入到了[Mathematical logic](https://en.wikipedia.org/wiki/Mathematical_logic)领域中。使用[Mathematical logic](https://en.wikipedia.org/wiki/Mathematical_logic)的思想来看待formal language中的一些列问题是更加容易理解的。




