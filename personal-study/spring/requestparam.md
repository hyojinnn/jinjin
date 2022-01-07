# requestParam

**@RequestParam**

* 단일 HTTP 요청 파라미터의 값을 메소드 파라미터에 넣어주는 어노테이션
* 가져올 요청 파라미터의 이름을 @RequestParam 어노테애션의 기본 값으로 지정해주면 됨
* 요청 파라미터의 값은 메소드 파라미터의 타입에 따라 적절히 변환 됨
* **해당 파라미터가 반드시 존재**해야하며, 없으면 HTTP 400 - Bad Request 발생
* 파라미터를 필수가 아니라 선택적으로 제공하게 하려면 required 엘리먼트를 false로 설정할 것

**@RequestParam을 이용하여 form 데이터를 Controller로 받기**

* Controller에서 @RequestParam 어노테이션을 이용하면 Http 요청의 데이터를 메소드 파라미터로 받을 수 있음.
* jsp의 **html 태그에 name으로 지정한 값으로 매칭**되는 방식
* 이 외의 파라미터 맵핑 방식 :: @RequestHeader, @RequestBody 등
