---
title: Reflection
categories: [dev]
comments: true
---

# 리플렉션 / Reflection API

힙 영역에 로드되어있는 클래스 타입의 객체를 통해 필드/메소드/생성자를 접근제어자와 상관 없이 사용할 수 있도록 지원하는 api
   
      
## 클래스 타입을 사용하는 법

```java
1) 
Class<User> class = User.class;

2)
User user = new User();
Class<? extends User> class = user.getClass(); 

3)
Class<?> class = Class.forName("org.example.model.User");


```

## 실전 사용법

```java
@Controller, @Service 를 사용하는 모든 클래스 찾기

private Set<Class<?>> getAnnotationType(List<Class<? extends Annotation>> annotations){   
    Reflection reflection = new Reflection("org.example");   

    Set<Class<?>> beans = new HashSet<>();
    annotations.forEach(annotation -> beans.addAll(reflection.getTypesAnnotationWith(annotation)));

    return beans;
} 



```


