CORS(Cross-Origin Resource Sharing)는 다른 출처의 자원을 공유할 수 있도록 하는 보안 체제이다.

*출처란 ?*
![](https://i.imgur.com/R4mJ2dF.png)
위의 구성요소 중에서 **Protocol + Host + Port** 3가지가 같으면 동일 출처(Origin)라고 한다.


| 동일 출처 예시                                                                 |                                                     |
| ------------------------------------------------------------------------ | --------------------------------------------------- |
| http://Example.com:80<br>http://example.com                              | HTTP 기본 Port인 80번이 생략되어있으므로 동일 출처이다.                |
| http://example.com/app1/index.html<br>http://example.com/app2/index.html | Protocol, Host, Port(생략)이 같으며, Path부터 다르므로 동일 출처이다. |

| 다른 출처 예시                                                                                         |                     |
| ------------------------------------------------------------------------------------------------ | ------------------- |
| http://example.com/app1  <br>https://example.com/app2                                            | Protocol이 다릅니다      |
| http://example.com<br>http://www.example.com<br>http://myapp.example.com                         | Host가 다릅니다          |
| [http://example.com](http://example.com/)<br>[http://example.com:8080](http://example.com:8080/) | 80, 8080으로 포트가 다릅니다 |