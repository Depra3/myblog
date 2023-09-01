---
title: JAVA - 예외(Exception) 정의 및 종류
date: 2023/08/31 20:30:00
categories:
- JAVA
tags:
- 개념
- 객체 지향 프로그래밍
- 객체
- Error(오류)
- 예외
- 종류
- NullPointerException
- ArrayIndexOutOfBoundsException
- NumberFormatException
- ClassCastException
---


# 

# **예외 - Exception**

- **프로그램에 대한 사용자의 조작 또는 개발자의 코딩에서 문제가 발생하여 생기는 오류**
- **에러와 같이 문제가 발생하면 프로그램은 곧바로 종료**가 되지만, **예외는 처리를 통해 실행 상태가 정상이 되도록 할 수 있다.**
---
# **예외 종류**

## **1. NullPointerException**

- **객체 참조가 없는 상태에서 메서드를 호출할 때 발생**

### ① 객체 생성 후 객체가 가리키는 heap주소를 null로 변경할 경우

- **코드**
    
    ```java
    public class Human {
    	public String name;
    
    	public Human(String name) {
    		this.name = name;
    	}
    
    	public void run() {
    		System.out.println("달리다.");
    	}
    }
    ---------------------------------------
    public class Exam {
    	public static void main(String[] args) {
    		Human h1 = new Human("Depra3");
    		System.out.println(h1);
    		h1.run();
    		
    		h1 = null;
    		System.out.println(h1);
    		h1.run();	// NullpointException
    	}
    }
    ```
    
- **결과**
    
    ![](/Images/2023/08/JAVA-예외(Exception)_정의_및_종류/Untitled.png)
    

### ② 배열 변수에 null로 초기화 한 후 배열 내의 값을 접근할 경우

- **코드**
    
    ```java
    public class Exam {
    	public static void main(String[] args) {
    		int[] arr = null;
    		System.out.printf("intValue[0] = %d\n", arr[0]);  // NullpointException
    	}
    }
    ```
    
- **결과**
    
    ![](/Images/2023/08/JAVA-예외(Exception)_정의_및_종류/Untitled%201.png)
    
---
## **2. ArrayIndexOutOfBoundsException**

- **배열에서 인덱스 범위를 초과하여 사용할 경우 발생**
#
- **코드**
    
    ```java
    public class Exam {
    	public static void main(String[] args) {
    		int[] arr = { 10, 20, 30 };
    		System.out.printf("arr[0] = %d\n", arr[0]);
    		System.out.printf("arr[2] = %d\n", arr[2]);
    		System.out.printf("arr[3] = %d\n", arr[3]); // ArrayIndexOutOfBoundsException
    	}
    }
    ```
    
- **결과**
    
    ![](/Images/2023/08/JAVA-예외(Exception)_정의_및_종류/Untitled%202.png)
    
---
## **3. NumberFormatException**

- **문자열을 숫자로 변환하는 경우 주로 발생**

### 숫자로 변환할 수 없는 문자가 포함되어 있는 경우

- **코드**
    
    ```java
    public class Exam {
    	public static void main(String[] args) {
    		String str1 = "1000";
    		int int1 = Integer.parseInt(str1);
    		int intplus1 = int1 + 10;
    		System.out.printf("intplus1 : %d \n", intplus1);
    		
    		String str2 = "a1000";
    		int int2 = Integer.parseInt(str2);     // NumberFormatException
    		// str2는 숫자로 변환할 수 없는 형태이므로 Exception발생
    		int intplus2 = int2 + 10;
    		System.out.printf("intplus2 : %d \n", intplus2);
    	}
    }
    ```
    
    - **Integer.parseInt() 는 문자열을 숫자로 변환하는 함수다.**
#    
- **결과**
    
    ![](/Images/2023/08/JAVA-예외(Exception)_정의_및_종류/Untitled%203.png)
    
---
## **4. ClassCastException**

- **타입 변환이 되지 않을 때 발생**
#
- **코드**
    
    ```java
    public class Animal {
    	public Animal() {
    		System.out.println("animal 객체 생성");
    	}
    }
    --------------------------------------
    public class Cat extends Animal {
    	public Cat() {
    		super();
    		System.out.println("Cat 객체 생성");
    	}
    
    	public void run() {
    		System.out.println("고양이가 뛰어다니다.");
    	}
    }
    --------------------------------------
    public class Dog extends Animal {
    	public Dog() {
    		super();
    		System.out.println("Dog 객체 생성");
    	}
    	
    	public void run() {
    		System.out.println("강아지가 뛰어다니다.");
    	}
    }
    --------------------------------------
    public class AnimalExam {
    	public static void main(String[] args) {
    		// 상속관계에서의 자동타입변환
    		Animal animal = new Dog();
    		
    		// 강제타입변환
    		Dog d1 = (Dog) animal;
    		d1.run();
    		
    		// 강제타입변환
    		Cat c1 = (Cat) animal;   // ClassCastException
    		c1.run();
    	}
    }
    ```
    
- **결과**
    
    ![](/Images/2023/08/JAVA-예외(Exception)_정의_및_종류/Untitled%204.png)