---
title: JAVA - System클래스 - exit()
date: 2023/10/16 22:30:00
categories:
- JAVA
tags:
- 개념
- System 클래스
- exit()
- 예제
---
<h1>
<details>
<summary>목차</summary>
<div markdown="1">

- [System 클래스](#System-클래스)
- [exit() 메서드](#exit-메서드)
</div>
</details>
</h1>

---

# System 클래스

> **운영체제 시스템과 관련된 기능을 제공하는 클래스**
 **프로그램 종료, 키보드로 부터의 입력, 모니터로 출력, 메모리 정리, 현재 시간 읽기, 환경 변수 읽기, 시스템 프로퍼티 읽기 등의 기능이 존재**한다.
 해당 클래스의 **모든 필드와 메서드는 정적필드와 정적 메서드로 구성**되어 있다.
>

---

# exit() 메서드

- 현재 실행 중인 **프로세스를 강제로 종료시키고 싶을 때 사용**한다.
- **정상 종료일 경우 0, 비정상 종료일 경우 0 이외의 값**을 준다.
    
    ```java
    System.exit(0); // 정상종료
    System.exit(1); // 비정상종료
    ```
    
- **특정 값이 입력되었을 경우에만 종료하고 싶다면, 자바의 보안 관리자를 직접 설정**하면 된다.
#
- **코드**
    
    ```java
    public static void main(String[] args) {
    	// 임의의 값이 입력되면 종료되도록 보안 관리자 설정
    	System.setSecurityManager(new SecurityManager(){
    		public void checkExit(int status) {
    			if (status != 5) { // 임의의 값 설정
    				throw new SecurityException();
    			}
    		}
    	});
    	
    	for (int i = 0; i < 10; i++) {
    		System.out.println(i);
    		try {
    			System.exit(i);
    			// System.exit 메서드가 실행되면 checkExit이 자동으로 호출됨.
    			// checkExit이 정상적으로 끝나면 JVM이 자동적으로 동작됨.
    			// 0~4까지는 checkExit이 정상작동하지 않음으로(Exception이 발생하므로) JVM이 끝나지 않음
    			// 5일 때 자동으로 종료됨.
    		} catch (SecurityException e) {
    			e.printStackTrace();
    		}
    	}
    }
    ```
#
- **결과**
    
    ![](/Images/2023/10/JAVA-System클래스-exit/Untitled.png)