출처: https://www.youtube.com/watch?v=wjLwmWyItWI&list=PLRx0vPvlEmdBjfCADjCc41aD4G0bmdl4R, 이것이 자바다 (저자 신용권, 임경균)

## 1 Intro
### 1.1 프로그래밍 언어
고급언어: 컴퓨터와 대화할 수 있도록 만든 언어 중 사람이 쉽게 이해할 수 있는 언어, 컴파일 과정을 통해 기계어로 변환
저급언어: 기게어에 가까운 언어, 대표적으로 어셈블리어가 속함

### 1.2 Java
- JSP, 안드로이드에 사용
- 모든 운영체제에서 실행 가능
- 객체 지향 프로그래밍 언어
- 메모리 자동 정리
- 무료 오픈 소스 라이브러리 풍부

### 1.3 코드 용어 이해
- 패키지
  >     package ch01.sec09;
  > 소스 파일 위치: src/ch01/sec09
- 클래스
  >     public class Hello {}
  > 클래스명/소스파일명: Hello
- 메소드
  >     public static void main(String[] args) {}
  > 메소드명: main

- - -

## 2 기본 입출력
### 2.1 출력

- 줄바꿈o
  >     System.out.println("");

- 줄바꿈x
  >     System.out.print("");


- 다양한 자료형
  >     System.out.println("" + int);
  > 두 자료형 사이에 + 사용

### 2.2 입력

- int
  >     Scanner scan = new Scanner(System.in);
  >     int i = scan.nextInt();
  >     scan.close();

- String
  >     Scanner scan = new Scanner(System.in);
  >     String j = scan.next();
  >     scan.close();

*다른 자료형의 경우 nextDouble() 등과 같이 자료형명 붙여 작성

### 2.3 파일 입출력
    File file = new File("input.txt");
    
    //오류 발생 대비 try catch문으로 만들기
    try {
      Scanner scan = new Scanner(file);
      while(scan.hasNextInt())
      {
        System.out.println(scan.nextInt() * 100);
      }
      scan.close();
    } catch (FileNotFoundException e) {
      System.out.println("파일을 읽어오는 도중 오류가 발생했습니다")
    }

- - -   

## 3 변수
- 변수
    + 하나의 값을 저장할 수 있는 메모리 번지에 붙여진 이름   
    + 프로그램이 실행되는 동안 저장된 값이 변경될 수 있는 공간   
- 상수: 한 번 정해지면 값이 변경될 필요가 없는 데이터

### 3.1 변수 선언
- 정수: int
  >     int integer = 100;
  
- 실수: double
  >     double real = 100.5;
  
- 문자: String
  >     String string = "word";

### 3.2 상수 선언
>     final static int PI = 3.14
> final: 상수   

### 3.3 오버플로우
int의 범위는 무한대가 아님   
-21억부터 +21억까지의 순환되는 범위를 가지고 있음
- - -

## 4 자료형

### 4.1 자료형 종류
- 정수
  + byte: 1 byte: -128~127
  + short: 2 byte: -32768~32767
  + char: 2 byte
  + int: 4 byte: 
  + long: 8 byte
- 실수
  + float: 4 byte
  + double: 8 byte
- string
- boolean    

#### 4.1.1 int의 활용
- 8진수로 변환
  >     System.out.format("8진수 %o", int);

- 16진수로 변환
  >     System.out.format("16진수 %x", int);

#### 4.1.2 char의 활용
ASCII 코드 기반으로 활용됨

#### 4.1.3 substring의 활용

    string = "word"
    System.out.println(string.substring(0,3);

substring을 사용해 string의 각 char를 array 형식으로 쪼갤 수 있음

### 4.2 자료형 변환

    int integer = (int) real
    
  실수 real의 소숫점 아래를 버림하여 정수 integer로 변환

    String j = i + ""

  정수 i를 문자열 j로 변환
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

### 7.1 무한루프
for( ; ; )   
break; 사용해서 루프 종료

- - -

## 9 사용자 정의 함수
정해진 특정한 기능을 수행하는 모듈   
각각의 모듈로서 쉽게 수정, 보완 가능   

반환형 함수명(매개변수){} 꼴로 작성   
*반환형이 없는 경우: void

    public static int function(int a, int b, int c){
      for (int i = min; i > 0; i--){
        if (a % i == 0 && b % i == 0 && c % i == 0){
          return i;
          //현재의 i값을 반환하며 함수 종료
        }
      }
        return -1;
    }

### 9.1 반복 함수
반복문을 포함한 함수

    public static int factorial(int number){
      int result = 1;
      for(int i = number; i > 1; i--){
        result *= i;
      }
      return result;
    }

### 9.2 재귀 함수
함수 안에 동일한 함수를 포함한 경우

    public static int factorial(int number){
      if (number == 1){
        return 1;
      } else{
        return number * factorial(number - 1)
        //f(number) = number * f(number-1) = number * (number-1) * (number-2) ... until number == 1
      }
    }

- - -
    
## 10 배열
많은 양의 데이터를 저장할 공간을 한번에 생성   

배열 선언

    int[] array = new int[a];
    //a개의 원소가 들어가는 배열 생성

### 10.1 다차원 배열

2차원 배열 선언

    int[][] array = new int[a][b]
    //a개의 행과 b개의 열을 가진 배열 생성

- - -

## 11 클래스

main method: 프로젝트에서 한 개만 존재 가능

Node: 점의 좌표를 나타냄

Node라는 class 아래에 private variable x, y 생성   
*private: 외부에서 한 번에 접근할 수 없는 변수

    public class Node {
      private int x;
      private int y;


고로 외부에서 x값에 접근할 수 있도록 하는 함수를 따로 만들어줘야함
  
      public int getX() {
        return x;
      }

x값을 설정할 수 있도록 하는 함수도 생성   
갖고 있던 변수 this.x를 매개변수로 받은 x의 값으로 바꿔줌  

      public void setX(int x) {
        this.x = x;
      }      

*y도 동일하게 작성   
*우클릭> Source> Generate Getters and Setters 이용해 자동 생성

생성자: 객체를 만들어줄 때 자동으로 값을 초기화 해주는 함수   
클래스와 동일한 이름을 가짐   


      public Node(int x, int y) {
        this.x = x;
        this.y = y;
      }

*우클릭> Source> Generate Constructor using Fields 이용해 자동 생성

다른 Node의 좌표를 받아 현재 Node와의 정중앙의 좌표를 반환

      public Node getCenter(Node other) {
        return new Node((this.x + other.getX()) / 2, (this.y + other.getY()) / 2)
      }

### 11.1 상속
다른 클래스가 가지고 있는 정보를 받는 것   
한 개 이상의 클래스에 상속 가능

    public class Person {
      private String name;
      private int age;
      //getter & setter 생성 
      //생성자 생성
    }

Person 클래스를 상속 받아 사용하는 Student 클래스

    public class Student extends Person {
      private String studentID;
      private int grade;
      //getter & setter 생성

Student 클래스에서 생성자 자동 생성 시

      public Student(String name, int age, String studentID, int grade) {
        super(name,age);
        this.studentID = studentID;
        this.grade = grade;
      }

super: 부모가 가진 생성자 실행

Student 클래스에 변수값을 출력하는 함수 show() 생성

    public void show() {
      System.out.println("이름: "+getName());
      //다른 변수로도 동일하게 작성성
    }


Main 클래스에서 Student 클래스의 정보를 불러올 시

    public static void main(String[] args) {
      Student student = new Student("name", age, "student ID", grade);
      student.show();
    }

- - -

## 12 JAVA 객체지향의 활용
추상, 인터페이스 등의 개념이 존재

### 12.1 추상
미완성 클래스
직접적으로 객체 인스턴스를 생성할 수 없으나 새로운 클래스를 작성하는 데에 밑바탕이 되는 역할을 함   
Override로 구현해야 할 함수를 알려줘 설계적인 측면에서 도움이 됨

추상 클래스 정의

    abstract class Player {
      abstract void play(String songName);
      abstract void pause();
      abstract void stop();
    }

Main 클래스에서 Player 클래스를 상속 받도록 함

    public class Main extends Player {

Main의 밑줄에서 Add unimplements methods 선택해 구현이 안된 함수 추가

      void play(String songName) {
        //각 함수에서 실행시킬 내용 구현
      }
      void pause() {
        //
      }
      void stop () {
        //
      }

Main 메소드 안에서 다른 메소드를 불러오기 위해서 해당 메소드도 Main과 동일하게 static으로 선언되어야함   
Main 클래스 활용해 인스턴스 생성, 인스턴스에서 함수 사용

      Main main = new Main();
      main.play("songName");
      main.pause();
      main.stop();
      
- - -

## 13 최종
최종(final): 절대 변하지 않는 특정한 것을 정하고 싶을 때 사용

    final int number = 10;
    number = 5;
    //오류 발생: number 변수값 바뀔 수 없음

상속 받은 함수를 main 클래스에서 재정의해 사용할 수 있음   
부모 클래스에서 함수를 정의할 때 최종을 붙인 경우:

    public final void show() {
    }

main 클래스에서 show() 함수 재정의 불가해짐

클래스를 final로 정의하는 경우:
    
    final class Parent {
    }

Parent 클래스는 다른 클래스에서 상속을 받을 수 없게됨

- - -

## 14 인터페이스
- 추상 클래스와 흡사한 개념
  + 추상화의 정도가 높음
  + 요구되는 설계의 기준이 더 높음
- 추상 클래스는 추상 메소드 외에 멤버 변수나 일반 메소드를 가질 수 있지만 인터페이스에서는 반드시 사전에 정의된 추상 메소드와 상수만을 가질 수 있음

      public interface Dog {
        public void show() {}
        //인터페이스 안에서 함수 구현 불가 > 오류 발생
        public void show();
        //함수가 존재한다는 부분만 설계
      }

인터페이스를 main 메소드에서 사용할 때:

    public class Main implements Dog {
    }

인터페이스의 경우 하나의 클래스에서 여러 개의 인터페이스를 다중으로 상속 받을 수 있음   
*추상 클래스의 경우에서는 불가
- - -

## 15 다형성
다양한 형태의 성질을 가진다는 의미

    public class Fruit {
      //fruit의 정보 변수 설정
      //fruit의 정보 출력하는 show() 함수 작성    
    }

Fruit를 상속 받는 클래스 Peach 생성

    public class Peach extends Fruit {
      //fruit에서 설정한 변수에 대한 peach의 정보 정의
    }

Main클래스에서 Peach 사용 시

부모 클래스의 변수로서 자식 클래스의 인스턴스를 사용 가능

    public class Main {
      public static void main(String[] args) {
        Fruit fruit = new Peach();
        fruit.show();
      }
    }

- - -

## 16 객체
객체(object) 클래스는 모든 객체의 조상으로써 쓰임   
자바의 모든 클래스는 Object 클래스를 상속 받음   
모든 클래스가 공통적으로 포함하고 있는 기능을 제공

    public class Archer {
      String name;
      String power;
    
      public Archer(String name, String power) {
        this.name = name;
        this.power = power;
      }
    
      public boolean equals(Object obj) {
        Archer temp = (Archer) obj;
        //Object가 Archer의 부모 클래스이기 때문에 Object의 변수를 Archer 형태로 바꿀 수 있음
        if (name == temp.name && power == temp.power) {
          return true;
        }
        else {
          return false;
        }

    }

equals(Object obj) 함수를 Main 클래스에서 사용하는 경우

    Archer archer1 = new Archer("1번", "상");
    Archer archer2 = new Archer("1번", "상");

    System.out.println(archer1 == archer2);
    //false 출력: 두 인스턴스가 같은지 판단
    System.out.println(archer1.equals(archer2));
    //true 출력: 두 인스턴스가 내부적으로 가지는 값이 같은지 판단
    

























      
