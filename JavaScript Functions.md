![[Screenshot 2026-02-02 at 11.04.40.png]]

1. 
	1. 2
	2. 2
2. ```
   function countChar(string, ch) { // initialize function
		let counted=0; // create the counter variable
		for (let i = 0; i < string.length; i++) { // start for loop to loop through the string
			if (string[i] == ch) { // check if the current char is the 
				counted += 1;
			}
		}
		return counted;
   }
   
   function countEs(string) {
		return countChar(string, "E");
   }
   ```