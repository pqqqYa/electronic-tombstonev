##### 1 [单选]  
以下哪个选项不是Scala的数据类型？  
A. Byte, Short, Int, Unit  
B. Long, Char, String  
C. Float, Double, Boolean  
D. Integer, Void  
答案：D  

##### 2 [单选]  
下面输出与其他不一致的是？  
A. print("Hello World\n")  
B. printf("Hello %s", "World\n")  
C. println("Hello World")  
D. val w = "World" ; println("Hello $w")  
答案：D  

##### 3 [单选]  
关于元组 Tuple 说法错误的是？  
A. 元组是不可变的  
B. 访问元组第一个元素的方式为 `tuple._1`  
C. 元组可以包含不同类型的元素  
D. 元组最多只有2个元素  
答案：D  

##### 4 [单选]  
有关操作符优先级的描述不正确的是？  
A. `%`的优先级高于`+`  
B. `+`的优先级高于`!`  
C. `>`的优先级高于`&`  
D. `*=`的优先级低于`+`  
答案：B  

##### 5 [单选]  
对集合(Set)进行操作 `Set(2, 0, 1) + 1 + 1 - 1` 之后的结果为？  
A. 以上均不正确  
B. Set(2, 0)  
C. Set(2, 0, 1, 1)  
D. Set(2, 0, 1)  
答案：B  

##### 6 [单选]  
Scala中，类成员的缺省访问级别是？  
A. 以上都不对  
B. public  
C. protected  
D. private  
答案：B  

##### 7 [单选]  
以下关于闭包描述错误的是？  
A. 闭包是一个函数，其返回值依赖于声明在函数外部的一个或多个变量  
B. 对于 `def mulBy(factor: Double) = (x: Double) => factor * x; val triple = mulBy(3)`，函数 triple 是一个闭包  
C. 对于 `def mulBy(factor: Double) = (x: Double) => 3 * x; val triple = mulBy(3)`，函数 triple 是一个闭包  
D. 通常可以将闭包看作是可以访问一个函数里面局部变量的另一个函数  
答案：C  

##### 8 [单选]  
高阶函数是指？  
A. 将函数作为参数，并返回结果为函数的函数  
B. 函数参数为函数或返回结果为函数的函数  
C. 执行时间长的函数  
D. 在程序中应该首先被定义的函数  
答案：B  

##### 9 [单选]  
对于 `Map("book" -> 5, "pen" -> 2).map(m => m._1 -> m._2 * 2)` 的结果，下面哪个正确？  
A. Map("book"->5, "pen"->2, "book"->5, "pen"->2)  
B. Map("bookbook"->10, "penpen"->4)  
C. Map("bookbook"->5, "penpen"->2)  
D. Map("book"->10, "pen"->4)  
答案：D  

##### 10 [单选]  
以下单例对象，定义错误的是？  
A. `object Person{var PID = ""}`  
B. `object Person{def PID = ""}`  
C. `object Person(PID:String){ }`  
D. `object PersonA{val PID = ""}`  
答案：C  

##### 11 [多选]  
以下哪些选项属于Scala的基本特性？  
A. 是一门纯粹的面向对象的语言  
B. 是一门类Java的多范式语言  
C. 是一门函数式语言，支持高阶函数、嵌套函数和柯里化  
D. 运行于JVM之上，兼容现有Java程序  
答案：A、B、C、D  

##### 12 [多选]  
关于主构造器，以下说法正确的是？  
A. 主构造器的参数可直接放在类名后  
B. 主构造器在每个类可以定义多个  
C. 主构造器中可使用默认参数  
D. 主构造器会执行类定义中的所有语句  
答案：A、C、D  

##### 13 [多选]  
Scala中，关于包的引用正确的是？  
A. 包和其成员可以用 `import`  
B. 包引用只能在编译单元的开始处  
C. 可以引用某个文件夹下的特定文件  
D. 可以引用某个文件夹下的所有文件  
答案：A、C、D  

##### 14 [多选]  
以下关于特质的说法正确的是？  
A. 特质可要求实现类具备特定字段、方法或超类  
B. 叠加多个特质时，顺序很重要（后叠加的特质先执行）  
C. 与Java接口相同，Scala特质不可提供方法和字段实现  
D. 类可实现任意数量的特质  
答案：A、B、D  

##### 15 [多选]  
对于元组 `val t = (1, 3.14, "Fred")` 说法正确的是？  
A. `t._0` 无法访问，会抛出异常  
B. `val (first, second, _) = t` 中 `second` 等于 3.14  
C. `t_1` 等于 1  
D. `t` 的类型为 `Tuple3[Int, Double, java.lang.String]`  
答案：A、B、D  

##### 16 [多选]  
Scala中，下面描述正确的是？  
A. `Float` 是 `AnyVal` 的子类  
B. `Double` 是 `AnyRef` 的子类  
C. `Int` 是 `Long` 的子类  
D. `Long` 是 `AnyVal` 的子类  
答案：A、D  

##### 17 [多选]  
Scala中，类和它的伴生对象说法正确的是？  
A. 类和伴生对象可互相访问私有特性  
B. 类和伴生对象需定义在同一文件中  
C. 类和伴生对象可以有不同的名称  
D. 类有静态方法，伴生对象没有静态方法  
答案：A、B  

##### 18 [多选]  
关于数组 `val a = Array(1,2,3)` 说法正确的是？  
A. `val b = a.map(_*2)` 结果为 `Array(2,4,6)`  
B. `val b = for(elem <- a if elem%2==0) yield 2*elem` 结果为 `Array(4)`  
C. `val b = for(elem <- a) yield 2*elem` 结果为 `Array(2,4,6)`  
D. `val b = 2*a` 结果为 `Array(2,4,6)`  
答案：A、B、C  

##### 19 [多选]  
关于Scala的类层级结构，以下说法正确的是？  
A. `null` 可以赋值给 `Char` 类型变量  
B. `Null` 是所有引用类型的子类  
C. `AnyVal` 是所有值类型的父类  
D. `Nothing` 是所有其他类型的子类  
答案：B、C、D  

##### 20 [多选]  
关于 `Nothing`, `null`, `Null`, `Option`, `Some`, `None` 说法正确的是？  
A. `Null` 是所有引用类型的子类，唯一实例是 `null`  
B. `Nothing` 是所有类型的子类，无实例，用于异常处理返回类型  
C. `null` 可赋值给任何引用类型  
D. `Option` 是抽象类，有子类 `Some`（有值）和对象 `None`（无值）  
答案：A、B、C、D  