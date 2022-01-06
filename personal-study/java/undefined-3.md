# 상속

자식 클래스는 부모 클래스로부터 확장된다는 의미로 extends 키워드를 사용해 상속상태를 선언

```jsx
부모클래스
class SuperClass {
	// 필드
	// 메소드
}

자식클래스
class SubClass extends SuperCLass {
	// 필드
	// 메소드
}
```

부모 클래스의 private 멤버를 제외한 모든 멤버는 자식 클래스에 상속된다.

생성자는 클래스 멤버가 아니기 때문에 상속되지 않는다.
