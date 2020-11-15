# Java

1. **Java**란?
   * 객체지향 프로그래밍 언어(Oriented Object Programming)
     * 객체 지향 언어의 특징인 **캡슐화, 상속성, 다형성**을 지원
   * Compile 언어이면서 Interpreter 언어
   * 메모리를 자동으로 관리(Garbage Collection)
   * 동적 로딩을 지원 (필요한 시점에 클래스를 로딩하여 사용 가능)



2. **Java**의 컴파일 과정

   * Java Compiler(javac.exe)를 통해 Byte code로 변환

   * Byte code를 클래스 로더를 통해 JVM에 로드

   * Interpreter가 Byte code를 Binary code로 변환

   * Runtime

     

3.  **Java**의 메모리 영역

   * Stack Area

     * 메소드가 동작할 때 사용되는 정보들이 저장되는 공간
     * 매개변수, 지역변수 등이 LIFO(Last In First Out)방식으로 저장되며 실행 완료시 제거
     * Thread마다 자신만의 stack 보유
     * primitive type 데이터가 값과 함께 할당

   * Heap Area

     * reference type 데이터가 생성(해당 object를 가리키는 레퍼런스 변수가 stack에 올라감)

     * 스레드의 개수에 상관없이 단 하나의 heap만 존재

     * Garbage Collection의 대상이 됨

       

4. 데이터 타입

   * 기본형 타입(Primitive Type)

     * 8가지의 타입 제공
     * 기본값이 있기 때문에 Null이 존재하지 않음
     * 실제 값을 Stack area에 저장

     |        |  타입   | 할당 메모리 크기 |  기본값  |                      데이터 범위                       |
     | :----: | :-----: | :--------------: | :------: | :----------------------------------------------------: |
     | 논리형 | boolean |      1 byte      |  false   |                      true, false                       |
     | 정수형 |  byte   |      1 byte      |    0     |                       -128 ~ 127                       |
     | 정수형 |  short  |      2 byte      |    0     |                    -32,768 ~ 32,767                    |
     | 정수형 |   int   |      4 byte      |    0     |             -2,147,483,648 ~ 2,147,483,647             |
     | 정수형 |  long   |      8 byte      |    0L    | -9,223,372,036,854,775,808 ~ 9,223,372,036,854,775,807 |
     | 실수형 |  float  |      4 byte      |   0.0F   |        3.4E-38(-3.4*10^38) ~ 3.4E+38(3.4*10^38)        |
     | 실수형 | double  |      8 byte      |   0.0    |    1.79E-308(-1.79*10^308) ~ 1.79E+308(1.79*10^308)    |
     | 문자형 |  char   |      2 byte      | '\u0000' |                       0 ~ 65,535                       |

     

   * 참조형 타입(Reference Type)

     * 기본형 타입을 제외한 모든 데이터
     * Null이 존재
     * 값이 저장되어 있는 곳의 주소값을 Heap area에 저장



---

### 용어 정리

* Garbage Collection
  * 더 이상 필요로 하지 않는 (쓰레기)객체를 찾아 지움