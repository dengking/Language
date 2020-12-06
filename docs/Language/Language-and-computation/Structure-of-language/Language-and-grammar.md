# [Language](https://en.wikipedia.org/wiki/Language) and [grammar](https://en.wikipedia.org/wiki/Grammar)

本文重要是基于维基百科[Language](https://en.wikipedia.org/wiki/Language)和维基百科[Grammar](https://en.wikipedia.org/wiki/Grammar)总结而来。

关于”what is language？“，这个问题，我很难给出回答，参考：

- 维基百科[Language](https://en.wikipedia.org/wiki/Language)
- [Language](https://dengking.github.io/Post/Language/Language/) （我的一篇文章）

本章既然是关于语言的，它属于[linguistics](https://en.wikipedia.org/wiki/Linguistics)（语言学），那看看当今语言学的研究吧，下面是摘自维基百科[Language](https://en.wikipedia.org/wiki/Language)的[Modern linguistics](https://en.wikipedia.org/wiki/Language#Modern_linguistics)章节：

> In the 1960s, [Noam Chomsky](https://en.wikipedia.org/wiki/Noam_Chomsky) formulated the [generative theory of language](https://en.wikipedia.org/wiki/Generative_linguistics). According to this theory, the most basic form of language is a set of syntactic rules that is universal for all humans and which underlies the grammars of all human languages. This set of rules is called [Universal Grammar](https://en.wikipedia.org/wiki/Universal_Grammar); for Chomsky, describing it is the primary objective of the discipline of linguistics. Thus, he considered that the grammars of individual languages are only of importance to linguistics insofar as they allow us to deduce the universal underlying rules from which the observable linguistic variability is generated.
>
> In opposition to the formal theories of the generative school, [functional theories of language](https://en.wikipedia.org/wiki/Functional_theories_of_grammar) propose that since language is fundamentally a tool, its structures are best analyzed and understood by reference to their functions. [Formal theories of grammar](https://en.wikipedia.org/wiki/Formal_grammar) seek to define the different elements of language and describe the way they relate to each other as systems of formal rules or operations, while functional theories seek to define the functions performed by language and then relate them to the linguistic elements that carry them out. The framework of [cognitive linguistics](https://en.wikipedia.org/wiki/Cognitive_linguistics) interprets language in terms of the concepts (which are sometimes universal, and sometimes specific to a particular language) which underlie its forms. Cognitive linguistics is primarily concerned with how the mind creates meaning through language

我们目前的关于language的一些问题，基本上都是采用的 [Noam Chomsky](https://en.wikipedia.org/wiki/Noam_Chomsky) 的 [generative theory of language](https://en.wikipedia.org/wiki/Generative_linguistics) 学说，也就是在下一段中会讨论的[Generative grammar](https://en.wikipedia.org/wiki/Generative_grammar)。

## Grammar

在[语言学](https://en.wikipedia.org/wiki/Linguistics)中，使用[**grammar**](https://en.wikipedia.org/wiki/Grammar)来描述语言的结构。只有知道了language的structure，才能够对其进行计算。



语言学家很早就发现了语言也是有结构的，他们使用[Grammar](https://en.wikipedia.org/wiki/Grammar)来描述语言的结构。

在维基百科[Grammar](https://en.wikipedia.org/wiki/Grammar)中总结了关于grammar的[Theoretical frameworks](https://en.wikipedia.org/wiki/Grammar)，如果使用我们的中国话来理解的是，它们是不同的学说或流派，本文重点关注那些基于"innate "[universal grammar](https://en.wikipedia.org/wiki/Universal_grammar)" " 思想的流派，这个思想是由 [Noam Chomsky](https://en.wikipedia.org/wiki/Noam_Chomsky)提出，该思想的核心：

> The basic postulate of UG is that a certain set of [structural rules](https://en.wikipedia.org/wiki/Grammar) are [innate](https://en.wikipedia.org/wiki/A_priori_and_a_posteriori) to humans.

[Generative grammar](https://en.wikipedia.org/wiki/Generative_grammar)就是基于该思想的一个流派，下面对其进行分析。



### [Generative grammar](https://en.wikipedia.org/wiki/Generative_grammar)

这个流派是由 [Noam Chomsky](https://en.wikipedia.org/wiki/Noam_Chomsky) 所创建，它的核心思想是：

> generative grammar considers [grammar](https://en.wikipedia.org/wiki/Grammar) as a system of **rules** that generates exactly those combinations of words that form grammatical sentences in a given language.

这段话的意思是：一句话是根据语法规则推导而生成的。“generate”的中文意思是“生成”，“产生”（意思非常类似于后面会接触到的 [production](https://en.wikipedia.org/wiki/Production_(computer_science) )（产生式）），“rule”是指语法规则。

请思考这些问题：

- 如何来表示这些规则
- 如何来进行推导

这些问题在[compiler-principle](https://dengking.github.io/compiler-principle/)中给出了答案，本章会对这些问题进行进一步地分析。

本章将要介绍的formal grammar就是属于这个流派。

目前我在[NLP](https://dengking.github.io/machine-learning/Application/NLP/NLP/)和[automata-and-formal-language](https://dengking.github.io/automata-and-formal-language)中接触了generative grammar，这项目，前者是关于natural language，后者是关于formal language。



