# 배열



**동일한 자료형(Data Type)의 데이터를 연속된 공간에 저장하기 위한 자료구조**

연관된 데이터를 저장하기 위한 **변수의 선언을 줄여**주며, **반복문 등을 이용하여 계산과 같은 과정을 쉽게 처리**할 수 있다.

```jsx
자료형[] 변수 = {데이터1, 데이터2, 데이터3, ... };
```

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d53ebbbe-3afc-48cd-95ee-0b294b73dd81/Untitled.png)

미리 알고 있는 값으로 배열

```jsx
int[] odds = {1, 3, 5, 7}; // or 
int[] evens = new int[]{2, 4, 6, 8};
```

2차원배열

```jsx
int[][]scores = new int[2][3]; int k = 0; 
for(int i = 0; i < scores.length; i++) { 
	for(int j = 0; j < scores[i].length; j++) { 
	scores[i][j] = k++; 
} 
System.out.println(Arrays.toString(scores[i]));
```
