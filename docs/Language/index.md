# Language



## 一切“描述”都是语言？

当谈到**语言**后，那么得说说“描述”这个词了，感觉这个词是一个非常宽泛、非常囊括的词，比如：

在wikipedia [Language of mathematics](https://en.wikipedia.org/wiki/Language_of_mathematics)的"The meanings of mathematics"段中就使用了“describes ”这个词（这段话总结的太好以至于我忍不住地把它摘录过来了）：

> **Mathematics describes the real world**: 
>
> many areas of mathematics originated with attempts to **describe** and solve real world phenomena - from measuring farms ([geometry](https://en.wikipedia.org/wiki/Geometry)) to falling apples ([calculus](https://en.wikipedia.org/wiki/Calculus)) to gambling(赌博) ([probability](https://en.wikipedia.org/wiki/Probability)). Mathematics is widely used in modern [physics](https://en.wikipedia.org/wiki/Mathematical_physics) and [engineering](https://en.wikipedia.org/wiki/Engineering), and has been hugely successful in helping us to understand more about the universe around us from its largest scales ([physical cosmology](https://en.wikipedia.org/wiki/Physical_cosmology)) to its smallest ([quantum mechanics](https://en.wikipedia.org/wiki/Quantum_mechanics)). Indeed, the very success of mathematics in this respect has been a source of puzzlement for some philosophers (see [The Unreasonable Effectiveness of Mathematics in the Natural Sciences](https://en.wikipedia.org/wiki/The_Unreasonable_Effectiveness_of_Mathematics_in_the_Natural_Sciences) by [Eugene Wigner](https://en.wikipedia.org/wiki/Eugene_Wigner)).
>
> **Mathematics describes abstract structures**: 
>
> on the other hand, there are areas of pure mathematics which deal with [abstract structures](https://en.wikipedia.org/wiki/Abstract_structure), which have no known physical counterparts at all. However, it is difficult to give any categorical examples here, as even the most abstract structures can be co-opted as models in some branch of physics (see [Calabi-Yau spaces](https://en.wikipedia.org/wiki/Calabi-Yau_spaces) and [string theory](https://en.wikipedia.org/wiki/String_theory)).
>
> > NOTE: 这和computer science密切相关
>
> **Mathematics describes mathematics**: mathematics can be used reflexively to describe itself—this is an area of mathematics called [metamathematics](https://en.wikipedia.org/wiki/Metamathematics).



那不禁想问：数学是一门语言吗？如果从“描述”的角度来看话，我觉得可以回答“是”，下面是原文中紧跟着的对这个问题的论述：

> Mathematics can communicate a range of meanings that is as wide as (although different from) that of a **natural language**. As [English](https://en.wikipedia.org/wiki/England) mathematician [R.L.E. Schwarzenberger](https://en.wikipedia.org/wiki/Rolph_Ludwig_Edward_Schwarzenberger) says:
>
> > *My own attitude, which I share with many of my colleagues, is simply that **mathematics is a language**. Like English, or Latin, or Chinese, there are certain concepts for which mathematics is particularly well suited: it would be as foolish to attempt to write a love poem in the language of mathematics as to prove the [Fundamental Theorem of Algebra](https://en.wikipedia.org/wiki/Fundamental_Theorem_of_Algebra) using the English language.*

根据上面的论述来看，[English](https://en.wikipedia.org/wiki/England) mathematician [R.L.E. Schwarzenberger](https://en.wikipedia.org/wiki/Rolph_Ludwig_Edward_Schwarzenberger) 认为 数学是一门语言。



让我们沿着这个思路进一步进行推广就得到本小节的标题所描述的问题：“一切“描述”都是语言？”，这个问题我无法给出答案，以我目前的认知水平，我觉得是的。





## Property of language

### 语言的递归性

像CFG就具备递归性，有[recursive grammar](https://en.wikipedia.org/wiki/Recursive_grammar)的概念。关于语言的递归性在[Production(computer-science)](./Formal-grammar/wikipedia-Production(computer-science).md)、[Chomsky-hierarchy](./Formal-grammar/Chomsky-hierarchy/wikipedia-Chomsky-hierarchy.md)中有专门的描述。

See also:

- [Recursive language](https://en.wikipedia.org/wiki/Recursive_language)

### Human-readable and machine-readable 

下面这段是我在阅读[The Python Language Specification](https://realpython.com/cpython-source-code-guide/#the-python-language-specification)时遇到的：

> Contained within the CPython source code is the definition of the Python language. This is the reference specification used by all the Python interpreters.
>
> The specification is in both **human-readable** and **machine-readable** format. Inside the documentation is a detailed explanation of the Python language, what is allowed, and how each statement should behave.

它对我的启发是：

- 不同的语言有着各自的优势，比如有的语言就不是machine-readable。
- 在工程中，我们往往需要将一种描述方式转换为另外一种描述方式



## 不同语言有着各自的优势

[English](https://en.wikipedia.org/wiki/England) mathematician [R.L.E. Schwarzenberger](https://en.wikipedia.org/wiki/Rolph_Ludwig_Edward_Schwarzenberger) 的这番言论（参见上一节）向我们揭示了：不同的语言有着各自的优势，即有的语言是非常适合于描述某一类事物（或者问题）的，或者说，使用不同的语言来描述相同的问题，使用这种语言更加地便利，更加易于理解，而有的语言则可能比较繁琐且不利于理解，也就是对这类问题而已，这种语言更加地**expressive**。正如它所总结的这个例子，自然语言显然更加适合于表达情感，数学语言更加适合于进行严格地证明。

我们知道，目前已经有非常多的programming language了，维基百科的[List of programming languages](https://en.wikipedia.org/wiki/List_of_programming_languages)中，已经收录了约700中programming language，所以，我们有必要分析一下不同的programming language的各自的优势。关于此，参见工程[programming-language](https://dengking.github.io/programming-language/)的文章Expressive of programming language。



## 语言的expressive power

参见`./Expressive-power`章节。



## 如何来进行描述/如何选择语言？

如何来进行描述？作为一个software engineer，这是需要我们不断地进行思考的问题，下面是我的一些经验: 

### 使用不同的学科的语言来进行描述

通过前面的内容，我们应该已经对语言有了更加宽泛的认识了。不同的学科创建了各自的理论体系（创建了概念、规则等），这就形成了该学科的特有的**语言**，这就形成了对于同一个事物，各个学科都可以使用自己的语言来对它进行描述，这就好比对于“苹果”，中文、英文、法文有着各自的描述方式。

拥有这样的认知是非常重要的，比如，当我们在阅读维基百科的一些文章的时候，常常会碰到的一种情况是某某概念，数学中怎么描述、计算机科学中怎么描述、语言学中怎么描述。

拥有这样的认知对于软件工程师尤其重要，正如在本文开头做说的：

> 我们所做的很多工作，就是将人们使用[natural language](https://en.wikipedia.org/wiki/Natural_language)、[language of mathematics](https://en.wikipedia.org/wiki/Language_of_mathematics)等语言的描述，转换为[programming language](https://en.wikipedia.org/wiki/Programming_language)的描述



**Example: 使用不同的描述语言来描述MLP:**

典型的例子就是对于MLP，对于同一个结构，可以使用不同的语言来进行描述。可以使用**graph**、**math expression**来进行描述，在文章 zhihu [如何直观地解释 backpropagation 算法？ - Anonymous的回答 - 知乎](https://www.zhihu.com/question/27239198/answer/89853077 ) 中有如下描述：

> 多层神经网络本质上是一个多层复合函数，数学是一门简洁但是含义丰富的原因，简单的公式，但是能够表达强大的结构



### Programming model and programming paradigm

在不同领域，有着适合于该领域问题的问题的描述方式，这就是所谓的programming model、programming paradigm。

关于programming model，参见工程programming-language的`Theory\Programming-model`章节。

关于programming paradigm，参见工程programming-language的`Theory\Programming-paradigm`章节。



### 使用更加抽象的语言

典型的例子就是C++ iterator、C++ range。iterator是一种非常强大的抽象的描述方式，可以抽象地描述container、stream。

### 使用适合于问题的语言

比如使用DSL；

比如创造适合于该领域的语言，JavaScript就是这样的一个例子；

