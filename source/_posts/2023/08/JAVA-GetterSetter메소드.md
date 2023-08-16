---
title: JAVA - Getter / Setter 메소드
date: 2023/08/16 19:00:00
categories:
- JAVA
tags:
- 개념
- 객체 지향 프로그래밍
- 객체 무결성
- Getter
- Setter
---

# Getter / Setter 메소드

> **객체 지향 프로그래밍에서 캡슐화를 이용해 데이터에 대한 직접적인 접근을 차단한다.**
그 **이유는 객체 무결성을 지키기 위함**이다.
객체에서 음수가 들어가면 안되는 변수에 직접적으로 음수를 넣으면 객체의 무결성이 깨진다.
때문에 **객체의 무결성을 보호하며 데이터를 변경하는 방법인 Getter/Setter 메소드를 사용**한다.
> 

## Getter

- **객체 내부의 멤버 변수에 저장된 값을 외부로 리턴**한다.
- **매개 변수가 없고 리턴이 있다.**
- **메소드명은 get + 변수명으로 사용**한다.
    - **변수명 첫글자는 대문자**로 한다.

## Setter

- **객체 내부의 멤버 변수에 데이터를 전달하여 저장**한다.
- **매개 변수가 있고 리턴이 없다.**
- **메소드명은 set + 변수명으로 사용**한다.
    - **변수명 첫글자는 대문자**로 한다.

# Getter / Setter 메소드 선언
- **예시**
    
    ```java
    private 자료형 변수명;
    
    public 리턴타입 get+변수명() {
    	return 변수명;
    }
    
    public void set+변수명(자료형 변수명) {
    	this.변수명 = 변수명;
    }
    ```
    
- **코드**
    
    ```java
    public class Test {
    	private int a;
    	
    	public int getA() {
    		return a;
    	}
    	
    	public void setA(int a) {
    		this.a = a;
    	}
    }
    
    ------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		Test t1 = new Test();
    		t1.setA(-1);
    		System.out.println(t1.getA());
    	}
    }
    ```
    
- **결과**
    
    ![](/Images/2023/08/JAVA-GetterSetter메소드/Untitled.png)
    

---

# 객체 무결성을 지키는 방법

## 객체 무결성

- **객체가 손상되지 않고 완전성, 정확성, 일관성을 유지하는 특성**
#
- **코드**
    
    ```java
    public class Weight {
    	private int kg;
    	
    	public int getKg() {
    		return kg;
    	}
    	
    	public void setKg(int kg) {
    		if (kg < 0) {
    			this.kg = 0;
    		} else {
    			this.kg = kg;
    		}
    	}
    }
    -----------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		Weight w1 = new Weight();
    		w1.setKg(-10);
    		System.out.println("w1객체의 몸무게의 값 : " + w1.getKg());
    	}
    }
    ```
    
- **결과**
    
    ![](/Images/2023/08/JAVA-GetterSetter메소드/Untitled%201.png)
    
    - **w1.setKg에서 -10 매개변수로 입력**되었지만 **몸무게는 음수가 될 수 없기에**
	**조건을 설정**하여 **음수가 입력되면 0으로 저장**하도록 했다.