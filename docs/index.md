[TOC]

# 前言

出于如下原因我创建了这个项目：

- 在从事[NLP](https://en.wikipedia.org/wiki/Natural_language_processing)相关的项目的开发过程中，遇到了很多和[语言](https://en.wikipedia.org/wiki/Language)相关的理论
- 阅读[《Natural Language Processing with Python》](http://www.nltk.org/book/)时，发现其中涉及了一些和[语言](https://en.wikipedia.org/wiki/Language)相关的理论
- 阅读[《*Compilers: Principles, Techniques, and Tools*》](https://en.wikipedia.org/wiki/Compilers:_Principles,_Techniques,_and_Tools)（龙书）时，发现其中涉及了很多[formal language](https://en.wikipedia.org/wiki/Formal_language)相关的理论

本项目的内容大多数来自:

- 维基百科: [Automata theory](https://en.wikipedia.org/wiki/Automata_theory) : [formal languages](https://en.wikipedia.org/wiki/Formal_language) **and** [formal grammars](https://en.wikipedia.org/wiki/Formal_grammar)
- [Introduction to Automata and Language Theory(aka ***Cinderella Book***)](http://infolab.stanford.edu/~ullman/ialc.html)

这个项目是对[语言](https://en.wikipedia.org/wiki/Language)相关的理论的一个梳理，它主要作为如下项目所涉及的理论的总结：

- [compiler-principle](https://github.com/dengking/compiler-principle)
- [compiler-principle-in-action](https://github.com/dengking/compiler-principle-in-action)
- [Natural-Language-Processing-with-Python](https://github.com/dengking/Natural-Language-Processing-with-Python)



# 学习计划--从入门到精通

[Formal language](https://en.wikipedia.org/wiki/Formal_language)所涉及的理论较多，并且大多数都是比较抽象的，刚开始学习（尤其对于缺乏使用programming language的人来说）可能会感觉比较吃力，以下是觉得比较好的学习计划：

首先搞清楚what is language、what is formal language、what is formal grammar、what is automata、What is the relationship between them，这样就建立起了建立起高屋建瓴的视野，这其实就是算入门了。推荐阅读下面的文章：

- [Formal Languages, Grammars, and Automata](http://www.sti.uniurb.it/aldini/publications/lfga.pdf)

入门了之后，就需要建立起theory framework，最终我们会发现，使用[Chomsky hierarchy](https://en.wikipedia.org/wiki/Chomsky_hierarchy)就能够将整个理论给统一起来；然后再逐个进行细致分析，最后就能够融会贯通，这其实就是精通了。



# Theory Framework

## [Language](https://en.wikipedia.org/wiki/Language)

对语言的一种分类方法：

- [Constructed language](https://en.wikipedia.org/wiki/Constructed_language)
  - [Formal language](https://en.wikipedia.org/wiki/Formal_language)
    - [Programming language](https://en.wikipedia.org/wiki/Programming_language)
- [Natural languages](https://en.wikipedia.org/wiki/Natural_language) 

> Note: 上诉分类所传达的含义有：
>
> - [Formal language](https://en.wikipedia.org/wiki/Formal_language)不是[natural language](https://en.wikipedia.org/wiki/Natural_language) 

## [Formal language](https://en.wikipedia.org/wiki/Formal_language)

提及[formal language](https://en.wikipedia.org/wiki/Formal_language)，就得请出[Noam Chomsky](https://en.wikipedia.org/wiki/Noam_Chomsky)，因为下面的理论框架是由他所建立的，该theory framework的是按照[Chomsky hierarchy](https://en.wikipedia.org/wiki/Chomsky_hierarchy)来进行组织的：

| [Chomsky hierarchy](https://en.wikipedia.org/wiki/Chomsky_hierarchy) | [Grammars](https://en.wikipedia.org/wiki/Formal_grammar)     | Languages                                                    | [Abstract machines](https://en.wikipedia.org/wiki/Abstract_machine) |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Type-0                                                       | [Unrestricted](https://en.wikipedia.org/wiki/Unrestricted_grammar) | [Recursively enumerable](https://en.wikipedia.org/wiki/Recursively_enumerable_language) | [Turing machine](https://en.wikipedia.org/wiki/Turing_machine) |
| —                                                            | (no common name)                                             | [Decidable](https://en.wikipedia.org/wiki/Recursive_language) | [Decider](https://en.wikipedia.org/wiki/Machine_that_always_halts) |
| Type-1                                                       | [Context-sensitive](https://en.wikipedia.org/wiki/Context-sensitive_grammar) | [Context-sensitive](https://en.wikipedia.org/wiki/Context-sensitive_language) | [Linear-bounded](https://en.wikipedia.org/wiki/Linear_bounded_automaton) |
| —                                                            | Positive [range concatenation](https://en.wikipedia.org/wiki/Range_concatenation_grammars) | Positive [range concatenation](https://en.wikipedia.org/wiki/Range_concatenation_language)* | [PTIME](https://en.wikipedia.org/wiki/PTIME) Turing Machine  |
| —                                                            | [Indexed](https://en.wikipedia.org/wiki/Indexed_grammar)     | [Indexed](https://en.wikipedia.org/wiki/Indexed_language)*   | [Nested stack](https://en.wikipedia.org/wiki/Nested_stack_automaton) |
| —                                                            | —                                                            | —                                                            | [Thread automaton](https://en.wikipedia.org/wiki/Thread_automaton) |
| —                                                            | [Linear context-free rewriting systems](https://en.wikipedia.org/wiki/Linear_context-free_rewriting_system) | [Linear context-free rewriting language](https://en.wikipedia.org/wiki/Linear_context-free_rewriting_language) | restricted [Tree stack automaton](https://en.wikipedia.org/wiki/Tree_stack_automaton) |
| —                                                            | [Tree-adjoining](https://en.wikipedia.org/wiki/Tree-adjoining_grammar) | [Tree-adjoining](https://en.wikipedia.org/wiki/Tree-adjoining_grammar) | [Embedded pushdown](https://en.wikipedia.org/wiki/Embedded_pushdown_automaton) |
| Type-2                                                       | [Context-free](https://en.wikipedia.org/wiki/Context-free_grammar) | [Context-free](https://en.wikipedia.org/wiki/Context-free_language) | [Nondeterministic pushdown](https://en.wikipedia.org/wiki/Pushdown_automaton) |
| —                                                            | [Deterministic context-free](https://en.wikipedia.org/wiki/Deterministic_context-free_grammar) | [Deterministic context-free](https://en.wikipedia.org/wiki/Deterministic_context-free_language) | [Deterministic pushdown](https://en.wikipedia.org/wiki/Deterministic_pushdown_automaton) |
| —                                                            | [Visibly pushdown](https://en.wikipedia.org/wiki/Nested_word) | [Visibly pushdown](https://en.wikipedia.org/wiki/Nested_word) | [Visibly pushdown](https://en.wikipedia.org/wiki/Nested_word) |
| Type-3                                                       | [Regular](https://en.wikipedia.org/wiki/Regular_grammar)     | [Regular](https://en.wikipedia.org/wiki/Regular_language)    | [Finite](https://en.wikipedia.org/wiki/Finite-state_machine) |
| —                                                            | —                                                            | [Star-free](https://en.wikipedia.org/wiki/Star-free_language) | [Counter-free (with aperiodic finite monoid)](https://en.wikipedia.org/wiki/Aperiodic_finite_state_automaton) |
| —|	[Non-recursive](https://en.wikipedia.org/wiki/Non-recursive_grammar) | [Finite](https://en.wikipedia.org/wiki/Finite_language)      | [Acyclic finite](https://en.wikipedia.org/wiki/Deterministic_acyclic_finite_state_automaton) |                                                              |

Each category of languages, except those marked by a `*`, is a [proper subset](https://en.wikipedia.org/wiki/Proper_subset) of the category directly above it. Any language in each category is generated by a grammar and by an automaton in the category in the same line.



# 目录结构说明

本工程就是按照[学习计划--从入门到精通](#学习计划--从入门到精通)章节所描述的思路组织的：

- introduction：入门
- theory-framework：理论框架



# Cinderella Book VS Dragon Book

[Introduction to Automata and Language Theory(aka ***Cinderella Book***)](http://infolab.stanford.edu/~ullman/ialc.html)是该领域的经典书籍。

[Introduction to Automata and Language Theory(aka ***Cinderella Book***)](http://infolab.stanford.edu/~ullman/ialc.html)和[Compilers: Principles, Techniques, and Tools (aka "***Dragon Book***")](http://en.wikipedia.org/wiki/Compilers:_Principles,_Techniques,_and_Tools)中的内容其实是紧密关联的，这不仅仅是因为Jeffrey D.Ullman参与了这两本书的编写，而是因为programming language是一种formal language，而Cinderella Book和Dragon Book其实都是在讲述和formal language相关的内容，当然，这些内容仅仅书中的一部分。Cinderella Book专注于讲述automata and language theory，而dragon book的内容则可以分为两个部分front end和back end，显然front end所讲述的内容就和automata and language theory紧密相关了。