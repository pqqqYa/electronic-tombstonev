## 第1章 大数据技术概述
##### 1 电子商务网站购物平台数据的实时分析处理属于哪种计算模式？
A. 查询分析计算  
B. 批处理计算  
C. 图计算  
D. 流计算  
答案：D  

##### 2 Hadoop生态系统中用于构建数据仓库并支持SQL查询的组件是？
A. Spark  
B. Pregel  
C. Flume  
D. Hive  
答案：D  

##### 3 MapReduce的基本设计思想是？
A. 计算向数据靠拢  
B. 提高数据的串行计算速度  
C. 提高数据的冗余度  
D. 数据向计算靠拢  
答案：A  

##### 4 以下哪项不是Hadoop的缺点？
A. 计算延迟高  
B. 数据文件被分布存储到多台机器上  
C. 磁盘I/O开销大  
D. 计算表达能力有限  
答案：B  

##### 5 HDFS的正确访问方式是？
A. 直接通过名称节点获取数据  
B. 通过名称节点查找数据块位置后从数据节点获取  
C. 以上都不对  
D. 直接通过数据节点获取数据  
答案：B  

##### 6 大数据处理的四个基本步骤是？
A. 数据安全和隐私保护  
B. 处理分析  
C. 数据采集  
D. 存储管理  
答案：B、C、D  

##### 7 大数据的四个公认特点是？
A. 价值密度低  
B. 数据类型多  
C. 数据可重复使用  
D. 处理速度快  
答案：A、B、D  

##### 8 YARN框架的优点包括？
A. 共享底层存储  
B. 降低运维成本  
C. 不同负载应用混搭  
D. 计算资源按需伸缩  
答案：A、B、C、D  

##### 9 Spark生态系统支持的计算包括？
A. 机器学习（MLlib）  
B. 图计算（GraphX）  
C. SQL即席查询（Spark SQL）  
D. 流式计算（Spark Streaming）  
答案：A、B、C、D  

##### 10 Flink在流式处理中的特点有？
A. 支持毫秒级响应  
B. 只能支持秒级响应  
C. 逐行处理数据  
D. 支持增量迭代优化  
答案：A、C、D  

##### 11 Pregel主要应用于哪种计算模式？
A. 图计算  
B. 流计算  
C. 批处理计算  
D. 查询分析计算  
答案：A  

##### 12 YARN的主要功能是？
A. 数据仓库工具  
B. 分布式并行编程模型  
C. 集群资源调度管理  
D. 日志采集传输系统  
答案：C  

##### 13 大型图分布式计算最适合的框架是？
A. Pregel  
B. Storm  
C. Spark Core  
D. Dremel  
答案：A  

##### 14 Hadoop两大核心组成部分是？
A. YARN  
B. HDFS  
C. MapReduce  
D. Zookeeper  
答案：B、C  

##### 15 Spark相比Hadoop的优点包括？
A. 内存计算提高迭代效率  
B. 支持多种数据集操作  
C. 基于DAG的任务调度  
D. 数据集中式计算更高效  
答案：A、B、C  

##### 16 大数据技术及其代表性的软件种类很多，不同的技术有其不同应用场景，都对应着不同的大数据计算模式，请问软件产品Pregel主要应用于以下哪种计算模式？

A. 查询分析计算  
B. 批处理计算  
C. 图计算  
D. 流计算  

答案：C

##### 17 经过多年的发展，Hadoop生态系统不断完善和成熟，目前已经包含多个子项目，其中YARN的主要功能是?

A. 分布式海量日志采集、聚合和传输系统
B. 负责集群资源调度管理的组件
C. 分布式并行编程模型
D. 数据仓库工具

答案：B

##### 18  MapReduce的一个基本设计思想是？

A.数据向计算靠拢
B.提高数据的串行计算速度
c.计算向数据靠拢
D.提高数据的冗余度

答案：C

##### 19 用户在使用HDFS时，仍然可以像普通文件系统那样用文件名去访问文件，以下哪个选项是正确的访问方式？

A. 把文件名发送给数据节点，根据文件名直接在数据节点上获取数据
B. 把文件名发送给名称节点，根据文件名直接在名称节点上获取数据
C.把文件名发送给名称节点，根据文件名在名称节点上找到数据块的实际存储信息，客户端再到数据节点上获取数据
D. 以上说法都不对

答案：C

##### 20 Hadoop两大核心组成部分是什么？

A.资源调度管理框架YARN
B.分布式协作服务Zookeeper
C.分布式文件系统HDFS
D.分布式计算框架MapReduce

答案：C、D

##### 21 YARN是负责集群资源调度管理的组件。不同的计算框架统一运行在YARN框架之上，具有哪些优点:

A. 不同负载应用混搭，集群利用率高
B. 计算资源按需伸缩
C. 共享底层存储，避免数据跨集群迁移
D. 大大降低了运维成本

答案：A、B、C、D

##### 22 关于Hadoop生态系统中HBase与其它部分的关系，以下说法正确的有

A. HBase利用MapReduce来处理HBase中的海量数据，实现高性能计算
B. 使用HDFS作为高可靠的底层存储，利用廉价集群提供海量数据存储能力
C. 利用Zookeeper作为协同服务，实现稳定服务和失败恢复
D. 使用Sqoop为HBase提供了高效便捷的RDBMS数据导入功能

答案：A、B、C、D

##### 23 Spark的设计遵循“一个软件栈满足不同应用场景”的理念，逐渐形成了一套完整的生态系统，可以支持以下哪些操作计算：

A. 图计算(GraphX)
B. SQL即席查询 (Spark SQL)
C. 机器学习(MLlib)
D. 流式计算(Spark Streaming)

答案：A、B、C、D
##### 24 ‍Flink和Spark一样，都是基于内存的计算框架，都支持流计算，在流式处理方面，以下选项是Flink的主要特点的有:

A.Flink支持增量选代，具有对迭代进行自动优化的功能
B.Flink是一行一行地处理数据
C.Flink只能支持秒级的响应
D. Flink可以支持毫秒级的响应

答案：A、B、D

##### ​Hadoop的生态系统组件之一Sqoop的功能是?




## 第2章 Scala语言基础
##### 1 关于操作符优先级描述不正确的是？
A. %的优先级高于+  
B. \*=的优先级低于+  
C. +的优先级高于！  
D. >的优先级高于&  
答案：C  

##### 2 引用sqrt函数的错误方式是？
A. import sqrt  
B. import scala.math._  
C. import math._  
D. import math.sqrt  
答案：A  

##### 3 关于辅助构造器正确的是？
A. 必须调用主构造器  
B. 可直接调用超类主构造器  
C. 名称和类名相同  
D. 参数可以是任意多个  
答案：D  

##### 4 关于闭包描述错误的是？
A. 可访问函数局部变量的另一个函数  
B. triple = mulBy(3)是闭包（factor参与计算）  
C. triple = mulBy(3)是闭包（固定乘3）  
D. 返回值依赖外部变量的函数  
答案：C  

##### 5 Map("book"->5,"pen"->2).map(m=>m.\_1->m.\_2 * 2)结果是？
A. Map("bookbook"->10, "penpen"->4)  
B. 原Map重复拼接  
C. Map("bookbook"->5, "penpen"->2)  
D. Map("book"->10, "pen"->4)  
答案：D  

##### 6 错误的单例对象定义是？
A. object Person{var PID=""}  
B. object Person{def PID=""}  
C. object Person(PID:String){}  
D. object PersonA{val PID=""}  
答案：C  

##### 7 for循环输出结果正确的是？
A. 12 13 21 23 31 32  
B. 11 12 21 22 31 32  
C. 11 13 21 23 31 33  
D. 所有两位数组合  
答案：A  

##### 8 breakable代码段输出结果是？
Array(2,6,10,5,4)中>5时break  
A. 10,5,4  
B. 2,5,4  
C. 6,10,5  
D. 2,6,4  
答案：B  

##### 9 Counter类的value字段默认方法？
A. value, value_  
B. getter, setter  
C. value, value_=  
D. getValue, setValue  
答案：C  

##### 10 递归函数pw(5)的结果是？
def pw(x:Int):Int = if(x\==0)1 else 2\*pw(x-1)  
A. 15  
B. 120  
C. 16  
D. 32  
答案：D  

##### 11 Scala基本特性包括？
A. 函数式语言支持高阶函数  
B. 类Java多范式语言  
C. 运行于JVM兼容Java  
D. 纯面向对象语言  
答案：A、B、C、D  

##### 12 关于主构造器正确的是？
A. 参数可直接放类名后  
B. 支持默认参数  
C. 可定义多个主构造器  
D. 执行类定义中所有语句  
答案：A、B、D  

##### 13 正确的包引用方式是？
A. 引用特定文件  
B. 只能在编译单元开始处  
C. 引用文件夹下所有文件  
D. 用import引用包成员  
答案：A、C、D  

##### 14 函数作为"头等公民"的表现？
A. 作为返回值  
B. 赋值给变量  
C. 作为参数传递  
D. 以上都不对  
答案：A、B、C  

##### 15 关于特质正确的是？
A. 可要求特定字段/方法  
B. 类可实现任意数量特质  
C. 叠加顺序影响执行  
D. 不能提供方法实现（错误）  
答案：A、B、C  

##### 16 Map操作结果正确的是？
A. prices("sticker")=1  
B. 添加后prices("shoes")=30  
C. prices("sock")会报错  
D. 删除后prices("book")=5  
答案：A、B、D  

##### 17 类和伴生对象关系？
A. 可不同名（错误）  
B. 需在同一文件  
C. 可互访私有成员  
D. 类有静态方法（错误）  
答案：B、C  

##### 18 类层级结构正确的是？
A. null不能赋给Char  
B. Nothing是所有子类  
C. AnyVal是值类型父类  
D. Null是引用类型子类  
答案：B、C、D  

##### 19 数据结构描述正确的是？
A. Set不重复元素  
B. Map键值对中值也唯一（错误）  
C. Iterator顺序访问元素  
D. List不可变  
答案：A、C、D  

##### 20 字符串转大写操作？
books = List("Hadoop","Hive")  
A. books.map(\_.toUpperCase)  
B. books.map(s=>s.toUpperCase)  
C. 错误嵌套循环  
D. for推导式yield转换  
答案：A、B、D  
## 第3章 Spark的设计与运行原理

##### 1 Spark的主要特点包括？
A. 运行速度快  
B. 简洁易用的API设计  
C. 通用完整的技术栈  
D. 支持多种运行模式  
答案：A、B、C、D  

##### 2 Spark运行架构包含哪些组件？
A. 集群资源管理器（Cluster Manager）  
B. 执行进程（Executor）  
C. Worker Node  
D. 任务控制节点Driver Program  
答案：A、B、C、D  

##### 3 关于RDD依赖关系正确的是？
A. 父RDD一个分区→子RDD多个分区=宽依赖  
B. 父RDD多个分区→子RDD一个分区=宽依赖  
C. 父RDD一个分区→子RDD一个分区=窄依赖  
D. 父RDD一个分区→子RDD多个分区=窄依赖（错误）  
答案：A、C  

##### 4 Spark支持的部署方式有？
A. Local本地模式  
B. Standalone独立集群  
C. Spark on Mesos  
D. Spark on YARN  
答案：A、B、C、D  

##### 5 大数据处理典型场景包括？
A. 复杂批量处理  
B. 历史数据交互查询  
C. 大数据分布式计算（非典型分类）  
D. 实时数据流处理  
答案：A、B、D  

##### 6 以下哪个不是Spark组件？
A. Spark Streaming  
B. MLlib  
C. GraphX  
D. Flink（属于其他框架）  
答案：D  

##### 7 RDD不具备的特点是？
A. 可分区  
B. 可序列化  
C. 可修改（RDD不可变）  
D. 可持久化  
答案：C  

##### 8 Task运行在哪个组件上？
A. Driver Program  
B. Spark Master  
C. Worker Node  
D. Cluster Manager  
答案：C  

##### 9 肯定是宽依赖的操作是？
A. map（窄依赖）  
B. filter（窄依赖）  
C. reduceByKey（需shuffle）  
D. union（窄依赖）  
答案：C  

##### 10 Spark的优点包括？
A. 高效容错机制  
B. 利用进程模型（非优点）  
C. 内存持久化中间结果  
D. 表达能力有限（是缺点）  
答案：A、C  

## 第4章 Spark环境搭建和使用方法

##### 1 Spark支持的部署模式包括？
A. Local模式（单机模式）  
B. Standalone模式  
C. YARN模式  
D. Mesos模式  
答案：A、B、C、D  

##### 2 关于Hadoop和Spark的关系正确的是？
A. 可以相互协作  
B. Hadoop负责数据存储管理  
C. Spark负责数据计算  
D. Spark操作HDFS数据需先启动HDFS  
答案：A、B、C、D  

##### 3 检查HDFS是否启动成功的命令是？
A. hdfs  
B. spark  
C. jps  
D. start-dfs  
答案：C  

##### 4 HDFS启动成功后会显示的进程包括？
A. NameNode  
B. HDFS（错误，非进程名）  
C. DataNode  
D. SecondaryNameNode  
答案：A、C、D  

##### 5 spark-shell使用local\[\*]参数表示？
A. 任意数量线程（错误）  
B. 逻辑CPU数量的线程  
C. 逻辑CPU数量的进程（错误）  
D. 单线程（错误）  
答案：B  

##### 6 yarn-client模式特点包括？
A. 提交作业后不能关闭Client  
B. 可关闭Client（错误）  
C. 适合交互式作业  
D. 不适合交互式作业（错误）  
答案：A、C  

##### 7 yarn-cluster模式特点包括？
A. 提交作业后不能关闭Client（错误）  
B. 可关闭Client  
C. 适合交互式作业（错误）  
D. 不适合交互式作业  
答案：B、D  

##### 8 开发Spark独立应用程序的步骤包括？
A. 安装sbt/Maven等工具  
B. 编写应用代码  
C. 编译打包  
D. 通过spark-submit运行  
答案：A、B、C、D  

##### 9 关于Hadoop和Spark的正确描述是？
A. 不能同集群部署（错误）  
B. Hadoop只有存储组件（错误）  
C. 可与Hadoop组合使用  
D. 是竞争关系不能组合（错误）  
答案：C  

##### 10 集群运行Spark应用的步骤包括？
A. 启动Hadoop集群  
B. 启动Spark主从节点  
C. 运行应用JAR包  
D. 查看集群运行信息  
答案：A、B、C、D  

## 第5章 RDD编程
##### 1 RDD求和操作结果
val rdd = sc.parallelize(Array(1,2,3,4,5))
rdd.reduce((a,b)=>a+b)
答案：15

##### 2 groupByKey单词计数结果
words = Array("one","two","two","three","three","three")
执行groupByKey().map(t => (t.\_1, t.\_2.sum))
答案：("one",1),("two",2),("three",3)

##### 3 reduceByKey单词计数结果
同上words数组执行reduceByKey(\_+\_)
答案：("one",1),("two",2),("three",3)

##### 4 keys操作结果
pairRDD = ("Hadoop",1),("Spark",1),("Hive",1),("Spark",1)
执行.keys
答案："Hadoop","Spark","Hive","Spark"

##### 5 values操作结果
同上pairRDD执行.values
答案：1,1,1,1

##### 6 RDD操作类型
A. 行动(Action)
B. 转换(Transformation)
答案：A、B

##### 7 Transformation操作示例
A. first()（Action）
B. reduceByKey(func)
C. filter()
D. count()（Action）
答案：B、C

##### 8 Action操作示例
A. collect()
B. groupByKey()（Transformation）
C. reduce()
D. map()（Transformation）
答案：A、C

##### 9 RDD持久化描述
A. 避免重复计算
B. MEMORY_AND_DISK存储策略
C. MEMORY_ONLY存储策略
D. cache()调用persist(MEMORY_ONLY)
答案：A、B、C、D

##### 10 RDD分区作用
A. 减少通信开销
B. 增加时间开销（错误）
C. 减少并行度（错误）
D. 增加并行度
答案：A、D

##### 11 map转换结果
data = Array(1,2,3,4,5)
执行.map(x=>x+10)
答案：11,12,13,14,15

##### 12 groupByKey复杂示例
words = ("Hadoop",1),("is",1),("good",1),...,("better",1)
执行groupByKey()
答案：("is",(1,1,1)), ("Spark",(1,1))等

##### 13 join操作结果
pairRDD1 = ("spark",1),("spark",2),("hadoop",3),("hadoop",5)
pairRDD2 = ("spark","fast")
执行join
答案：("spark",(1,"fast")), ("spark",(2,"fast"))
## 第6章 Spark SQL

##### 1 关于Shark的正确描述是？
A. 提供类似Pig功能（错误）  
B. 转换SQL为MapReduce作业（错误）  
C. 重用Hive的HiveQL解析和优化逻辑  
D. 性能比Hive差很多（错误）  
答案：C  

##### 2 Spark SQL架构描述错误的是？
A. 重写优化部分解决Shark问题  
B. 仅依赖HiveQL解析和元数据  
C. 由Catalyst负责执行计划优化  
D. 需要依赖Hive完成优化（错误）  
答案：D  

##### 3 正确保存DataFrame为JSON的语句是？
A. df.write.json("people.json")  
B. df.json("people.json")（错误）  
C. 以CSV格式保存为JSON（错误）  
D. 保存为CSV文件（错误）  
答案：A  

##### 4 非DataFrame常用操作的是？
A. printSchema()  
B. select()  
C. filter()  
D. sendto()（不存在）  
答案：D  

##### 5 Shark设计导致的问题包括？
A. 优化完全依赖Hive难以扩展  
B. 优化不依赖Hive（错误）  
C. Spark线程级并行引发线程安全问题  
D. Spark进程级并行（错误）  
答案：A、C  

##### 6 推出Spark SQL的原因包括？
A. 提供DataFrame API整合多数据源  
B. 融合结构化数据管理和机器学习能力  
C. 无法整合数据源（错误）  
D. 无法融合能力（错误）  
答案：A、B  

##### 7 DataFrame的正确描述包括？
A. 使Spark能处理结构化数据  
B. 比RDD更易用且性能更高  
C. 支持MySQL转换和SQL查询  
D. 基于RDD的带结构信息数据集  
答案：A、B、C、D  

##### 8 读取JSON生成DataFrame的命令是？
A. spark.read.json("people.json")  
B. 读取Parquet格式（错误）  
C. spark.read.format("json").load("people.json")  
D. 以CSV格式读取JSON（错误）  
答案：A、C  

##### 9 RDD转DataFrame的方法包括？
A. 利用反射推断模式  
B. 编程方式定义模式  
C. 投影机制（错误）  
D. 互联机制（错误）  
答案：A、B  

##### 10 编程定义RDD模式的步骤包括？
A. 制作表头（StructType）  
B. 制作记录（Row对象）  
C. 制作映射表（错误）  
D. 拼接表头和记录（createDataFrame）  
答案：A、B、D  
## 第7章 Spark Streaming
##### 1 以下哪个流计算框架不是开源的？
A. IBM StreamBase  
B. Twitter Storm  
C. Yahoo! S4  
D. Spark Streaming  
答案：A

##### 2 关于Spark Streaming的错误描述是？
A. 时间片拆分处理数据流  
B. 主要抽象是DStream  
C. 支持多种数据源接入  
D. 数据抽象是DataFrame（错误）  
答案：D

##### 3 Spark Streaming与Storm的比较正确的是？
A. Spark无法毫秒级，Storm可以  
B. Spark可以毫秒级，Storm不能（错误）  
C. 两者都能毫秒级（错误）  
D. 两者都不能毫秒级（错误）  
答案：A

##### 4 错误的编程对象描述是？
A. RDD需要SparkContext  
B. SQL需要SparkSession  
C. Streaming需要StreamingContext  
D. SQL需要StreamingContext（错误）  
答案：D

##### 5 不属于Streaming基本输入源的是？
A. 文件流  
B. 套接字流  
C. RDD队列流  
D. 双向数据流（不存在）  
答案：D

##### 6 流数据的特征包括？
A. 持续快速到达  
B. 多源复杂格式  
C. 海量不持久存储  
D. 无序不完整  
答案：A、B、C、D

##### 7 流计算处理流程的三个阶段是？
A. 实时采集  
B. 实时计算  
C. 汇总分析（错误）  
D. 实时查询服务  
答案：A、B、D

##### 8 日志采集组件包括？
A. Scribe  
B. GraphX（非采集组件）  
C. Flume  
D. MySQL（数据库）  
答案：A、C

##### 9 流处理与传统系统的区别？
A. 实时vs静态数据  
B. 实时结果vs历史结果  
C. 主动推送结果  
D. 处理历史数据（错误）  
答案：A、B、C

##### 10 Streaming编程基本步骤？
A. 创建输入DStream  
B. 定义转换和输出操作  
C. 调用start()启动  
D. awaitTermination()等待结束  
答案：A、B、C、D

##### 11 DStream有状态转换操作包括？
A. update操作（错误）  
B. reduceByKey（无状态）  
C. 滑动窗口操作  
D. updateStateByKey操作  
答案：C、D
## 第8章 Spark MLlib

##### 1 关于机器学习的错误论述是？
A. 机器学习与人工智能无关联（错误）  
B. 强调算法、经验、性能  
C. 应用于推荐系统、语音识别等领域  
D. 是研究人工智能的科学  
答案：A

##### 2 机器学习处理过程的错误描述是？
A. 基于数据构建和评估模型  
B. 达标模型用于测试数据  
C. 不达标则调整算法重建模型  
D. 模型无需评估直接使用（错误）  
答案：D

##### 3 机器学习流水线的错误描述是？
A. 连接多个阶段形成工作流  
B. 需先定义各PipelineStage  
C. 阶段包括转换器和评估器  
D. 流水线本身是转换器（错误）  
答案：D

##### 4 评估器的错误描述是？
A. 是算法或训练方法的抽象  
B. 操作DataFrame生成转换器  
C. 实现transform()方法（错误）  
D. 实现fit()方法生成转换器  
答案：C

##### 5 转换器的错误描述是？
A. 转换DataFrame的算法  
B. 实现fit()方法（错误）  
C. 模型是转换预测标签的转换器  
D. 实现transform()方法  
答案：B

##### 6 正确的论述是？
A. 传统机器学习受限于数据量  
B. MapReduce提升全量数据学习精度  
C. MapReduce高效迭代（错误）  
D. Spark不支持高效迭代（错误）  
答案：A、B

##### 7 Spark MLlib的正确描述是？
A. 1.2+版本分为mllib和ml包  
B. mllib含基于DataFrame的API（错误）  
C. mllib含基于RDD的原始API  
D. ml提供基于RDD的高层API（错误）  
答案：A、C

##### 8 正确的论述是？
A. DataFrame含schema类似二维表  
B. 流水线使用DataFrame存储数据  
C. 转换器转换DataFrame的算法  
D. 评估器转换DataFrame（错误）  
答案：A、B、C