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

## 8 기본 입출력

- int

      Scanner scan = new Scanner(System.in);
      int i = scan.nextInt();
      scan.close();

- String
  
      Scanner scan = new Scanner(System.in);
      String j = scan.next();
      scan.close();

*다른 자료형의 경우 nextDouble() 등과 같이 자료형명 붙여 작성

### 8.1 파일 입출력
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
      









      
