![[Screenshot 2026-02-04 at 11.06.58.png]]
1. ```
<!DOCTYPE html> 
<html lang="en">
<body>
<h2>JavaScript Arrays</h2>
<p>Compute the sum of the rounded numbers in an array.</p>
<p id="demo"></p>
<script>
const numbers = [15.5, 2.3, 1.1, 4.7];
document.getElementById("demo").innerHTML = numbers.reduce(getSum, 0);
function getSum(total, num) {
	return total + Math.round(num);
}
</script>
</body>
</html>
   ```