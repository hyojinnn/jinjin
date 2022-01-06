# 반복문



반복문의 종류

while, do\~while, for문

while, do\~while → 반복할 횟수는 모르지만, 조건을 알 때

for문 → 반복할 횟수를 알 때 사용

while문

```jsx
int i=0 //도와주는 변수 선언 
while(i<10){ //괄호 안에 조건 넣어주기 
   i++ //도와주는 변수 업데이트
}
```

while문 무한루프

```
while(true){
   //무한루프
}
```

do\~while문

```
do{
   System.out.println("안녕하세요"); //실행할 구문
}while(false); //조건 검사
```

for문

```
for(int i=0 ; i<10 ; i++) {
   //조건이 참일 경우 for문 내부 실행
}
```

* int i = 0 //나를 도와주는 변수 정의
* i<10 //조건
* i++ //나를 도와주는 변수 업데이트

무한루프를 탈출하려면, if 문으로 특정조건을 걸어주면 된다.

break; 를 해주면 루프문을 종료시켜준다.

중첩for문

```jsx
for(int i=0;i<10;i++) {
	for(int j=0;j<10;j++) {
		System.out.print(j); //실행할 구문 
	}
}
```
