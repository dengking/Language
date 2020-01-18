# 如何来进行描述？

各种学科，在进行研究的时候，往往是使用简洁的[公式](https://en.wikipedia.org/wiki/Well-formed_formula)（表达式）来**描述**/**表达**/**说明**复杂的问题，比如数学中的[表达式](https://en.wikipedia.org/wiki/Expression_(mathematics))。公式（表达式）其实是一种[抽象](https://en.wikipedia.org/wiki/Abstraction)，抽象的过程对于任何学科都是至关重要的，因为抽象的过程是对本质的靠近的过程。那我们进行科学研究的时候，使用什么来进行描述呢？

在不同的领域，有不同的描述方式，比如：

- 数学中的表达式（[expression](https://en.wikipedia.org/wiki/Expression_(mathematics))）

- 计算机科学中的[programming language](https://en.wikipedia.org/wiki/Programming_language)

上述两种**描述**本质上来说是一种[**语言**](https://en.wikipedia.org/wiki/Language)。科学需要具备严谨性、准确的表达方式，所以它使用的语言需要不同于人类说话时使用的[自然语言](https://en.wikipedia.org/wiki/Natural_language)，在科学中，往往使用的一种叫做[formal language](https://en.wikipedia.org/wiki/Well-formed_formula)的语言，这类语言有着诸多优良的特性，它是很多学科的基础。

## 语言学中的描述方式

在语言学中，通常使用[grammar](https://en.wikipedia.org/wiki/Grammar)来描述语言的结构，[formal language](https://en.wikipedia.org/wiki/Well-formed_formula)的grammar是[formal grammar](https://en.wikipedia.org/wiki/Formal_grammar)，比如[context free grammar](https://en.wikipedia.org/wiki/Context-free_grammar)。formal grammar常常采用的描述方式是产生式（[production](https://en.wikipedia.org/wiki/Production_(computer_science))），那production这种描述方式是语言吗？显然它是一种语言，因为它有固定的语法、语义。

## compiler的描述方式

在compiler中使用了多种[Intermediate representation](https://en.wikipedia.org/wiki/Intermediate_representation)

# [Formal system](https://en.wikipedia.org/wiki/Formal_system) and [formal language](https://en.wikipedia.org/wiki/Formal_language)

[Formal system](https://en.wikipedia.org/wiki/Formal_system)这篇文章向我们揭示了提供[formal language](https://en.wikipedia.org/wiki/Formal_language)，我们能够构建一套系统，这是我们使用[formal language](https://en.wikipedia.org/wiki/Formal_language)的终极目标所在。





# 所有的描述都是语言？



那能否说：所有的描述都是语言？



在计算机科学中，对于语言（描述）的研究是非常重要的， 简单语言能够带来巨大的好处。

有的语言是general purpose的，如

- python
- c

有些则是special-purpose的，如

- [Zephyr  ASDL](https://www.cs.princeton.edu/research/techreps/TR-554-97)
- [Interface description language](https://en.wikipedia.org/wiki/Interface_description_language)
- [Data modeling languages](https://en.wikipedia.org/wiki/Category:Data_modeling_languages)。







# 产生式

## 产生式VS推导式

TODO: 从[Formation rule](https://en.wikipedia.org/wiki/Formation_rule)的角度来看待production，则它是一种推导。

如果从推导的角度来看待产生式的话，则关于自顶向下parsing无法处理左递归的情况就非常任意理解了。这个需要尽快地补充。

## 递归公式VS产生式

数学中的递归公式（[recurrence relation](https://en.wikipedia.org/wiki/Recurrence_relation)），语言学中的产生式，两者其实有着共同之处：递归。

production可以用来描述所有的具有hierarchy结构的数据，这样的结构是允许具备递归性的。这种hierarchy结构对应着一棵树。

> NOTE: formal grammar是描述具有hierarchy structure的一个非常好的工具

递归公式则描述了问题求解过程的递归性，它并不是像产生式那样描述的是具体实际的结构。但是，如果从计算机程序实现递归公式的角度来看，由于计算机执行过程中使用的是stack，每次函数调用都会new一个栈帧对象，通过以适当的方式将栈帧给摆放起来的话，可以对应一棵树。

从本质上来说，program是对各种描述的计算机实现。





# 描述抽象结构

在论文[The Zephyr Abstract Syntax Description Language](https://www.cs.princeton.edu/research/techreps/TR-554-97)中有这样的总结：

Regular expressions describe lexical structures  of programming languages.

Context free grammars describe syntactic structures of programming languages .

ASDL describes the [abstract syntax](https://en.wikipedia.org/wiki/Abstract_syntax)  of compiler intermediate representations (IRs) and other tree-like data
structures.

[Algebraic data types](https://en.wikipedia.org/wiki/Algebraic_data_type)

## ASDL

## python ASDL

python使用ASDL来描述自己的AST

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



# 描述描述的描述

meta的概念，现在想想meta的概念其实是存在递归性质的

描述CFG的描述的相关文章：https://en.wikipedia.org/wiki/Metasyntax





# [The Python Language Specification](https://realpython.com/cpython-source-code-guide/#the-python-language-specification)

> Contained within the CPython source code is the definition of the Python language. This is the reference specification used by all the Python interpreters.
>
> The specification is in both **human-readable** and **machine-readable** format. Inside the documentation is a detailed explanation of the Python language, what is allowed, and how each statement should behave.

不同的描述有不同的优势。