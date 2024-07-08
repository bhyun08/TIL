### 프로그래밍 오류의 종류
프로그램에서 오류가 발생하면 시스템 레벨에서 프로그램에 문제를 야기하여 원치 않는 버그를 일으키거나, 심각하면 실행 중인 프로그램을 강제로 종료시키도 한다. 프로그램 오류의 원인으로는 다양한 상황이 있다.

1. 논리 에러 (Logic Error)
   - 프로그램이 실행되지만 의도한 대로 동작하지 않는 경우이다.
   - 논리적 오류는 컴퓨터 입장에서 에러가 발생하지 않은것 이기 때문에 에러 메시지를 알려주지 않는다. 따라서 개발자는 프로그램의 전반적인 코드와 알고리즘을 체크 필요가 있다.
2. 컴파일 에러 (Compillation Error)
   - 컴파일 단계에서 발생하는 문법 오류이다.
   - 컴파일 에러 발생의 대표적인 원인으로 문법 구문 오류(syntax error)가 있다.
3. 런타임 에러
   - 프로그램 실행 중 발생하는 오류이다.
   - 대체로 개발 시 설계 미숙(논리적)으로 발생하는 에러가 대부분이며, 런타임 에러 발생 시 프로그래머가 역추적해서 원인 확인해야 한다. 
### 오류(Error)와 예외(Exception)

![Runtime Error](https://blog.kakaocdn.net/dn/daaSR8/btrMxEiWv6g/GTFbMlkhgtjAi4izITeKg0/img.png)

자바 프로그래밍에서는 실행 시(runtime) 발생할 수 있는 오류를 '**에러(error)**'와 '**예외(exception)**' 두가지로 구분 하였다. 오류(Error)와 예외(exception)클래스는 모두 Throwable 클래스를 상속받고 Throwable 클래스는 Object 클래스를 상속 받는다.

- 에러(error) : 프로그램 코드에 의해서 수습될 수 없는 심각한 오류
- 예외(exception) : 프로그램 코드에 의해서 수습될 수 있는 다소 미약한 오류

따라서 개발자는 예외 처리(exception handling)를 통해 언제나예외 상황을 처리하여 프로그램이 종료되는 일이 없록 코드의 흐름을 바꿀 필요가 있다.
### 자바의 예외(Exception) 클래스
##### 예외 클래스 계층 구조
자바에서는 오류를 Error와 Exception으로 나누었고 이들을 클래스로 구현하여 처리하도록 하였다. 우리에게 익숙한 IllegalArgumentException을 비롯해 NullPointerException과 IOException도 모두 클래스이다.   
JVM은 프로그램을 실행하는 도중에 예외가 발생하면 해당 예외 클래스로 객체를 생성하고서 예외 처리 코드에서 예외 객체를 이용할 수 있도록 해준다.

![Language/Java](https://blog.kakaocdn.net/dn/c2FA9K/btrMC0ghD9Q/aYBYxY27KrQwASlBbbzyPk/img.png)

**Error 클래스**는 위에서 언급한 바와 같이 외부적인 요인으로 인해 발생하는 오류이기 때문에 개발자가 대처 할 수는 없다. 따라서 우리가 처리할 수 있는 클래스는 바로 **Exception 클래스**이다.
##### 런타임에러 vs 컴파일에러

![Language/Java](https://blog.kakaocdn.net/dn/pW5yl/btrMye5lmK3/5TkR8hcVZi9xFk3xFTjAKk/img.png)

Exception 클래스는 다시 RuntimeException(런타임 에러를 다룸)과 그 외의 자식 클래스 그룹(컴파일 에러를 다룸)으로 나뉘게 된다.
- Exception 및 하위 클래스 : 사용자의 실수와 같은 외적인 요인에 의해 발생하는 컴파일시 발생하는 예외
- RuntimeException 클래스 : 프로그래머의 실수로 발생하는 예외
##### Checked Exception vs Unchecked Exception

![Checked Exception / Unchecked Exception](https://blog.kakaocdn.net/dn/MThfh/btrRtcbb2Xl/zR5vUkvvJNLOPo7kXhkQHK/img.png)

자바의 예외(Exception)는 컴파일 에러와 런타임 에러로 구분된다. 그런데 또다시 예외는 예외의 종류로서 Checked Exception 과 Unchecked Exception 으로 나뉜다.
이는 Checked Exception은 컴파일 예외클래스들을 가리키는 것이고, Unchecked Exception은 런타임 예외클래스들을 가리키는 것으로 보면 된다.

checked Exception은 반드시 예외를 처리해야하고, Unchecked Exception은 명시적인 처리를 하지 않아도 된다.

[[예외 처리]]



