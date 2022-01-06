# mybatis-1. DB접속 환경설정



DB 접속에 관한 환경 설정

JdbcTransactionFactory : 수동커밋

ManagedTransactionFactory : 자동 커밋

PooledDataSource : ConnectionPool 사용

UnpooledDataSource : ConnectionPool 미사용

```jsx
Environment environment =
				new Environment("dev" 
// 환경 정보 이름
						, new JdbcTransactionFactory() 
// 트렌잭션 매니저 종류 결정(JDBC or MANAGED)
						, new PooledDataSource(DRIVER, URL, USER, PASSWORD)); 
// ConnectionPool 사용여부(Pooled or UnPooled)
```

```jsx
/* 생성한 환경 설정 정보를 가지고 마이바티스 설정 객체 생성 */
		Configuration configuration = new Configuration(environment);

/* 설정 객체에 매퍼 등록 */
		configuration.addMapper(Mapper.class);
```

SqlSessionFactory : SqlSession 객체를 생성하기 위한 팩토리 역할을 수행하는 인터페이스

SqlSessionFactoryBuilder : SqlSessionFactory 인터페이스 타입의 하위 구현 객체를 생성하기 위한 별도의 역할 수행

build() : 설정에 대한 정보를 담고 있는 Configuration 타입의 객체 혹은 외부 설정 파일과 관련된 스트림을 매개변수로 전달하면 SqlSessionFactory 인터페이스 타입의 객체를 반환하는 메소드

```jsx
SqlSessionFactory sqlSessionFactory = new SqlSessionFactoryBuilder().build(configuration);
```

openSession() : SqlSession 인터페이스 타입의 객체를 반환하는 메소드

false : Connection인터페이스 타입의 객체로 DML 수행 후 auto commit에 대한 옵션을 false (권장)

true : Connection인터페이스 타입의 객체로 DML 수행 후 auto commit에 대한 옵션을 true

```jsx
SqlSession sqlSession = sqlSessionFactory.openSession(false);

/* getMapper() : Configuration에 등록된 매퍼를 동일 타입에 대해 반환하는 메소드 */
Mapper mapper = sqlSession.getMapper(Mapper.class);

/* Mapper 인터페이스에 작성된 메소드를 호출하여 쿼리 실행 */
java.util.Date date = mapper.selectSysdate();

System.out.println(date);

/* close() : SqlSession 객체 반납 */
sqlSession.close();
```

mybatis-config.xml

```jsx
<configuration>
	<environments default="dev">
		<environment id="dev">
			<!-- JDBC와 MANAGED 둘 중 하나 선택 가능 -->
			<transactionManager type="JDBC"/>
			
			<dataSource type="POOLED">
				<property name="driver" value="oracle.jdbc.driver.OracleDriver"/>
				<property name="url" value="jdbc:log4jdbc:oracle:thin:@localhost:1521:xe"/>
				<property name="username" value="C##GREEDY"/>
				<property name="password" value="GREEDY"/>
			</dataSource>
		</environment>
	</environments>
	
	<mappers>
		<mapper resource="com/greedy/section02/xmlconfig/mapper.xml"/>
	</mappers>
</configuration>
```
