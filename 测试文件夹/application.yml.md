~~~yml
server:  
  port: 8089  
  servlet:  
    context-path: /  
  
spring:  
  datasource:  
    driver-class-name: com.mysql.cj.jdbc.Driver  
    url: jdbc:mysql://localhost:3306/test?characterEncoding=UTF-8&serverTimezone=GMT%2B8  
    username: root  
    password: 123123  
    type: com.alibaba.druid.pool.DruidDataSource  
  
  
mybatis:  
  mapper-locations: classpath:mapper/*.xml  
  #  打印sql语句  
  configuration:  
    log-impl: org.apache.ibatis.logging.stdout.StdOutImpl
~~~~