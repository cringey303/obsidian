1. ```
<!doctype html>
<html>
	<head>
		<meta charset="utf-8">
	</head>
	<body>
		<p id="line1"></p>
		<p id="line2"></p>
		<button type="button" onclick="changeText()">
			Change Text
		</button>
			<script>
				function changeText(){
				var element = document.getElementById("line1");
				element.innerHTML = "Hello";
				element = document.getElementById("line2");
				element.innerHTML = "World!";
}
</script>
</body>
</html>
   ```