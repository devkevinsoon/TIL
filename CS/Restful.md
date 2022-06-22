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

    또 아래의 주소로 접속하면 트윗터의 글을 가져올 수 있다. 데이터를 가져오는 것 뿐만 아니라 데이터를 추가, 수정, 삭제 하는 것도 가능하다. (ex. CRUD)

```javascript
    https://api.twitter.com/2/tweets/1067094924124872705
    {
        "data" : {
            "id" : "1067094924124872705",
            "text": "Just getting started with Twitter APIs"
        }
    }
```

    이렇게 인터넷과 웹을 통해서 나의 컴퓨터를 제어할 때 어떻게 하면 시행착오를 줄이고 더 좋은 API를 만들수 있는가에 대한 고민의 결과물이 REST API라고 할 수 있을 것 같다.

    REST API는 특정 기술을 의미하는 것이 아닌 HTTP를 이용해서 기계들이 통신을 할 때 HTTP가 가진 잠재력을 최대한 이용할 수 있도록 유도하기 위한 모범사례라고 말 할 수 있다.

### 🌱 RESTFul

    👨‍💻 REST가 적용된 시스템
    RESTFul : REST가 적용된 시스템
    REST API를 제공하는 시스템은 RESTful이다. 그런데 보다 정확하게 표현된 REST라는 개념은
    다음의 6가지 조건을 만족해야 한다.

    1. 일관된 인터페이스(Uniform interface)
    URI 사용, HTTP 메소드 사용, RPC 미호출 등의 지정된 인터페이스를 준수한다.
    2. 클라이언트/서버(Client-Server)
    클라이언트는 서버에 요청(request)메시지를 전송하고
    서버는 요청에 대한 응답(response)메시지를 전송한다.
    3. 비연결성(Statelessness)
    세션 등 이전 상황(문맥) 없이도 통신할 수 있다.
    4. 캐시가능(cacheable)
    서버의 응답 메시지는 캐싱(저장 후 재사용)될 수 있다.
    5. 계층화된 시스템(Layered system)
    계층별로 기능이 분리된다. 그러므로 중간 계층의 기능(로드 밸런싱, 서버증설, 인증 시스템 도입 등)이 변경되어도 통신에 영향을 주시 않는다.
    6. 주문형 코드(code on demand)(선택)
    손쉬운 데이터 처리를 위해 서버는 클라이언트서 실행될 스크립트를 전송할 수 있다.

    `REST`는 `HTTP`를 잘 활용하기 위해서 만들어진 `아키텍처 스타일`이다. 이는 아키텍처 제작 시 사용되는 가이드(지침)정도의 의미로 사용되며 명확히 준수해야 할 표준은 없다. 그렇다 보니, 겉으로는 REST를 표방하고 있으나  특히 "1.일관된 인터페이스" 조건을 준수하지 않아 REST가 아닌 경우가 많다.

    - 오늘날 대부분의 “REST API”는 사실 REST를 따르지 않고 있다.
    - REST의 제약조건 중에서 특히 **Self-descriptive**와 **HATEOAS**를 잘 만족하지 못한다.
    - REST는 **긴 시간에 걸쳐(수십년) 진화** 하는 웹 어플리케이션을 위한 것이다.
    - REST를 따를 것인지는 API를 설게하는 이들이 스스로 판단하여 결정해야한다.
    - REST를 따르겠다면, **Self-descriptive**와 **HATEOAS**를 만족시켜야한다.
    - self-descriptive는 **custom media type**이나 **profile link relation**등으로 만족시킬 수 있다.
    - HATEOAS는 HTTP헤더난 본분에 링크를 담아 만족시킬 수 있다.
    - REST를 따르지 않겠다면, “REST를 만족하지 않는 REST API”를 뭐라고 부를지 결정해야 할 것이다.
    - HTTP API라고 부를 수도 있고
    - 그냥 이대로 REST API라고 부를 수도 있다.~~( Roy  T. Fielding이 싫어함)~~
