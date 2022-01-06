# mybatis-2. Scope



```jsx
public static SqlSession getSqlSession() {
		
	if(sqlSessionFactory == null) {
		String resource = "com/greedy/section01/xmlconfig/mybatis-config.xml";
		
		try {
			InputStream inputStream = Resources.getResourceAsStream(resource);
			sqlSessionFactory = new SqlSessionFactoryBuilder().build(inputStream);
		} catch (IOException e) {
			e.printStackTrace();
		}
	}
	
	/*
	 *  sqlSession은 요청 시 마다 생성해야 한다.
	 */
	SqlSession sqlSession = sqlSessionFactory.openSession(false);
	
	System.out.println("sqlSessionFactory의 hashCode() : " + sqlSessionFactory.hashCode());
	System.out.println("sqlSession의 hashCode() :" + sqlSession.hashCode());
	
	return sqlSession;
}
```
