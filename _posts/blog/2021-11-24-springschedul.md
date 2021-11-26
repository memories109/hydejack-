---
title:  "Blog - Socket 통신 개념잡기"
excerpt: "양반향 통신의 Socket에 대해서 알아보겠다."

categories: [Blog, Socket]
tags:
  - Blog
last_modified_at: 2021-11-21T08:07:00-08:00
---


@Scheduled는 Spring 3.1 이상부터 지원합니다.

 

1.Annotation 사용 방법

2.XML 사용 방법

 

이 글에서는 1.Annotation 사용 방법만 다루고 있습니다. 참고 바랍니다.

 

Annotation 설정

 

@Scheduled

 

개념

주기적인 작업이 있을 때 @Scheduled 애노테이션을 사용하면 쉽게 적용할 수 있다.

Linux를 조금 배우신 분들이라면 Linux의 crontab이라고 생각하면 됩니다.

 

 

사용 이유

특정시간 혹은 몇분 혹은 몇시간마다 동작해는 스케쥴러를 구현

주기적인 작업이 필요 할 때

 

문법

먼저 새로운 기술은 항상 그렇듯 XML 설정을 해줘야 한다.

 

새로운 XML를 만들거나 기존에 쓰던 XML에 다음과 같은 문구를 추가 한다.

 

1.새로운 XML를 만들어 추가하는 방법

```xml
<!--?xml version="1.0" encoding="UTF-8"?-->
<beans xmlns="http://www.springframework.org/schema/beans"
             xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
             xmlns:task="http://www.springframework.org/schema/task"
             xsi:schemalocation="
        http://www.springframework.org/schema/beans
        http://www.springframework.org/schema/beans/spring-beans-3.0.xsd
        http://www.springframework.org/schema/task
        http://www.springframework.org/schema/task/spring-task-3.0.xsd">
    <task:annotation-driven>
</task:annotation-driven>
</beans>
 ```

2.기존 XML에 추가하는 방법

```xml
xmlns:task="http://www.springframework.org/schema/task"
 xsi:schemalocation="
 http://www.springframework.org/schema/task
 http://www.springframework.org/schema/task/spring-task-3.0.xsd">
 <task:annotation-driven>
</task:annotation-driven>
```

```java
사용 예시

@Scheduled(fixedDelay=1000)
    public void testScheduler(){
        System.out.println("스케줄링 테스트");
    }
```