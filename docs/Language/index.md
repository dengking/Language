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





## Classification of language

在wikipedia [Language](https://en.wikipedia.org/wiki/Language) 中给出 了language的简单分类方法: 

1) [Constructed language](https://en.wikipedia.org/wiki/Constructed_language) 人造语言

2) [Natural languages](https://en.wikipedia.org/wiki/Natural_language) 自然语言

3) [Formal language](https://en.wikipedia.org/wiki/Formal_language) 形式语言

[Programming language](https://en.wikipedia.org/wiki/Programming_language) 编程语言，它是一种 formal language。后面会对它进行详细介绍。

需要注意的是: [Formal language](https://en.wikipedia.org/wiki/Formal_language) 不是 [natural language](https://en.wikipedia.org/wiki/Natural_language) 。



## 形式语言

科学需要严谨的、准确的描述方式，所以它使用的语言不同于人类说话时使用的[自然语言](https://en.wikipedia.org/wiki/Natural_language)，在科学中，往往使用的一种叫做 [formal language](https://en.wikipedia.org/wiki/Well-formed_formula) 的语言，这类语言有着诸多优良的特性，它是很多学科的基础。它相较于[自然语言](https://en.wikipedia.org/wiki/Natural_language)，有着诸多优势，其中一个优势就是 machine-readable，所以这也是它吸引计算机科学家的一个原因。在下章将对其进行详细讨论。
