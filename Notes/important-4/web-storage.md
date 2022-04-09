# 브라우저 저장소의 차이점

### LocatStorage

- 로컬 스토리지는 저장한 데이터를 지우지 않는 이상 영구적으로 보관이 가능합니다.([도메인](#gear-도메인)마다 별도로 로컬 스토리지가 생성됩니다.)
- 최대 크기: 5MB
- 사용 예시: 자동 로그인

### SessionStorage

- 세션 종료 시 클라이언트에 대한 정보가 삭제됩니다.
- 최대 크기: 5MB
- 사용 예시: 입력 폼 정보, 비로그인 장바구니

### [쿠키](#gear-쿠키)(Cookie)

- 웹 사이트에서 쿠키를 설정하면, 모든 웹 요청에는 쿠키 정보가 포함됩니다. => 서버 부담 증가
- 최대 크기: 4KB
- 사용 예시: 팝업 창

### 서버 인증과 브라우저 저장소

- 주요 정보를 요청 헤더에 넣는 방법

  > 보안에 매우 취약합니다.

- Session, Cookie 방식

  > 서버 부하가 증가하고, 세션 하이재킹 공격에 취약합니다.

- [JWT](#gear-jwt) 방식
  > 별도의 브라우저 저장소에 저장하지 않고 JWT를 발급하고 검증하면 되어 확장성이 뛰어납니다.<br>
  > 그러나 Payload 정보가 제한적이고, JWT길이가 길다는 단점 존재합니다.

<br>

---

<br>

## :hammer_and_wrench: 용어 공부

### :gear: 도메인

- ip는 사람이 이해하고 기억하기 어렵기 때문에 이를 위해서 각 ip에 이름을 부여할 수 있게 했는데, 이것을 도메인이라고 한다.

### :gear: 쿠키

- 쿠키(Cookie)란 인터넷 사용자가 어떠한 웹 사이트를 방문할 경우 그 사이트가 사용하고 있는 서버를 통해 인터넷 사용자의 컴퓨터에 설치되는 작은 기록 정보 파일입니다.

### :gear: JWT

- JWT(Json Web Token)란 Json 포맷을 이용하여 사용자에 대한 속성을 저장하는 Claim 기반의 Web Token입니다. JWT는 토큰 자체를 정보로 사용하는 Self-Contained 방식으로 정보를 안전하게 전달합니다.

<br>

## 참고

- [blog, 프론트엔드 면접 문제 은행](https://velog.io/@wkahd01/%ED%94%84%EB%A1%A0%ED%8A%B8%EC%97%94%EB%93%9C-%EB%A9%B4%EC%A0%91-%EB%AC%B8%EC%A0%9C-%EC%9D%80%ED%96%89-HTML-%EC%A7%88%EB%AC%B8-%EB%8B%B5%EB%B3%80#%EB%B8%8C%EB%9D%BC%EC%9A%B0%EC%A0%80-%EC%A0%80%EC%9E%A5%EC%86%8C%EC%9D%98-%EC%B0%A8%EC%9D%B4%EC%A0%90)
- [생활코딩, 도메인이란?](https://opentutorials.org/course/228/1450)
- [blog, 쿠키(Cookie)란?](https://stupidsecurity.tistory.com/9)
- [blog, JWT란?](https://mangkyu.tistory.com/56)