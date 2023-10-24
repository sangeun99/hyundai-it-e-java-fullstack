## 13장. 이너 클래스와 이너 인터페이스

- 중첩된 형태의 nested class
- 아우터 클래스
    - 멤버 이너 클래스
        - 인스턴스 멤버 클래스
        - 정적 멤버 클래스
    - 지역 이너 클래스
        - 지역 클래스

### 이너 클래스의 클래스 객체 생성

- 아우터 클래스의 인스턴스를 먼저 생성한 후 그 인스턴스를 이용하여 이너 클래스의 인스턴스를 생성할 수 있다
    - 정적 이너 클래스의 경우, 아우터클래스 인스턴스 없이 바로 생성 가능하다.
        - but 아우터 인스턴스 없이 접근할 경우 메모리에 없는 애들은 접근이 안 됨
        - static이 붙은 메서드와 필드만 접근 가능
- 아우터 클래스의 모든 필드를 사용할 수 있다
    - private도 모두 사용 가능
- 이너클래스 내부에서 아우터클래스의 멤버를 참조하고 싶다면 “아우터클래스명.this” 이용

- p.434 코드에서 b는 스택에 저장이 됨. 그래서 자동으로 final 선언됨
- class B에서는 b에 접근할 수 없음

### 이너 인터페이스

- 정적 이너 인터페이스만 존재할 수 있음
- A(아우터클래스)의 인스턴스 없이 인터페이스를 사용하려면 당연히 static으로 정의되어야 함