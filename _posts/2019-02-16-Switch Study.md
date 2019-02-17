---
layout: post
title: 스위치 공부!
---
1.switch
	if문과 같은 제어문에 속한다.
	enum과 함께 사용된다.

3.2.switch 사용순서
	1.enum 정의하기
	2.enum을 상수에 넣어주기
	3.switch문 작성


A.
예) 빨주노초파람보 무지개색에서 보라색일 경우 "빨주노초파람보 중 보라색!" 출력하는 코드 작성하기.

1. enum Rainbow {
	case red
	case orange
	case yellow
	case green
	case blue
	case indigo
	case violet
	}
-enum뒤에 자료형을 만들어 준다. 이따 첫 문자는 대문자 사용.
-대괄호 안에 케이스로 여러경우의 수를 입력해준다.
-예문은 (Rainbow 자료형을 갖는 enum이고 red부터 violet 7가지 칼라의 경우를 가지고 있다)로 해석

2. let rainbowColor: Rainbow = Rainbow.violet
-새로운 상수를 생성. enum자료형을 맞춰주고 출력하려는 값을 넣어준다.
-예문은 (Rainbow자료형이고 그안에 Rainbow.violet값이 들어간 상수 rainbowColor를 생성했다)로 해석

3. switch rainbowColor {
	case Rainbow.red:
	print("빨주노초파람보 중 빨간색!")
	case Rainbow.orange:
	print("빨주노초파람보 중 주황색!")
	case Rainbow.yellow:
	print("빨주노초파람보 중 노란색!")
	case Rainbow.green:
	print("빨주노초파람보 중 초록색!")
	case Rainbow.blue:
	print("빨주노초파람보 중 파란색!")
	case Rainbow.indigo:
	print("빨주노초파람보 중 남색!")
	case Rainbow.violet:
	print("빨주노초파람보 중 보라색!")
}
-swich 조건에 상수 rainbowColor를 입력.
-대괄호 안에 상수의 값이 참일때 실행될 케이스를 입력해준다
-예문은 (rainbowColor(=Rainbow.violet)이고 이것이 참인 경우는 case Rainbow.violet: 일때 이므로 실행될 코드는 print안의 구문 "빨주노초파람보 중 보라색!" 이다.)로 해석

B.
예)
1.enum 자료형 : 자료형 {
case 1
case 2
case 3...
}


enum Animals: String{
case dog = "멍멍"
case cat = "냐옹"
case duck = "꽥꽥"
case cow = "음매"
}

2. let animalsSound : Animals = Animals.dog


3. switch animalsSound {
case Animals.dog:
print(Animals.dog.rawValue)
case Animals.cat:
print(Animals.cat.rawValue)
case Animals.duck:
print(Animals.duck.rawValue)
case Animals.cow:
print(Animals.cow.rawValue)
}
