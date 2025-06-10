1

单选(2分)

‌以下哪个选项不是Scala的数据类型？

​

得分/总分

- A.
    
    A Byte，Short，Int，Unit
    
- B.
    
    Long，Char，String
    
    0.00/2.00
    
- C.
    
    Float，Double，Boolean
    
- D.
    
    Integer，Void
    

正确答案：D你错选为B

2

单选(2分)

‌下面输出与其他不一致的是？

​

得分/总分

- A.
    
    print("Hello World\n")
    
- B.
    
    printf("Hello %s", "World\n")
    
- C.
    
    println("Hello World")
    
- D.
    
    val w = "World" ; println("Hello $w")
    

正确答案：D你没选择任何选项

3

单选(2分)

‌关于元组 Tuple 说法错误的是？

‍

得分/总分

- A.
    
    元组是不可变的
    
- B.
    
    访问元组tuple第一个元素的方式为tuple._1
    
- C.
    
    元组可以包含不同类型的元素
    
- D.
    
    元组最多只有2个元素
    

正确答案：D你没选择任何选项

4

单选(2分)

‍有关操作符优先级的描述不正确的是？

‏

得分/总分

- A.
    
    %的优先级高于+
    
- B.
    
    +的优先级高于！
    
- C.
    
    >的优先级高于&
    
- D.
    
    *=的优先级低于+
    

正确答案：B你没选择任何选项

5

单选(2分)

‍对集合(Set)进行操作"Set(2, 0, 1) + 1 + 1 - 1"之后的结果为？

‌

得分/总分

- A.
    
    以上均不正确
    
- B.
    
    Set(2, 0)
    
- C.
    
    Set(2, 0, 1, 1)
    
- D.
    
    Set(2, 0, 1)
    

正确答案：B你没选择任何选项

6

单选(2分)

‎Scala中，类成员的缺省访问级别是？

‎

得分/总分

- A.
    
    以上都不对
    
- B.
    
    public
    
- C.
    
    protected
    
- D.
    
    private
    

正确答案：B你没选择任何选项

7

单选(2分)

‏以下关于闭包描述错误的是？

‌

得分/总分

- A.
    
    闭包是一个函数，其返回值依赖于声明在函数包部的一个或多个变量
    
- B.
    
    对于def mulBy(factor: Double) = (x: Double) => factor * x; val triple = mulBy(3);,函数triple是一个闭包
    
- C.
    
    对于def mulBy(factor: Double) = (x: Double) => 3 * x; val triple = mulBy(3);,函数triple是一个闭包
    
- D.
    
    通常来讲，可以将闭包看作是可以访问一个函数里面局部变量的另一个函数
    

正确答案：C你没选择任何选项

8

单选(2分)

​高阶函数是指？

‏

得分/总分

- A.
    
    将函数作为参数，并返回结果为函数的函数
    
- B.
    
    函数参数为函数或返回结果为函数的函数
    
- C.
    
    执行时间长的函数
    
- D.
    
    在程序中应该首先被定义的函数
    

正确答案：B你没选择任何选项

9

单选(2分)

‍对于Map("book" -> 5, "pen" -> 2).map(m => m._1 -> m._2 * 2)的结果，下面哪个是正确的？

‎

得分/总分

- A.
    
    Map("book" -> 5, "pen" -> 2 ,"book" -> 5, "pen" -> 2)
    
- B.
    
    Map("bookbook" -> 10, "penpen" -> 4)
    
- C.
    
    Map("bookbook" -> 5, "penpen" -> 2)
    
- D.
    
    Map("book" -> 10, "pen" -> 4)
    

正确答案：D你没选择任何选项

10

单选(2分)

​以下单例对象，定义错误的是？

‏

得分/总分

- A.
    
    object Person{var PID = “”}
    
- B.
    
    object Person{def PID = “”}
    
- C.
    
    object Person(PID:String){ }
    
- D.
    
    object PersonA{val PID = “”}
    

正确答案：C你没选择任何选项

11

多选(3分)

‎以下哪些选项属于Scala的基本特性?

‎

得分/总分

- [ ] 
    
    A.
    
    是一门纯粹的面向对象的语言
    
- [ ] 
    
    B.
    
    是一门类Java的多范式语言
    
- [ ] 
    
    C.
    
    是一门函数式语言，支持高阶函数，允许嵌套多层函数，并支持柯里化（Currying）
    
- [ ] 
    
    D.
    
    运行于Java虚拟机（JVM）之上，并且兼容现有的Java程序
    

正确答案：A、B、C、D你没选择任何选项

12

多选(3分)

​关于主构造器，以下说法正确的是？

​

得分/总分

- [ ] 
    
    A.
    
    主构造器的参数可以直接放在类名后
    
- [ ] 
    
    B.
    
    主构造器在每个类都可以定义多个
    
- [ ] 
    
    C.
    
    主构造器中可以使用默认参数
    
- [ ] 
    
    D.
    
    主构造器会执行类定义中的所有语句
    

正确答案：A、C、D你没选择任何选项

13

多选(3分)

‍Scala中，关于包的引用正确的是？

‎

得分/总分

- [ ] 
    
    A.
    
    包和其成员可以用import
    
- [ ] 
    
    B.
    
    包引用只能在编译单元的开始处
    
- [ ] 
    
    C.
    
    可以引用某个文件夹下的特定文件
    
- [ ] 
    
    D.
    
    可以引用某个文件夹下的所有文件
    

正确答案：A、C、D你没选择任何选项

14

多选(3分)

‎以下关于特质的说法正确的是？

​

得分/总分

- [ ] 
    
    A.
    
    特质可以要求实现它们的类具备特定的字段、方法或超类
    
- [ ] 
    
    B.
    
    当将多个特质叠加在一起时，顺序很重要，其方法先被执行的特质排在更后面
    
- [ ] 
    
    C.
    
    与Java接口(Interface)相同，Scala特质不可以提供方法和字段的实现
    
- [ ] 
    
    D.
    
    类可以实现任意数量的特质
    

正确答案：A、B、D你没选择任何选项

15

多选(3分)

‌对于元组val t = (1, 3.14, "Fred")说法正确的是？

‏

得分/总分

- [ ] 
    
    A.
    
    t._0无法访问，会抛出异常
    
- [ ] 
    
    B.
    
    val (first, second, _) = t // second 等于 3.14
    
- [ ] 
    
    C.
    
    t_1 等于 1
    
- [ ] 
    
    D.
    
    t 的类型为 Tuple3[Int, Double, java.lang.String]
    

正确答案：A、B、D你没选择任何选项

16

多选(3分)

‍Scala语言中，下面描述正确的是？

​

得分/总分

- [ ] 
    
    A.
    
    Scala中，Float是AnyVal的子类
    
- [ ] 
    
    B.
    
    Scala中，Double是AnyRef的子类
    
- [ ] 
    
    C.
    
    Scala中，Int是Long的子类
    
- [ ] 
    
    D.
    
    Scala中，Long是AnyVal的子类
    

正确答案：A、D你没选择任何选项

17

多选(3分)

‌Scala 中，类和它的伴生对象说法正确的是？

​

得分/总分

- [ ] 
    
    A.
    
    类和它的伴生对象可以互相访问私有特性
    
- [ ] 
    
    B.
    
    类和它的伴生对象定义在同一个文件中
    
- [ ] 
    
    C.
    
    类和它的伴生对象可以有不同的名称
    
- [ ] 
    
    D.
    
    类有静态方法，伴生对象没有静态方法
    

正确答案：A、B你没选择任何选项

18

多选(3分)

‍关于数组val a = Array(1,2,3)下列说法正确的是？

‍

得分/总分

- [ ] 
    
    A.
    
    val b = a.map(_*2) // b 等于 Array(2,4,6)
    
- [ ] 
    
    B.
    
    val b = for(elem <- a if elem % 2 == 0) yield 2 * elem // b 等于 Array(4)
    
- [ ] 
    
    C.
    
    val b = for(elem <- a) yield 2 * elem // b 等于 Array(2,4,6)
    
- [ ] 
    
    D.
    
    val b = 2 * a // b 等于 Array(2,4,6)
    

正确答案：A、B、C你没选择任何选项

19

多选(3分)

‎关于Scala的类层级结构，以下说法正确的是 ？

‌

得分/总分

- [ ] 
    
    A.
    
    null可以赋值给Char类型的变量
    
- [ ] 
    
    B.
    
    Null是所有引用类型的子类
    
- [ ] 
    
    C.
    
    AnyVal是所有值类型的父类
    
- [ ] 
    
    D.
    
    Nothing是所有其他类型的子类
    

正确答案：B、C、D你没选择任何选项

20

多选(3分)

‎在Scala中，关于Nothing，null，Null，Option，Some，None的说法正确的是？

​

得分/总分

- [ ] 
    
    A.
    
    Null是所有引用类型的子类，其唯一的实例是null
    
- [ ] 
    
    B.
    
    Nothing 是所有其他类型的子类，没有实例，主要用于异常处理函数的返回类型
    
- [ ] 
    
    C.
    
    null表示一个空对象，可以赋值给任何引用类型
    
- [ ] 
    
    D.
    
    类Option是一个抽象类，有一个具体子类Some 和一个对象None，分别表示有值和无值的情况
    

正确答案：A、B、C、D你没选择任何选项