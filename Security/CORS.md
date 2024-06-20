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

