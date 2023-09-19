# study_eGov

## Interface class & Abstract class

1. 공통점

- 두 클래스 다 선언만 있고 구현 내용은 없는 클래스
- 자기 자신이 new 로 객체생성을 해서 사용하는 게 불가능
- abstract class 는 extends 한 자식 클래스 & interface class 를 implements 한 자식 인터페이스만
  객체를 생성할 수 있다.

---

2. 차이점

- Abstract class (추상클래스)
- 추상 클래스는 말 그대로 클래스, 인터페이스와 같은 경우 구현하기 전 메소드에 대해 명시된 것으로 볼 수 있다.
- 추상클래스와 같은 경우 반드시 클래스 내에 Abstract Method() (추상메소드) 가 존재해야 한다.
- 오로지 **단일 상속(extends)**만 가능
- 여러 메서드가 있지만 가져다 쓰거나 오버라이드 하거나, abstract 가 붙은 메서드는 반드시 구현해야 한다.
- class A extends b {} 라고 하면 A 는 B 라는 클래스를 상속 받겠다고 이해하면 된다.

---

- Interface class
- 인터페이스는 구현체 없이 메소드에 대한 명세만 되어있다.
- 상속받는 자식클래스에는 반드시 인터페이스에 있는 메소드를 다 구현해야 한다.
- implements 를 구현하는 부분에서 extends 또한 사용할 수 있다. (**다중 상속** 가능)
- '이러한 메소드를 사용할 것이다.' 라는 망므으로 인터페이스에 선언한 다음 선언된 그대로 모두 구현해야 하는 게 인터페이스다.
- class A implements C {} 라고 하면 A 는 C 라는 인터페이스를 구현하겠다는 의미로 생각하면 된다.
- 구현 객체의 같은 동작을 보장한다.
- 오로지 메소드 선언만 가능하다.
- 생성자와 일반 변수를 가질 수 없다.
- 추상메소드만 가능하다.

---

3. 사용처

- 추상클래스는 IS - A "~이다"
- 인터페이스는 HAS - A "~을 할 수 있는"

---

## DAO class & VO class

1. DAO(Data Access Object) class

- jdbc 에 연결하는 (데이터베이스 접근) class
- 데이터베이스에 접속해서 데이터의 CRUD 를 수행하는 class
- 일반적으로 JSP 혹은 Servlet 에서 함께 기술 할 수 있지만, 유지보수 및 코드의 모듈화를 위해 별도의 DAO class 를 만들어서 사용
- **보통 한 개의 테이블에 한 개의 DAO class 를 작성**
- DAO class 는 singleton pattern 으로 작성

2. VO(Value Object) class / DTO(Data Transfer Object) class

- DAO 클래스를 이용해 데이터베이스에서 데이터를 관리할 때 데이터를 일반적인 변수에 할당해 작업할 수 있지만, 별도의 VO 클래스를 작성해 데이터베이스와 관련된 변수들의 모음 역할을 함
- VO 클래스의 변수들은 외부에서 쉽게 접근할 수 없도록 은닉(private) 처리

## project 생성

- ctrl + n -> eGovFrame Web Project
