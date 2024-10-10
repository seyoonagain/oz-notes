# Library vs. Framework

개발 공부를 하면서 가장 어려운 것이 이런 용어들이다.  
라이브러리와 프레임워크.  
차이에 대한 영상을 분명 여러 번 봤는데도 또 헷갈려서 문서화를 통해 기억에 칵 남기고자 한다.

<br>

일단 두 단어 자체의 의미로부터 그 특징과 차이를 느낄 수 있다.

- **Library**: 특정 기능이나 도구를 제공하는 코드 모음

  도서관이라는 뜻의 라이브뤄뤼~  
  도서관에 가면 내가 원하는 정보를 찾아 책을 골라서 보는 것처럼  
  개발에 있어 라이브러리란, 두둥!  
  내가 원하는 기능을 가진 도구이며, 필요할 때 꺼내(import)와서 쓸 수 있다.

  프레임워크보단 작은 단위의 기능 구현에 사용되는 도구라고 볼 수 있다.

  - 라이브러리의 예시: React, Axios, Moment.js,...

<br>

- **Framework**: 애플리케이션의 전체 구조와 규칙을 제공하며 애플리케이션의 구축 방식이 정해져 있는 환경

  틀이라는 뜻의 프뤠임~  
  서비스 구현을 위해 모든 것이 정해져 있고,  
  그 정해진 틀에서 벗어나지 않고 규칙에 따라 기능을 구현해 나갈 수 있는 환경이라 할 수 있다.

  - 프레임워크의 예시: Next.js, Express.js, Angular, Android, iOS, ...

---

### 장단점

- **Library**

  - 장점
    - 라이브러리가 제공하는 특정 기능에 대해서만 숙지하면 되기 때문에 진입 장벽이 보다 낮다.
    - 애플리케이션의 흐름을 개발자가 직접 유연하게 제어할 수 있다.
  - 단점
    - 필요한 기능을 위한 여러 라이브러리를 조합하다보면 관리가 복잡해질 수 있다.
    - 큰 규모의 프로젝트 시 아키텍처 설계에 많은 고민이 필요하다.

- **Framework**

  - 장점
    - 전체적인 구조가 이미 잡혀있기 때문에 개발을 시작하기 수월하다.
    - 일관성을 유지할 수 있다.
    - 외부 라이브러리가 아닌 프레임워크 내부 기능을 사용함으로써 더 안정적이고 빠른 개발이 가능하다.
  - 단점
    - 초기 사용 시 정해진 규칙을 숙지해야 하므로 처음 사용하기 어려울 수 있다.
    - 정해진 대로 해야하기 때문에 자율성이 떨어진다.

---