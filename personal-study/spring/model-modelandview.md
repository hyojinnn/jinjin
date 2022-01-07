# model modelandview

**Model**은 **파라미터 방식**으로 메소드에 **(Model model) 파라미터**를 넣어주고 **String형태로 리턴**한다

Model은 **값을 넣을 때 addAttribute()를 사용**

\


**ModelAndView**는 **컴포넌트 방식**으로 **ModelAndView 객체를 생성**해서 **객체형태로 리턴**한다

MoelAndView는 말그대로 Model과 View를 합쳐놓은 것으로,

**값을 넣을때 addObject()를 사용**하고, **setViewName()**으로 보낼 곳 **View**를 세팅한다

\


\


\* ModelAndView는 @Controller를 이용하기 전부터 사용했지만, Spirng MVC가 @Controller annotation을

지원하기 시작한 이후로 **ModelAndView는 잘사용하지 않는다고 함.**

