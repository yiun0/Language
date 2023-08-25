# Java
## 1 Intro
- JSP, 안드로이드에 사용   
- 운영체제 가리지 않고 실행   
- 객체 지향 프로그래밍 언어   
- - -

## 2 Print
### 2.1 기본

- 줄바꿈o
  
        System.out.println("");

- 줄바꿈x
 
        System.out.print("");


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
- 정수
  + short: 2 byte
  + int: 4 byte
  + long: 8 byte
- 실수
  + float: 4 byte
  + double: 8 byte
- string
- char
- boolean    

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

substring을 사용해 string의 각 char를 array 형식으로 쪼갤 수 있음

### 4.2 자료형 변환

    int integer = (int) real
    
  실수 real의 소숫점 아래를 버림하여 정수 integer로 변환
- - -

## 5 연산자

### 5.1 기본 연산자
- 덧셈: +
- 뺄셈: -
- 곱셈: *
- 나눗셈: /
- 나머지: %

### 5.2 증감연산자
- ++ : +1   
  동일한 증감식
  + i += 1
  + i = i + 1
- -- : -1   

증감연산자가 출력문 안쪽에 위치한 경우
- ++a: +1 먼저 실행 후 a값 출력
- a++: a값 출력 후 +1

### 5.3 논리 연산자
- a == b: a와 b의 값이 같으면 참 반환
- a > b: a가 b보다 크면 참 반환
- a < b: a가 b보다 같으면 참 반환
+ (조건) && (조건): 두 개의 조건이 모두 만족되면 참 반환
+ !(조건): 조건이 만족되지 않는 경우 참 반환

### 5.4 삼항 연산자
    int result = (a > b) ? a : b;
(조건) ? 참 반환값 : 거짓 반환값 꼴로 작성

### 5.5 pow() 함수의 활용
    double a = Math.pow(3.0, 20.0)
a = 3^20
- - -

## 6 조건문
조건에 따라 결정을 내리는 것
- String

      if(a.contains("word")){
          //if문이 참인 경우 실행
      }
      else{
          //if문이 거짓인 경우 실행
      }

- int

      if(a >= 20){
          //if문이 참인 경우 실행
      }
      else if(a >= 10){
          //if문이 거짓이고 else if문이 참인 경우 실행
      }
      else{
          //if문과 else if문이 모두 거짓인 경우 실행 

- - -

## 7 반복문
반복적으로 어떠한 처리를 되풀이하는 것
- while

        int i = 1, sum = 0;
        while(i <= 1000){
            sum += i++;
            //sum에 i값을 더한 후 i값에 +1
        }
          
- for   
  for(변수 초기화; 조건; 연산) 꼴로 작성

          for(int i = 30; i > 0; i--){
              //i > 0인 동안 실행
          }










    

