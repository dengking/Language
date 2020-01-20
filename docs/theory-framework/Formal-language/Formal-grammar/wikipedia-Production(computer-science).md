[TOC]

# [Production (computer science)](https://en.wikipedia.org/wiki/Production_(computer_science))



production是否是



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