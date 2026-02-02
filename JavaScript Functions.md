![[Screenshot 2026-02-02 at 11.04.40.png]]

1. 
	1. 2
	2. 2
2. ```
   function countChar(string, ch) { // initialize function
		let counted=0; // create the counter variable
		for (let i = 0; i < string.length; i++) { // start for loop to loop through the string
			if (string[i] == ch) { // check if the current char is the one we are counting
				counted += 1; // add one to the count if yes
			} // end if
		} // end for
		return counted; // return the amount of counted chars
   } // end function
   
   function countEs(string) { // initialize countEs func
		return countChar(string, "E"); // call countChar function for "E" and return it
   }
   ```
3. ```
   const countEs = countEs(string)
   ```