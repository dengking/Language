# Expression problem

在阅读 eli.thegreenplace [A polyglot's guide to multiple dispatch](https://eli.thegreenplace.net/2016/a-polyglots-guide-to-multiple-dispatch/) 时，其中提及了 expression problem:

> If we don't control the `Shape` base class at all, we're in real trouble. This is an instance of the [expression problem](https://en.wikipedia.org/wiki/Expression_problem). I'll have more to say about the expression problem in a future post, but for now the Wikipedia link will have to do. 

## stackoverflow [What is the 'expression problem'?](https://stackoverflow.com/questions/3596366/what-is-the-expression-problem)

[A](https://stackoverflow.com/a/3776140)

Watch [this lecture](http://channel9.msdn.com/shows/Going+Deep/C9-Lectures-Dr-Ralf-Laemmel-Advanced-Functional-Programming-The-Expression-Problem/).

The idea is that your program is a combination of a **datatype** and **operations** over it. The problem asks for an implementation that allows to add new cases of the type and new operations without the need for recompilation of the old modules and keeping static type safety(no casts or runtime type checks).

It's interesting to notice that in **functional programming languages** it's easy to add new operations, but hard to add cases to the **datatype**. While in an OO language it's the other way round. This is one of the big conceptual differences between the two programming paradigms.

## wikipedia [Expression problem](https://en.wikipedia.org/wiki/Expression_problem)

The **expression problem** is a term used in discussing strengths and weaknesses of various [programming paradigms](https://en.wikipedia.org/wiki/Programming_paradigms) and [programming languages](https://en.wikipedia.org/wiki/Programming_languages).

[Philip Wadler](https://en.wikipedia.org/wiki/Philip_Wadler) coined the term[[1\]](https://en.wikipedia.org/wiki/Expression_problem#cite_note-WadlerPost-1) in response to a discussion with Rice University's [*Programming Languages Team* (PLT)](https://en.wikipedia.org/wiki/Racket_(programming_language)#Development):

> The expression problem is a new name for an old problem.[[2\]](https://en.wikipedia.org/wiki/Expression_problem#cite_note-Reynolds-2)[[3\]](https://en.wikipedia.org/wiki/Expression_problem#cite_note-Cook-3) The goal is to define a datatype by cases, where one can add new cases to the datatype and new functions over the datatype, without recompiling existing code, and while retaining static type safety (e.g., no casts).

### Solutions

There are various solutions to the expression problem. Each solution varies in the amount of code a user must write to implement them, and the language features they require.

- [Multiple dispatch](https://en.wikipedia.org/wiki/Multiple_dispatch)[[11\]](https://en.wikipedia.org/wiki/Expression_problem#cite_note-Chambers_&_Leavens,_Multi-Methods-11)
- [Open classes](https://en.wikipedia.org/wiki/Ruby_(programming_language)#Open_classes)[[12\]](https://en.wikipedia.org/wiki/Expression_problem#cite_note-Clifton_et._al.,_MultiJava_Open_Classes-12)
- [Coproducts](https://en.wikipedia.org/wiki/Coproduct) of [functors](https://en.wikipedia.org/wiki/Functor)[[13\]](https://en.wikipedia.org/wiki/Expression_problem#cite_note-13)
- [Type classes](https://en.wikipedia.org/wiki/Type_class)[[14\]](https://en.wikipedia.org/wiki/Expression_problem#cite_note-Wehr_&_Thiemann,_JavaGI_Type_Classes-14)
- Tagless-final[[15\]](https://en.wikipedia.org/wiki/Expression_problem#cite_note-Carette_et_al.,_Finally_tagless,_partially_evaluated:_Tagless_staged_interpreters_for_simpler_typed_languages-15) / Object algebras[[16\]](https://en.wikipedia.org/wiki/Expression_problem#cite_note-Oliveira_&_Cook,_Object_Algebras-16)
- Polymorphic Variants[[17\]](https://en.wikipedia.org/wiki/Expression_problem#cite_note-Code_Reuse_Through_Polymorphic_Variants-17)