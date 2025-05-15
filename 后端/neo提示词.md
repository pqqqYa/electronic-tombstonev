**pojo的创建**


~~~txt
根据sql文件帮我在pojo文件夹下创建`order`和`product`类 *(替换为表的名字)*，注意属性名和列名需要保持完全一致
~~~
  

**mapperxml创建**
~~~txt
这是一个Springboot+Mybatis构建的购物商城软件
1. 实现用户的登录、注册、信息更新、信息查询
2. 实现商品的增加，删除，修改信息
3. 实现购物车增加，删除，即订单的增删改查
我在这里有一些没有提到的功能，你分析我的描述，帮我适当添加一些合理的功能
 
pojo类已存在src/main/java/com/swpu/zhuhaowei/pojo|
根据sql文件在src/main/resources/mapper中书写xml文件，如UserMapper.xml。

满足软件对数据库操作的需要。
1. 严格按照sql文件中的列名进行编写
2. 使用<where> 和<if>动态标签支持按条件查询
3. 添加尽量详细的注释
4. 注意代码编写的规范性
~~~