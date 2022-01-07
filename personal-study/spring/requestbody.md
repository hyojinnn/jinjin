# requestbody

스프링에서 비동기 처리를 하는 경우 @RequestBody , @ResponseBody를 사용한다.\
\
클라이언트에서 서버로 통신하는 메시지를 요청(request) 메시지라고 하며, 서버에서 클라이언트로 통신하는 메시지를 응답(response) 메시지라고 한다.\
비동기통신을 하기위해서는 클라이언트에서 서버로 요청 메세지를 보낼 때, 본문에 데이터를 담아서 보내야 하고, 서버에서 클라이언트로 응답을 보낼때에도 본문에 데이터를 담아서 보내야 한다.&#x20;

**이 본문이 바로 body 이다.**

**즉, 요청본문 requestBody, 응답본문 responseBody 을 담아서 보내야 한다.**&#x20;

\
\
@RequestBody를 통해서 자바객체로 conversion을 하는데, 이때 HttpMessageConverter를 사용한다.&#x20;

@ResponseBody 가 붙은 파라미터에는 HTTP 요청의 분문 body 부분이 그대로 전달된다.

**@RequestBody**&#x20;

이 어노테이션이 붙은 파라미터에는 http요청의 본문(body)이 그대로 전달된다.

**일반적인 GET/POST의 요청 파라미터라면 @RequestBody를 사용할 일이 없을 것이다.**

**반면에 xml이나 json기반의 메시지를 사용하는 요청의 경우에 이 방법이 매우 유용하다.**

HTTP 요청의 바디내용을 통째로 자바객체로 변환해서 매핑된 메소드 파라미터로 전달해준다.

