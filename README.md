# Java
## 1 Intro
- JSP, 안드로이드에 사용됨   
- 운영체제 가리지 않고 실행   
- 객체 지향 프로그래밍 언어   
- - -

## 2 Print
### 2.1 기본

    System.out.println("");

### 2.2 다양한 자료형

    System.out.println("" + int);

두 자료형 사이에 + 사용
- - -   

## 3 변수
변수: 프로그램이 실행되는 동안 저장된 값이 변경될 수 있는 공간
상수: 한 번 정해지면 값이 변경될 필요가 없는 데이터

### 3.1 변수 선언
- 정수: int

      int integer = 100;
  
- 실수: double
  
      double real = 100.5;
  
- 문자: String

      String string = "word";

### 3.2 상수 선언

    final static int PI = 3.14
    
final: 상수   

### 3.3 오버플로우
int의 범위는 무한대가 아님   
-21억부터 +21억까지의 순환되는 범위를 가지고 있음

- - -
## 4 자료형

### 4.1 자료형 종류
대표적으로는:
  - int
  - float
  - double
  - string
  - char
  - boolean   

등이 존재한다   

#### 4.1.1 int의 활용
8진수로 변환

    System.out.format("8진수 %o", int);

16진수로 변환

    System.out.format("16진수 %x", int);

#### 4.1.2 char의 활용
ASCII 코드 기반으로 활용됨

#### 4.1.3 substring의 활용

    string = "word"
    System.out.println(string.substring(0,3);

substring을 사용해 string의 각 letter를 array 형식으로 쪼갤 수 있음

### 4.2 자료형 변환

    int integer = (int) real
    
  실수 real의 소숫점 아래를 버림하여 정수 integer로 변환














    

