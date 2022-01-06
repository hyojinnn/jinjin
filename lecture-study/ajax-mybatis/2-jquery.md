# 2 jquery



JQuery를 이용하면 브라우저 호환성을 고려하지 않아도 편하게 ajax를 사용할 수 있다.

```jsx
$('#sendServer').click(function(){
			
	const name = $('#param').val();
	
	$.ajax({
		url:"/chap02/jquery",
		data: { name : name },
		method: "GET",
		success: function(data, textStatus, xhr){
			$('#result').text(data);
			console.log(textStatus);
			console.log(xhr);
		},
		error: function(xhr, status, error){
			console.log(xhr);
			console.log(status);
			console.log(error);
		}
	});
});
```
