## 💡 Restful API에 대해서 아는대로 설명해보세요?

    👨‍💻 RESTful하다는 것 = REST한 특징을 지키는 것을 의미한다.
    👨‍💻 소통이 원활한 API를 구성하는 것

### 🌱 REST

    👨‍💻 (Representational State Transfer) : 자원(리소스)의 표현을 가지고 상태(정보) 전달
    👨‍💻 클라이언트 ↔ 서버의 통신 방식.
    👨‍💻 URI와 HTTP를 이용한, 통신 목적의 아키텍처 스타일(유형).
    👨‍💻 *URI(Uniform Resource Identifier):문서, 그림, 영상 등의 자원 식별용 이름(경로)
    👨‍💻 *아키텍처 스타일 : 아키텍처(구조)의 종류(유형, 스타일, 타입). 제약조건의 집합

### 🌱 REST API

    👨‍💻 REST 아키텍쳐 스타일을 따르는 API
    REST API는 컴퓨터의 기능을 실행시키는 명령이라고 할 수 있는데, 내 컴퓨터를 실행시키는 것이 아닌 남의 컴퓨터를 실행시킨다.
    예를 들어 나의 앱이 아래의 주소로 접속하면 구글 켈린더에 등록되어 있는 나의 켈린더를 구글 켈린더에서 아래와같이 출력해준다.

```javascript
    https://www.googleapis.com/…/calendars/calendar_id
    {
	    "summary" : "일정",
	    "timeZone": "Asia/Seoul"
    }
```
