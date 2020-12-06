# Synthesizing Object-Oriented and Functional Design to Promote Re-Use

是在阅读 eli.thegreenplace [The Expression Problem and its solutions](https://eli.thegreenplace.net/2016/the-expression-problem-and-its-solutions/) 时，其中介绍了这篇论文。



# [Synthesizing Object-Oriented and Functional Design to Promote Re-Use](https://cs.brown.edu/~sk/Publications/Papers/Published/kff-synth-fp-oo/)

Shriram Krishnamurthi, Matthias Felleisen, Daniel P. Friedman

European Conference on Object-Oriented Programming, 1998

## Abstract

Many problems require recursively specified types of data and a collection of tools that operate on those data. Over time, these problems evolve so that the programmer must extend the toolkit or extend the types and adjust the existing tools accordingly. Ideally, this should be done without modifying existing code. Unfortunately, the prevailing program design strategies do not support both forms of extensibility: functional programming accommodates the addition of tools, while object-oriented programming supports either adding new tools or extending the data set, but not both. In this paper, we present a composite design pattern that synthesizes the best of both approaches and in the process resolves the tension between the two design strategies. We also show how this protocol suggests a new set of linguistic facilities for languages that support class systems.