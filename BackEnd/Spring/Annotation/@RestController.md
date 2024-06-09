`@RestController` : `@Controller`와 `@ResponseBody`를 결합한 형태로, 메서드의 반환 값이 뷰 이름이 아니라 HTTP 응답 본문으로 직접 쓰여지는 컨트롤러, JSON 또는 XML 같은 형식으로 데이터를 반환하는 데 주로 사용된다.

- `@RestController`는 Spring 에서 RESTful 웹 서비스를 쉽게 만들 수 있도록 지원한다.
- 메서드의 반환 값이 JSON 또는 XML 형식으로 자동 변환된다.
- 경로 변수, 요청 매개변수, 요청 본문 등을 쉽게 처리할 수 있다.

[[@Controller]]
[[@ResponseBody]]
