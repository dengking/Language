# [Formal system](https://en.wikipedia.org/wiki/Formal_system)

A **formal system** is used for inferring **theorems** from **axioms** according to a set of **rules**. These rules, which are used for carrying out the inference of theorems from axioms, are the **logical calculus** of the formal system. A formal system is essentially an "[axiomatic system](https://en.wikipedia.org/wiki/Axiomatic_system)". In 1921, David Hilbert proposed to use such system as the foundation for the knowledge in [mathematics](https://en.wikipedia.org/wiki/Mathematics). A formal system may represent a well-defined [system of abstract thought](https://en.wikipedia.org/wiki/Abstraction).

> NOTE: 如何理解theorem和axiom？参考一下下面的内容：
>
> - [Axiom](https://en.wikipedia.org/wiki/Axiom)：公理，一定为True
>- [Theorem](https://en.wikipedia.org/wiki/Theorem)：定理，由axiom推理而来
> 

The term *formalism* is sometimes a rough synonym for *formal system*, but is also refers to a given style of [notation](https://en.wikipedia.org/wiki/Notation), for example, [Paul Dirac](https://en.wikipedia.org/wiki/Paul_Dirac)'s [bra–ket notation](https://en.wikipedia.org/wiki/Bra–ket_notation).



## Background

Each formal system uses primitive [symbols](https://en.wikipedia.org/wiki/Symbol_(formal)) (which collectively form an [alphabet](https://en.wikipedia.org/wiki/Alphabet_(computer_science))) to finitely construct a [formal language](https://en.wikipedia.org/wiki/Formal_language) from a set of [axioms](https://en.wikipedia.org/wiki/Axiom) through inferential [rules of formation](https://en.wikipedia.org/wiki/Rules_of_formation).

The system thus consists of valid **formulas** built up through finite combinations of the primitive symbols—combinations that are formed from the axioms in accordance with the stated rules.

More formally, this can be expressed as the following:

1. A finite set of symbols, known as the alphabet, which concatenate **formulas**, so that a formula is just a finite string of symbols taken from the alphabet.
2. A [grammar](https://en.wikipedia.org/wiki/Formal_grammar) consisting of rules to form formulas from simpler formulas. A formula is said to be [well-formed](https://en.wikipedia.org/wiki/Well-formed_formula) if it can be formed using the rules of the formal grammar. It is often required that there be a decision procedure for deciding whether a formula is well-formed.
3. A set of axioms, or [axiom schemata](https://en.wikipedia.org/wiki/Axiom_schema), consisting of well-formed formulas.
4. A set of [inference rules](https://en.wikipedia.org/wiki/Rule_of_inference). A well-formed formula that can be inferred from the axioms is known as a theorem of the formal system.

### Recursive

A formal system is said to be [recursive](https://en.wikipedia.org/wiki/Recursive_set) (i.e. effective) or recursively enumerable if the set of axioms and the set of inference rules are [decidable sets](https://en.wikipedia.org/wiki/Decidable_set) or [semidecidable sets](https://en.wikipedia.org/wiki/Recursively_enumerable_set), respectively.



# [List of formal systems](https://en.wikipedia.org/wiki/List_of_formal_systems)