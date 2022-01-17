# ROWNUM

ROWNUM 이란?

SELECT로 조회해온 테이블에 일련번호를 붙이는것.



SELECT절에 의해 추출되는 데이터(ROW)에 붙는 순번이다. 다시 말해 WHERE절까지 만족 시킨 자료에 1부터 붙는 순번이다.

WHERE절에 ROWNUM을 이용하여 조건을 주면 다른 조건을 만족시킨 결과에 대해 조건이 반영된다.



**ROWNUM을 올바로 사용하기 위해서는?**

ROWNUM을 사용한 곳에 ORDER BY를 사용하면 안된다

ORDER BY를 사용해야 한다면

서브쿼리 안에 사용할 것 &#x20;
