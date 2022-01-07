# 인터페이스

일반클래스는 new 연산자를 이용해 인스턴스를 생성할 수 있지만, 추상클래스는 인스턴스를 생성할 수 없고, 오직 상속을 통한 자식클래스를 구현한 후에  인스턴스를 생성할 수 있다.

```
abstract class 클래스이름{
    // 필드
    // 생성자
    // 메소
} 
```



```
abstract class Shape {
    double pi = 3.14; -> 추상클래스도 멤버 필드를 포함할 수 있다.    
    
    abstract void draw(); -> 추상메서드는 본체가 없다.  
    
    public double findArea() { -> 추상클래스도 구현메소드를 포함할 수 있다.   
        return 0.0;
    }
}
```



인터페이스

java.lang -> CharSequence, Comparable, Runnable

java.util -> Collection, Comparator, List

```
interface 인터페이스이름{
  // 상수필드
  // 추상메서드
  // 디폴트메소드
  // 정적메서드
  // 비공개메서
 } 
```

