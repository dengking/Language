# 前言

本章节，首先以[description-and-language](./description-and-language.md)这篇文章作为开头，引出[Formal language](https://en.wikipedia.org/wiki/Formal_language)， 然后对它进行详细的分析。

理论往往不是孤立的，而是相互关联，相互借用的，下面梳理一下[Formal languages](https://en.wikipedia.org/wiki/Formal_language) 和 [Mathematical logic](https://en.wikipedia.org/wiki/Mathematical_logic)之间的关联、[Formal languages](https://en.wikipedia.org/wiki/Formal_language)和[Automata theory](https://en.wikipedia.org/wiki/Automata_theory)之间的关联。

## [Formal languages](https://en.wikipedia.org/wiki/Formal_language) 和 [Mathematical logic](https://en.wikipedia.org/wiki/Mathematical_logic)

在阅读维基百科中关于[Formal language](https://en.wikipedia.org/wiki/Formal_language)的内容时，发现了如下事实：

> [formal languages](https://en.wikipedia.org/wiki/Formal_language) 和[Mathematical logic](https://en.wikipedia.org/wiki/Mathematical_logic)之间共享很多的基础概念

感觉如果从[Mathematical logic](https://en.wikipedia.org/wiki/Mathematical_logic)的逻辑推导的角度来看待[formal languages](https://en.wikipedia.org/wiki/Formal_language) **and** [formal grammars](https://en.wikipedia.org/wiki/Formal_grammar)的话，[formal languages](https://en.wikipedia.org/wiki/Formal_language) **and** [formal grammars](https://en.wikipedia.org/wiki/Formal_grammar)的很多内容就变得非常容易理解了，并且context free grammar（一种[formal grammars](https://en.wikipedia.org/wiki/Formal_grammar)）本质上就是一种[推导规则](https://en.wikipedia.org/wiki/Formation_rule)，我觉得；两者对于理解[Turing machine](https://en.wikipedia.org/wiki/Turing_machine)都是至关重要的。

需要总结一下formal language中的一些概念和mathematical logic中的一些概念之间的对应关系，如下：

| [Formal language](https://en.wikipedia.org/wiki/Formal_language) | [Mathematical logic](https://en.wikipedia.org/wiki/Mathematical_logic) |                                                      |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ---------------------------------------------------- |
| [Production rule](https://en.wikipedia.org/wiki/Production_(computer_science)) | [Formation rule](https://en.wikipedia.org/wiki/Formation_rule) | [Rewriting](https://en.wikipedia.org/wiki/Rewriting) |
|                                                              |                                                              |                                                      |
|                                                              |                                                              |                                                      |

按照公式进行推导从另外一个角度来看其实是重写，不断地进行替换。感觉数理逻辑本质上就是这个东西。从这个角度来看，parsing的过程其实就是不断的推导的过程，不断的重写的过程。由于可能的推导格式是非常多的，所以需要不断地进行尝试，这个过程其实就是[search](https://en.wikipedia.org/wiki/Search_algorithm)，所以从这个角度来看，[parsing](https://en.wikipedia.org/wiki/Parsing)所做的工作其实就是推导加search。自顶向下其实所对应的是正向推导，自底向上其实所对应的就是方向推导。

不同的学科对同一事物的命名可能不同，但是它们本质上所描述的是同一事物。

其实上述所有这些讨论，本质上都是属于[Logic](https://en.wikipedia.org/wiki/Logic)学的范轴，逻辑学中的很多问题，需要考虑计算机的实现。

[Set theory](https://en.wikipedia.org/wiki/Set_theory)是数学的基石所在，很多其他数学学科都是建立在它的基础之上。

我一直想要搞清楚的closure就是基于逻辑推导和集合论的。

推理：[Inference](https://en.wikipedia.org/wiki/Inference)

## [Automata theory](https://en.wikipedia.org/wiki/Automata_theory)和[Formal language](https://en.wikipedia.org/wiki/Formal_language)

[Chomsky hierarchy](https://en.wikipedia.org/wiki/Chomsky_hierarchy)将[Automata theory](https://en.wikipedia.org/wiki/Automata_theory)和[formal language](https://en.wikipedia.org/wiki/Formal_language)进行了关联和对应。需要注意的是，[Automata theory](https://en.wikipedia.org/wiki/Automata_theory)在其他领域有着非常广泛的应用。





## [Turing machine](https://en.wikipedia.org/wiki/Turing_machine) and [Mathematical logic](https://en.wikipedia.org/wiki/Mathematical_logic)

图灵机需要能够实现各种形式的推导过程。