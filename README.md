## Parking Management System

이 프로젝트는 주차 관리 시스템을 구현하는 것을 목표로 합니다. 이 시스템은 주차장의 주차 및 결제 정보를 관리합니다.

### 구조

이 프로젝트는 MVC(Model-View-Controller) 패턴을 따릅니다. 이 패턴은 애플리케이션을 세 가지 역할로 분리하여 코드의 재사용성과 유지보수성을 향상시킵니다.

- Model: 데이터와 비즈니스 로직을 처리합니다. 이 부분에서는 데이터베이스 연결, 쿼리 실행, 데이터 처리 등의 작업을 수행합니다. (`Database.h`, `Database.cpp`)
- View: 사용자 인터페이스와 데이터의 시각적 표현을 담당합니다. 이 부분에서는 사용자에게 보여줄 화면을 구성하고, 모델로부터 받은 데이터를 사용자에게 보여주는 작업을 수행합니다. (`View.h`, `View.cpp`)
- Controller: 사용자의 입력을 처리하고, 모델과 뷰 사이의 인터페이스 역할을 합니다. 이 부분에서는 사용자의 입력을 받아 적절한 모델의 함수를 호출하고, 그 결과를 뷰에 전달하여 사용자에게 보여주는 작업을 수행합니다. (`Controller.h`, `Controller.cpp`)

### 데이터베이스

이 프로젝트는 주차장의 주차 및 결제 정보를 관리하기 위한 데이터베이스를 사용합니다. 이 데이터베이스는 다음과 같은 테이블을 포함합니다:

- Guest: 방문객에 대한 정보를 저장합니다. 각 방문객은 고유한 ID와 차량 ID를 가집니다.
- Members: 회원에 대한 정보를 저장합니다. 각 회원은 고유한 ID, 차량 ID, 이름, 주소, 전화번호, 그리고 만료 날짜를 가집니다.
- Admin: 관리자에 대한 정보를 저장합니다. 각 관리자는 고유한 ID, 이름, 전화번호, 그리고 이메일을 가집니다.
- Parking: 주차 정보를 저장합니다. 각 주차 정보는 고유한 ID, 방문객 ID, 회원 ID, 그리고 입차 시간을 가집니다.
- Pay: 결제 정보를 저장합니다. 각 결제 정보는 방문객 ID, 주차 요금, 결제 방법, 입차 시간, 그리고 출차 시간을 가집니다.

### 시작하기

이 프로젝트를 사용하려면, 먼저 데이터베이스를 설정해야 합니다. 이를 위해 `DB/query.txt` 파일에 있는 SQL 쿼리를 실행하세요. 이 쿼리는 데이터베이스 구조를 생성하고, 테스트 데이터를 삽입합니다.

그런 다음, 소스 코드를 컴파일하고 실행하세요. 이 프로젝트는 C++로 작성되었으므로, C++ 컴파일러가 필요합니다.

### 라이선스

이 프로젝트는 MIT 라이선스에 따라 배포됩니다. 자세한 내용은 `LICENSE` 파일을 참조하세요.

<aside>
👉 **Note:** 이 글은 Notion에서 작성되었으며, [여기](https://www.notion.so/)에서 확인하실 수 있습니다.

</aside>