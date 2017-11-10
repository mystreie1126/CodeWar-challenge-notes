# JsNotes
**this is bold text**

**1.forEach() is a shorthand version compare with for loop, but be careful**
```	myArr = [1,2,3];
	myArr.forEach(function(elements,index,array){
    	// loop 3 times.....
	});```
  
**	2. convert binary number to decimal numbers, the most straight forward solutions is using paraseInt(binary, 2) **
	 ```var arr = [0,0,1,1];```
	 >arr to binary is :
	``` parseInt(arr.join(""), 2); ```
	**  3. apply() method to convert an array object into parameters... **
	 >finding the biggest number in the array.
	 ```Math.max.apply(null,myArr); // return 3;```
	 **4. Date.parase() returns the number of milliseconds**
	 ```var d = Date.parse("March 21, 2012"); ```
   >return 1332288000000
