`@Controller` : 특정 클래스를 컨트롤러로 지정하고, 이 클래스 내의 메서드들을 웹 요청 처리 메서드로 정의할 수 있다.

- `@Controller`는 Spring 에서 웹 요청을 처리하고, 뷰를 반환하는 클래스에 사용된다.
- 모델 객체를 통해 뷰에 데이터를 전달할 수 있으며, 다양한 요청 처리 메서드를 정의할 수 있다.
- `@RestController`는 RESTful 웹 서비스에서 JSON/XML 형식의 응답을 쉽게 처리할 수 있게 해준다.

[[@RestController]] - @Controller와 @ResponseBody를 결합한 어노테이션