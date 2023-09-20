---
title: JAVA - 예외 발생 및 처리 (throw, throws)
date: 2023/09/20 22:20:00
categories:
- JAVA
tags:
- 개념
- Exception
- try
- catch
- finally
- throw
- throws
- 예제
---
<h1>
<details>
<summary>목차</summary>
<div markdown="1">

- [예외 ㅡ Exception](#예외-ㅡ-Exception)
- [throw](#throw)
- [throws](#throws)
</div>
</details>
</h1>
---

# 예외 ㅡ Exception

- **프로그램에 대한 사용자의 조작 또는 개발자의 코딩에서 문제가 발생하여 생기는 오류**
- **정의 및 종류 : [Depra3's JAVA - 예외(Exception) 정의 및 종류](https://depra3.github.io/2023/08/31/2023/08/JAVA-%EC%98%88%EC%99%B8(Exception)_%EC%A0%95%EC%9D%98_%EB%B0%8F_%EC%A2%85%EB%A5%98/)**
- **예외 처리 : [Depra3's JAVA - 예외처리 (try ~ catch ~ finally)](https://depra3.github.io/2023/09/03/2023/09/JAVA-%EC%98%88%EC%99%B8%EC%B2%98%EB%A6%AC(try~catch~finally)/)**

# throw

> **억지로 에러를 발생시키고자 할 때 사용되거나 현재 메소드의 에러를 처리한 후 상위 메소드에 에러 정보를 넘겨 상위 메서드에서도 에러가 발생한 것을 감지하게 함**
>
#
- **예시**
    
    ```java
    
    try {
    	예외가 발생할 가능성이 있는 코드들
    	throw new 예외 종류("~~ 예외 발생시 보내질 메시지 ~~"); // 예외 발생
    } catch(예외 종류){
    	예외가 발생하면 처리하는 코드들
    	System.out.println(e.getMessage());  // 메시지 받아서 출력
    } finally{  // 생략 가능
    	예외 상관없이 무조건 실행하는 코드들
    }
    ```
#    
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
    		try {
    			Human h1 = new Human("Depra3");
    			System.out.println(h1);
    			h1.run();
    			
    			h1 = null;
    			System.out.println(h1);
    			// 코드 추가
    			if (h1 == null) {
    				throw new NullPointerException("객체 h1가 존재하지 않습니다."); // 예외 발생
    			}
    			System.out.println("객체 h1 가 달리다.");
    			
    			h1.run();	// NullpointException
    		} catch (NullPointerException ne) {
    			System.out.println();
    			System.out.println("예외 발생!! Catch 블록 실행!!");
    			System.out.println(ne.getStackTrace());
    			System.out.println(ne.getMessage());
    			System.out.println(ne);
    		} ****finally {
    			System.out.println();
    			System.out.println("Finally 블록 실행!!");
    		}
    	}
    }
    ```
#    
- **결과**
    
    ![](/Images/2023/09/JAVA-예외발생및처리throw,throws/Untitled.png)
    
    - [**Depra3's JAVA - 예외처리 (try ~ catch ~ finally)](https://depra3.github.io/2023/09/03/2023/09/JAVA-%EC%98%88%EC%99%B8%EC%B2%98%EB%A6%AC(try~catch~finally)/) 글의 사용 예제 ① 과는 다른 결과를 볼 수 있다**
        
        ![](/Images/2023/09/JAVA-예외발생및처리throw,throws/Untitled%201.png)
        

---

# throws

> **현재 메서드에서 예외가 발생하면 해결하지 않고 자신을 호출한 상위 메서드로 예외를 전가시킴**
>
#
- **예시**
    
    ```java
    
    public static void main(String[] args) {
    	try {
    		예외가 발생할 가능성이 있는 코드들
    		func();
    	} catch(Exception e){
    		예외가 발생하면 처리하는 코드들
    		System.out.println(e.getMessage());  // 메시지 받아서 출력
    	} finally{  // 생략 가능
    		예외 상관없이 무조건 실행하는 코드들
    	}
    }
    --------------------------------------------
    public static void func() throws Exception {
    	throw new 예외 종류("~~ 예외 발생시 보내질 메시지 ~~");  // 예외 발생
    }
    ```
#    
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
    		try {
    			Human h1 = new Human("Depra3");
    			System.out.println(h1);
    			h1.run();
    			
    			h1 = null;
    			System.out.println(h1);
    			// 코드 추가
    			if (h1 == null) {
    				func();
    			}
    			System.out.println("객체 h1 가 달리다.");
    			
    			h1.run();	// NullpointException
    		} catch (NullPointerException ne) {
    			System.out.println();
    			System.out.println("예외 발생!! Catch 블록 실행!!");
    			System.out.println(ne.getStackTrace());
    			System.out.println(ne.getMessage());
    			System.out.println(ne);
    		} ****finally {
    			System.out.println();
    			System.out.println("Finally 블록 실행!!");
    		}
    	}
    
    	public static void func() throws NullPointerException {
    		throw new NullPointerException("객체 h1가 존재하지 않습니다.");  // 예외 발생
    	}
    }
    ```
#    
- **결과**
    
    ![](/Images/2023/09/JAVA-예외발생및처리throw,throws/Untitled%202.png)
    
    - **방식을 바꾸어 코드가 throw와 다르지만 결과가 같은 것을 볼 수 있다.**