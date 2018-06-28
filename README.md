# Spring-Cloud-Microservice
Java : 1.8+   
Spring Boot : 2.0.3.RELEASE   
Spring Cloud : Finchley.RELEASE     


# Using Components

服务注册发现：Eureka Server,Eureka Client    
服务消费负载均衡：Ribbon、Feign   
服务容错保护（降级、隔离、熔断）：Hystrix、Hystrix-Dashboard      
服务容网关：Zuul    

# Use       
1，启动eureka-server 服务注册中心，http://localhost:9000      
2，启动user-service 服务，http://localhost:9100,http://localhost:9101     
&emsp; 启动两个服务，用于测试负载均衡功能，启动命令：  
```jshelllanguage
java -jar user-service-0.0.1-SNAPSHOT.jar --server.port=9100     
java -jar user-service-0.0.1-SNAPSHOT.jar --server.port=9101  
```
3，启动eureka-ribbon 服务负载均衡，http://localhost:9200        
4，启动eureka-feign 服务负载均衡，http://localhost:9210       
5，启动eureka-feign-hystrix 服务容错降级，http://localhost:9220   
6，启动hystrix-dashboard 服务容错仪表盘监控，http://localhost:9230   
&emsp;&ensp;在hystrix-dashboard 界面输入 http://localhost:9220/actuator/hystrix.stream 监控服务        
      
          

