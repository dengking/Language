# 如何来进行描述？

各种学科，在进行研究的时候，往往是使用简洁的公式/表达式来**描述**/**表示**复杂的问题，以达到简化的目的。其实是一种[抽象](https://en.wikipedia.org/wiki/Abstraction)，抽象的过程对于任何学科都是至关重要的，因为抽象的过程是对本质的靠近的过程。

下面总结了在各个学科中都非常常见的描述/表示方式：

# 数学中的描述方式

## [Expression (mathematics)](https://en.wikipedia.org/wiki/Expression_(mathematics))

表示计算，human-readable、machine-readable



# 语言学中的描述方式

在语言学中，[grammar](https://en.wikipedia.org/wiki/Grammar)来描述语言的结构，[formal language](https://en.wikipedia.org/wiki/Well-formed_formula)的grammar是[formal grammar](https://en.wikipedia.org/wiki/Formal_grammar)，比如[context free grammar](https://en.wikipedia.org/wiki/Context-free_grammar)。[Production (computer science)](https://en.wikipedia.org/wiki/Production_(computer_science))常常用来表示[context free grammar](https://en.wikipedia.org/wiki/Context-free_grammar)。



# 计算机科学

## [сomputer language](https://en.wikipedia.org/wiki/Computer_language)

### [programming language](https://en.wikipedia.org/wiki/Programming_language)

表示算法，human-readable、machine-readable

### [Specification language](https://en.wikipedia.org/wiki/Specification_language)



### [Interface description language](https://en.wikipedia.org/wiki/Interface_description_language)

human-readable、machine-readable

### [Markup language](https://en.wikipedia.org/wiki/Markup_language)

human-readable、machine-readable

- [YAML](https://en.wikipedia.org/wiki/YAML)

### [Data modeling languages](https://en.wikipedia.org/wiki/Category:Data_modeling_languages)

## 描述结构

### ADSL

在论文[The Zephyr Abstract Syntax Description Language](https://www.cs.princeton.edu/research/techreps/TR-554-97)中有这样的总结：

> Regular expressions describe lexical structures  of programming languages.
>
> Context free grammars describe syntactic structures of programming languages .
>
> ASDL describes the [abstract syntax](https://en.wikipedia.org/wiki/Abstract_syntax)  of compiler intermediate representations (IRs) and other tree-like data
> structures.

### [Algebraic data types](https://en.wikipedia.org/wiki/Algebraic_data_type)

### see also

在我的工程[data-structure](https://github.com/dengking/data-structure)给出了各种数据结构的描述方式，下面给出链接：

- https://github.com/dengking/data-structure/blob/master/docs/tree/representing-trees.md
- 

## compiler中的描述

在compiler中使用了多种[Intermediate representation](https://en.wikipedia.org/wiki/Intermediate_representation)，这些IR都是对source code的不同的表示/描述。

see also：

- dragon book





## human-readable and machine-readable 

下面这段是我在阅读[The Python Language Specification](https://realpython.com/cpython-source-code-guide/#the-python-language-specification)时遇到的：

> Contained within the CPython source code is the definition of the Python language. This is the reference specification used by all the Python interpreters.
>
> The specification is in both **human-readable** and **machine-readable** format. Inside the documentation is a detailed explanation of the Python language, what is allowed, and how each statement should behave.

它对我的启发是：

- 不同的描述有其相应的的优势
- 在工程中，我们往往需要将一种描述方式转换为另外一种描述方式



# 所有的描述都是语言？

可以认为描述的本质是[**语言**](https://en.wikipedia.org/wiki/Language)。科学需要严谨的、准确的描述方式，所以它使用的语言需要不同于人类说话时使用的[自然语言](https://en.wikipedia.org/wiki/Natural_language)，在科学中，往往使用的一种叫做[formal language](https://en.wikipedia.org/wiki/Well-formed_formula)的语言，这类语言有着诸多优良的特性，它是很多学科的基础。

本章所要研究的就是[formal language](https://en.wikipedia.org/wiki/Well-formed_formula)。

# 描述抽象结构



## ASDL

cpython 使用ASDL来描述自己的AST

https://www.usenix.org/legacy/publications/library/proceedings/dsl97/full_papers/wang/wang.pdf

http://www.oilshell.org/blog/2016/12/11.html

https://stackoverflow.com/questions/8873126/zephyr-asdl-abstract-syntax-description-language

https://devguide.python.org/compiler/

https://github.com/python/cpython/blob/master/Parser/Python.asdl

http://asdl.sourceforge.net/

https://www.cs.princeton.edu/research/techreps/TR-554-97

显然，它也可以作为一种树描述语言。

https://en.wikipedia.org/wiki/Algebraic_data_type

https://en.wikipedia.org/wiki/Abstract_syntax





# 描述的递归性

像CFG就具备递归性，有[recursive grammar](https://en.wikipedia.org/wiki/Recursive_grammar)的概念。关于描述的递归性在[Production(computer-science)](./Formal-grammar/wikipedia-Production(computer-science).md)、[Chomsky-hierarchy](./Formal-grammar/Chomsky-hierarchy/wikipedia-Chomsky-hierarchy.md)中有专门的描述。