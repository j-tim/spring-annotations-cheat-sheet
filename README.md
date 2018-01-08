# Spring Annotations Cheat Sheet

Quick overview of Spring (and related project) annotations.
This page is written from a Spring developer viewpoint and not all annotations are necessarily
from the Spring Framework or related sub project.

| Annotation                | (Spring) Project           | Description                                                        | Note(s) | Maven                                                              |
|---------------------------|--------------------------|--------------------------------------------------------------------|---------|--------------------------------------------------------------------|
| [@EnableCircuitBreaker](https://github.com/spring-cloud/spring-cloud-commons/blob/master/spring-cloud-commons/src/main/java/org/springframework/cloud/client/circuitbreaker/EnableCircuitBreaker.java)   | Spring Cloud Netflix   | Annotation to enable a CircuitBreaker implementation           | Circuit breaker | [spring-cloud-starter-hystrix](http://www.mvnrepository.com/artifact/org.springframework.cloud/spring-cloud-starter-hystrix)   | 
| [@EnableHystrixDashboard](https://github.com/spring-cloud/spring-cloud-netflix/blob/master/spring-cloud-netflix-hystrix-dashboard/src/main/java/org/springframework/cloud/netflix/hystrix/dashboard/EnableHystrixDashboard.java)   | Spring Cloud Netflix   | Turns a Spring Boot application into a Hystrix dashboard           | Circuit breaker | [spring-cloud-starter-hystrix-dashboard](http://www.mvnrepository.com/artifact/org.springframework.cloud/spring-cloud-starter-hystrix-dashboard)   | 
| [@HystixCommand](https://github.com/Netflix/Hystrix/blob/master/hystrix-contrib/hystrix-javanica/src/main/java/com/netflix/hystrix/contrib/javanica/annotation/HystrixCommand.java)   | Javanica (comes with Spring Cloud Netflix)   | Spring Cloud automatically wraps Spring beans with that annotation in a proxy that is connected to the Hystrix circuit breaker. The circuit breaker calculates when to open and close the circuit, and what to do in case of a failure.                                | Circuit breaker | [spring-cloud-starter-hystrix](http://www.mvnrepository.com/artifact/org.springframework.cloud/spring-cloud-starter-hystrix)   |
| [@HystrixProperty](https://github.com/Netflix/Hystrix/blob/master/hystrix-contrib/hystrix-javanica/src/main/java/com/netflix/hystrix/contrib/javanica/annotation/HystrixProperty.java)   | Javanica (comes with Spring Cloud Netflix)   | One of the `commandProperties` to configure a `@HystixCommand` | Circuit breaker | [spring-cloud-starter-hystrix](http://www.mvnrepository.com/artifact/org.springframework.cloud/spring-cloud-starter-hystrix)   |


