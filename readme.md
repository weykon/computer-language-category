从OOP中获取了更直观的理解方式，但是在隐含的细节和具体的逻辑中，我们也容易迷失了方向。

# 从协变到逆变开始

许多编程语言的类型系统支持子类型。例如，如果类型 Cat 是类型 Animal 的子类型，那么类型 Cat 的表达式应该可以替代任何类型 Animal 的表达式使用。

变异性表明了更复杂类型之间的子类型与它们组成部分之间的子类型之间的关系。例如，一个包含 Cat 的列表应该如何与一个包含 Animal 的列表相关联？或者，一个返回 Cat 的函数应该如何与一个返回 Animal 的函数相关联？

根据类型构造函数的变异性，简单类型的子类型关系对于相应的复杂类型可能是保留、反转或忽略。例如，在 OCaml 编程语言中，“listofCat” 是 “listofAnimal” 的子类型，因为这种类型构造函数是协变的。这意味着简单类型的子类型关系对于复杂类型是被保留的。

另一方面，“从动物到字符串的函数”是“从猫到字符串的函数”的子类型，因为函数类型构造函数在参数类型上是逆变。在这里，简单类型的子类型关系在复杂类型中是相反的。

[函数式中范畴论和Functor](https://zmxiaodao.com/post/tech/fp/functor/)
这个文章可以很好地解释到了Functor指的是什么。

假设目前的两个范畴A和B，他们之间的内部，也可以跨范畴去转换的时候，那么这个过程就描述为Functor的存在。