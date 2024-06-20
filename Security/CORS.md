CORS(Cross-Origin Resource Sharing)는 다른 출처의 자원을 공유할 수 있도록 하는 보안 체제이다.

*출처란 ?*
![](https://i.imgur.com/R4mJ2dF.png)
위의 구성요소 중에서 **Protocol + Host + Port** 3가지가 같으면 동일 출처(Origin)라고 한다.


| 동일 출처 예시                                                                 |                                                     |
| ------------------------------------------------------------------------ | --------------------------------------------------- |
| http://Example.com:80<br>http://example.com                              | HTTP 기본 Port인 80번이 생략되어있으므로 동일 출처이다.                |
| http://example.com/app1/index.html<br>http://example.com/app2/index.html | Protocol, Host, Port(생략)이 같으며, Path부터 다르므로 동일 출처이다. |

| 다른 출처 예시                                                                 |                     |
| ------------------------------------------------------------------------ | ------------------- |
| http://example.com/app1  <br>https://example.com/app2                    | Protocol이 다릅니다      |
| http://example.com<br>http://www.example.com<br>http://myapp.example.com | Host가 다릅니다          |
| http://example.com<br>http://example.com:8080                            | 80, 8080으로 포트가 다릅니다 |

#### 다른 출처의 위험성

- CORS 설정이 잘못되면 API 키와 같은 중요한 정보가 노출될 수 있다.
- CORS 취약점을 악용하여 다른 사용자의 데이터에 접근할 수 있다.
- CORS 설정 오류로 인해 악성 웹사이트가 동일 출처 정책을 우회할 수 있다.

 따라서, 다른 출처의 접근을 막기 위해서는 동일 출처 정책이 필요하다.

#### 동일 출처 정책

동일 출처 정책(Same-Origin Policy)이란 웹 보안을 위한 중요한 메커니즘으로, 웹 페이지의 자바스크립트 코드가 다른 출처의 리소스와 상호 작용하는 것을 제한하는 정책이다. 이를 통해 잠재적으로 악성적인 문서를 격리하여 공격 벡터를 줄이고, 동일한 출처에서 가져온 리소스만 상호 작용할 수 있도록 하여 웹 보안을 강화한다.

**즉, 요청하는 클라이언트와 요청받는 서버가 같은 출처에 있으면 동일 출처, 서로 다른 서버에 있으면 다른 출처 요청이다.**
![](https://i.imgur.com/mwiFAO4.png)


### 다른 출처 요청의 특징

1. 단순요청(Simple Request):
    - HTTP 메서드가 GET, HEAD, POST 중 하나이고,
    - Content-Type 헤더가 application/x-www-form-urlencoded, multipart/form-data, text/plain 중 하나인 경우
    - 이런 요청은 브라우저가 자동으로 Origin 헤더를 추가하여 보낸다.
    - 서버에서는 Access-Control-Allow-Origin 헤더로 응답하여 허용 여부를 알려준다.
    
2. 플리플라이트 요청(Preflight Request):
    - Simple Request 조건을 만족하지 않는 경우 (예: PUT, DELETE 메서드 사용)
    - 브라우저가 먼저 OPTIONS 메서드로 Preflight 요청을 보낸다.
    - 서버에서는 Access-Control-Allow-Origin, Access-Control-Allow-Methods, Access-Control-Allow-Headers 등의 헤더로 응답한다.
    - 브라우저가 이 응답을 확인하고 본 요청을 보낸다.
    
3. 신용 요청(Credentialed Request):
    - 쿠키, HTTP 인증 정보 등 자격 증명(credentials)이 포함된 요청
    - Simple Request, Preflight Request와 달리 Access-Control-Allow-Credentials 헤더를 반드시 포함해야 한다.
    - 와일드카드 '*' 는 사용할 수 없고, 구체적인 Origin 값을 지정해야 한다.

