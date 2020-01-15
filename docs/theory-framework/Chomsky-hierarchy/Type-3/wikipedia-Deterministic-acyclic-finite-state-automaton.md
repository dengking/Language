[TOC]



# [Deterministic acyclic finite state automaton](https://en.wikipedia.org/wiki/Deterministic_acyclic_finite_state_automaton)

In [computer science](https://en.wikipedia.org/wiki/Computer_science), a **deterministic acyclic finite state automaton** (**DAFSA**),[[1\]](https://en.wikipedia.org/wiki/Deterministic_acyclic_finite_state_automaton#cite_note-daciuk-1) also called a **directed acyclic word graph** (**DAWG**; though that name also refers to a [related data structure](https://en.wikipedia.org/wiki/Suffix_automaton) that functions as a suffix index[[2\]](https://en.wikipedia.org/wiki/Deterministic_acyclic_finite_state_automaton#cite_note-2)) is a [data structure](https://en.wikipedia.org/wiki/Data_structure) that represents a set of [strings](https://en.wikipedia.org/wiki/String_(computer_science)), and allows for a query operation that tests whether a given string belongs to the set in time proportional to its length. Algorithms exist to construct and maintain such automata,[*[citation needed](https://en.wikipedia.org/wiki/Wikipedia:Citation_needed)*] while keeping them [minimal](https://en.wikipedia.org/wiki/DFA_minimization).

A DAFSA is a special case of a [finite state recognizer](https://en.wikipedia.org/wiki/Finite_state_recognizer) that takes the form of a [directed acyclic graph](https://en.wikipedia.org/wiki/Directed_acyclic_graph) with a single source vertex (a vertex with no incoming edges), in which each edge of the graph is labeled by a letter or symbol, and in which each vertex has at most one outgoing edge for each possible letter or symbol. The strings represented by the DAFSA are formed by the symbols on paths in the graph from the source vertex to any sink vertex (a vertex with no outgoing edges). In fact, a [deterministic finite state automaton](https://en.wikipedia.org/wiki/Deterministic_finite_state_automaton) is acyclic [if and only if](https://en.wikipedia.org/wiki/If_and_only_if) it recognizes a [finite set of strings](https://en.wikipedia.org/wiki/Finite_language).[[1\]](https://en.wikipedia.org/wiki/Deterministic_acyclic_finite_state_automaton#cite_note-daciuk-1)



## application

- [jieba](https://github.com/fxsjy/jieba)
- [jieba分词算法源码解析](https://blog.csdn.net/yuanlisky/article/details/55050071)
- [jieba分词的原理](https://www.cnblogs.com/echo-cheng/p/7967221.html)