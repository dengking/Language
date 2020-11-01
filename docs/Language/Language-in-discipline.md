# 不同学科/领域中的语言(或者说表示方式)

各种学科/领域，在进行研究的时候，需要使用简洁的语言来**描述**/**表示**复杂的问题，以达到[抽象](https://en.wikipedia.org/wiki/Abstraction)的目的，抽象的过程对于任何学科的理论的建立都是至关重要的，因为抽象的过程是对问题本质的靠近的过程。因此不同学科就创造了该领域的语言，下面总结了一些常见的学科中使用的语言(或者说表示方式)：

## Mathematics

数学中使用math expression来表示计算，它是human-readable、machine-readable。

参见: wikipedia [Expression (mathematics)](https://en.wikipedia.org/wiki/Expression_(mathematics))

## Computer science

computer science中的语言，被称为[сomputer language](https://en.wikipedia.org/wiki/Computer_language)，在wikipedia [сomputer language](https://en.wikipedia.org/wiki/Computer_language) 中对它进行了非常好的分类，下面是参考自其中的分类: 

1) [programming language](https://en.wikipedia.org/wiki/Programming_language)

表示算法，human-readable、machine-readable



2) [Specification language](https://en.wikipedia.org/wiki/Specification_language)



3) [Interface description language](https://en.wikipedia.org/wiki/Interface_description_language) (IDL)

human-readable、machine-readable。下面是一些应用了IDL的一些software:

- Thrift interface description language[¶](https://thrift.apache.org/docs/idl.html#thrift-interface-description-language)

- protobuf



4) [Markup language](https://en.wikipedia.org/wiki/Markup_language)

human-readable、machine-readable，比如: 

- [YAML](https://en.wikipedia.org/wiki/YAML)
- HTML



5) [Data modeling languages](https://en.wikipedia.org/wiki/Category:Data_modeling_languages)



## 描述结构的语言

如何来描述structure？科学家们已经回答了这个问题，下面是一些案例: 

### Abstract syntax description language(ADSL)

在论文 [The Zephyr Abstract Syntax Description Language](https://www.cs.princeton.edu/research/techreps/TR-554-97) 中有这样的总结：

> Regular expressions describe lexical structures  of programming languages.
>
> Context free grammars describe syntactic structures of programming languages .
>
> ASDL describes the [abstract syntax](https://en.wikipedia.org/wiki/Abstract_syntax)  of compiler intermediate representations (IRs) and other tree-like data
> structures.



### [Algebraic data types](https://en.wikipedia.org/wiki/Algebraic_data_type)





### 语言学中的描述结构的语言

在语言学中，[grammar](https://en.wikipedia.org/wiki/Grammar)来描述语言的结构，[formal language](https://en.wikipedia.org/wiki/Well-formed_formula)的grammar是[formal grammar](https://en.wikipedia.org/wiki/Formal_grammar)，比如[context free grammar](https://en.wikipedia.org/wiki/Context-free_grammar)。[Production (computer science)](https://en.wikipedia.org/wiki/Production_(computer_science))常常用来表示[context free grammar](https://en.wikipedia.org/wiki/Context-free_grammar)。



### See also

在我的工程[data-structure](https://github.com/dengking/data-structure)给出了各种数据结构的描述方式，下面给出链接：

- https://github.com/dengking/data-structure/blob/master/docs/tree/representing-trees.md



## Compiler中的语言

在compiler中使用了多种[Intermediate representation](https://en.wikipedia.org/wiki/Intermediate_representation)，这些IR都是对source code的不同的表示/描述。

参见

1) 工程compiler-principle



