# thymleaf 반복문

단순반복시

```
<li th:each="num: ${#numbers.sequence(1,5)}">
```

Model에서 넘어온 값

```
    <tr th:each="user : ${userList}">
        <td th:text="${user.id}"></td>
        <td th:text="${user.name}"></td>
    </tr>
```

&#x20;
