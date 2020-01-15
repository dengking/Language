[TOC]



# [Chomsky hierarchy](https://en.wikipedia.org/wiki/Chomsky_hierarchy)

In the [formal languages](https://en.wikipedia.org/wiki/Formal_language) of [computer science](https://en.wikipedia.org/wiki/Computer_science) and [linguistics](https://en.wikipedia.org/wiki/Linguistics), the **Chomsky hierarchy** (occasionally referred to as the **Chomsky–Schützenberger hierarchy**) is a [containment hierarchy](https://en.wikipedia.org/wiki/Containment_hierarchy) of classes of [formal grammars](https://en.wikipedia.org/wiki/Formal_grammar).

This hierarchy of grammars was described by [Noam Chomsky](https://en.wikipedia.org/wiki/Noam_Chomsky) in 1956. It is also named after [Marcel-Paul Schützenberger](https://en.wikipedia.org/wiki/Marcel-Paul_Schützenberger), who played a crucial role in the development of the theory of [formal languages](https://en.wikipedia.org/wiki/Formal_language).



## The hierarchy

The following table summarizes each of Chomsky's four types of grammars, the class of language it generates, the type of automaton that recognizes it, and the form its rules must have. 

| Grammar |                          Languages                           |                          Automaton                           |               Production rules (constraints)*                |                         Examples                         |
| :-----: | :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: | :------------------------------------------------------: |
| Type-0  | [Recursively enumerable](https://en.wikipedia.org/wiki/Recursively_enumerable_language) | [Turing machine](https://en.wikipedia.org/wiki/Turing_machine) |    $ \alpha A\beta \rightarrow \delta $ (no constraints)     | $ L=\{w|w $ describes a terminating Turing machine$ \} $ |
| Type-1  | [Context-sensitive](https://en.wikipedia.org/wiki/Context-sensitive_grammar) | [Linear-bounded non-deterministic Turing machine](https://en.wikipedia.org/wiki/Linear_bounded_automaton) |      $ \alpha A\beta \rightarrow \alpha \gamma \beta $       |              $ L=\{a^{n}b^{n}c^{n}|n>0\} $               |
| Type-2  | [Context-free](https://en.wikipedia.org/wiki/Context-free_grammar) | Non-deterministic [pushdown automaton](https://en.wikipedia.org/wiki/Pushdown_automaton) |                   $ A\rightarrow \alpha $                    |                 $ L=\{a^{n}b^{n}|n>0\} $                 |
| Type-3  |   [Regular](https://en.wikipedia.org/wiki/Regular_grammar)   | [Finite state automaton](https://en.wikipedia.org/wiki/Finite_state_automaton) | $ A\rightarrow {\text{a}} $ and $ A\rightarrow {\text{a}}B $ |                 $ L=\{a^{n}|n\geq 0\} $                  |

>  Meaning of symbols: 
>
> - $ {\text{a}} $ = terminal
> - $ A $, $ B $ = non-terminal
> - $ \alpha $, $ \beta $, $ \gamma $, $ \delta $ = string of terminals and/or non-terminals
>     -  $ \alpha $, $ \beta $, $ \delta $ = maybe empty 
>     -  $ \gamma $ = never empty 

[![The Chomsky hierarchy](https://upload.wikimedia.org/wikipedia/commons/thumb/9/9a/Chomsky-hierarchy.svg/200px-Chomsky-hierarchy.svg.png)](https://en.wikipedia.org/wiki/File:Chomsky-hierarchy.svg)

 Set inclusions described by the Chomsky hierarchy 

Note that the set of grammars corresponding to [recursive languages](https://en.wikipedia.org/wiki/Recursive_language) is not a member of this hierarchy; these would be properly between Type-0 and Type-1.

Every regular language is context-free, every context-free language is context-sensitive, every context-sensitive language is **recursive** and every **recursive language** is **recursively enumerable**. These are all **proper inclusions**, meaning that there exist recursively enumerable languages that are not context-sensitive, context-sensitive languages that are not context-free and context-free languages that are not regular.

### Type-0 grammars

 *Main article:* [Unrestricted grammar](https://en.wikipedia.org/wiki/Unrestricted_grammar) 

Type-0 grammars include all formal grammars. They generate exactly all languages that can be recognized by a [Turing machine](https://en.wikipedia.org/wiki/Turing_machine). These languages are also known as the [*recursively enumerable*](https://en.wikipedia.org/wiki/Recursively_enumerable_language) or *Turing-recognizable* languages. Note that this is different from the [recursive languages](https://en.wikipedia.org/wiki/Recursive_language), which can be *decided* by an [always-halting Turing machine](https://en.wikipedia.org/wiki/Machine_that_always_halts). 



### Type-1 grammars

 *Main article:* [Context-sensitive grammar](https://en.wikipedia.org/wiki/Context-sensitive_grammar) 

 Type-1 grammars generate [context-sensitive languages](https://en.wikipedia.org/wiki/Context-sensitive_language). These grammars have rules of the form $ \alpha A\beta \rightarrow \alpha \gamma \beta $ with $ A $ a nonterminal and $ \alpha $, $ \beta $ and $ \gamma $ strings of terminals and/or nonterminals. The strings $ \alpha $ and $ \beta $ may be empty, but $ \gamma $ must be nonempty. The rule $ S\rightarrow \epsilon $ is allowed if $ S $ does not appear on the right side of any rule. The languages described by these grammars are exactly all languages that can be recognized by a [linear bounded automaton](https://en.wikipedia.org/wiki/Linear_bounded_automaton) (a nondeterministic Turing machine whose tape is bounded by a constant times the length of the input.) 

### Type-2 grammars

 *Main article:* [Context-free grammar](https://en.wikipedia.org/wiki/Context-free_grammar) 

 Type-2 grammars generate the [context-free languages](https://en.wikipedia.org/wiki/Context-free_language). These are defined by rules of the form $ A\rightarrow \alpha $ with $ A $ being a nonterminal and $ \alpha $ being a string of terminals and/or nonterminals. These languages are exactly all languages that can be recognized by a non-deterministic [pushdown automaton](https://en.wikipedia.org/wiki/Pushdown_automaton). Context-free languages—or rather its subset of [deterministic context-free language](https://en.wikipedia.org/wiki/Deterministic_context-free_language)—are the theoretical basis for the phrase structure of most [programming languages](https://en.wikipedia.org/wiki/Programming_language), though their syntax also includes context-sensitive name resolution due to declarations and [scope](https://en.wikipedia.org/wiki/Scope_(computer_science)). Often a subset of grammars is used to make parsing easier, such as by an [LL parser](https://en.wikipedia.org/wiki/LL_parser). 

### Type-3 grammars

 *Main article:* [Regular grammar](https://en.wikipedia.org/wiki/Regular_grammar) 

 Type-3 grammars generate the [regular languages](https://en.wikipedia.org/wiki/Regular_language). Such a grammar restricts its rules to a single nonterminal on the left-hand side and a right-hand side consisting of a single terminal, possibly followed by a single nonterminal (right regular). Alternatively, the right-hand side of the grammar can consist of a single terminal, possibly preceded by a single nonterminal (left regular). These generate the same languages. However, if left-regular rules and right-regular rules are combined, the language need no longer be regular. The rule $ S\rightarrow \epsilon $ is also allowed here if $ S $ does not appear on the right side of any rule. These languages are exactly all languages that can be decided by a [finite state automaton](https://en.wikipedia.org/wiki/Finite_state_automaton). Additionally, this family of formal languages can be obtained by [regular expressions](https://en.wikipedia.org/wiki/Regular_expression). Regular languages are commonly used to define search patterns and the lexical structure of programming languages. 