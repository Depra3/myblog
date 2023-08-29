---
title: JAVA-객체
date: 2023/07/25 20:00:00
categories:
- JAVA
tags:
- 개념
- 객체
- 객체의 속성
- 객체의 기능
- 메서드
- 멤버 변수
- 필드
---

# 객체 (Object)

- **물리적으로 존재**하거나 **추상적으로 생각할 수 있는 것 중**에서 **자신과 다른 것을 식별 가능한 것**
    - **물리적**
        - 사람, 책, 자동차, 컴퓨터 등
    - **추상적**
        - 학과, 부서, 종류 등

# 객체의 구성

- **속성(property)**
    - 자동차의 **속성** - 제조사, 모델, 색깔 등
    - **멤버 변수(member variable), 특성(attribute), 필드(field), 상태(state)**
#
- **기능(function)**
    - 자동차의 **기능** - 시동, 주행, 정지 등
    - **메서드(method), 함수(function), 행위(behavior)**
#
- **코드**

	```java
	public class Car {
		// 속성 - 멤버 변수
		public String company;   // 제조사
		public String model;     // 자동차 모델
		public String color;     // 자동차 색깔
		public int maxSpeed;     // 최고 속도
		public int currentSpeed; // 현재 속도

		// 기능 - 메서드
		public void speedUp() {
			this.currentSpeed = this.currentSpeed + 1;
		}
		
		public int speedDown() {
			this.currentSpeed--;
			return this.currentSpeed;
		}
		
		public int getCurrentSpeed() {
			return this.currentSpeed;
		}
	}
	```