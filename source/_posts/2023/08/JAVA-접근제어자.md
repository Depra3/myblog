---
title: JAVA - 접근제어자
date: 2023/08/07 19:40:00
categories:
- JAVA
tags:
- 개념
- 객체 지향 프로그래밍
- 접근 제어자
- 접근 제한자
- public
- protected
- default
- private
---

# 접근제어자

- **클래스 or 클래스 멤버(필드, 메소드 생성자)를 사용할 때, 접근할 수 있는 범위를 지정**하는 역할
- **생략이 가능하며, 생략할 때는 자동적으로 default로 설정**된다.

# 특징

- **접근을 제어하여 외부에 의한 접근으로부터 데이터를 보호**한다.
- **객체지향 프로그래밍**에서 **캡슐화하기 위한 기능으로 사용**된다.
---
# 종류

## public

- **접근 제한이 없어 모든 접근이 가능**
- **클래스, 클래스 멤버 모두 사용**
#
- **예시**
    
    ```java
    public class Test(){        // 클래스
    	public int a;       // 클래스 멤버
    	public String b;
    }
    ```
    
---
## protected

- **같은 패키지 내의 모든 클래스, 다른 패키지의 자식 클래스에서 접근 가능**
- **클래스 멤버만 사용**
#
- **예시**
    
    ```java
    public class Test(){        // 클래스
    	protected int a;    // 클래스 멤버
    	protected String b;
    }
    ```
    
---
## default

- **같은 패키지 내에서만 접근 가능**
- **클래스, 클래스 멤버 모두 생략해서 사용**
#
- **예시**
    
    ```java
    class Test(){        // 클래스
    	int a;       // 클래스 멤버
    	String b;
    }
    ```
    
---
## private

- **같은 클래스 내에서만 접근 가능**
- **클래스 멤버만 사용**
#
- **예시**
    
    ```java
    public class Test(){        // 클래스
    	private int a;      // 클래스 멤버
    	private String b;
    }
    ```
    
---
# 접근 범위

- **접근 범위 : public > protected > default > private**

![](/Images/2023/08/JAVA-접근제어자/Untitled.png)