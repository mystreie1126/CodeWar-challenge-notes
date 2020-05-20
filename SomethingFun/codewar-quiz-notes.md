JsNote
=========

1. `forEach()` is a shorthand version compare with `for` loop,sample code as:
```
myArr= [1,2,3];
myArr.forEach(function(elements,index,array){
     	//loop 3 times.....
});
```
2. convert binary number to decimal numbers, the most straight forward solutions is using `paraseInt(binary, 2)`,sample code  as: 
```
var arr = [0,0,1,1];
parseInt(arr.join(""), 2);
```

3. Normally when using `Math()`methods like Math.Max(),the parameters can't be an array, but with using `apply()`method can convert array into parameters, sample code:

```
var myArr = [1,2,3,4];
Math.max.apply(null,myArr); //return 4
```

4. `Date.parase()` returns the number of milliseconds
```
var d = Date.parse("March 21, 2012"); // return 1332288000000
```

5. Apply `Array.filter()`functions is a short hand of filter value from an array. code sample as:
```
var arr = [1,2,3]
var myArr = arr.filter(function(elements,index,array){
   return elements == 2; 
});
//myArr = [2];
```

6. Use `Array.filter()` also can remove the duplicated items from an Array.
```
var str = [a,a,a,b,c];
var str1 = str.filter(function(e,i,a){
  return str.indexOf(e) == i;
});
//str1 = [a,b,c];
```
:coffee: same value shared same `str.indexOf(e)` value

7. Point free style and merge array 

```
let calc = (x)=> x*2;
let a = [1,2,3].map(calc); // return [2,4,6] 
let b = [1,2,3].every(Array.isArray) // check every element is array which return false 

let arr1 = [1,2,3], arr2 = [4,5,6];
Array.prototype.push.apply(arr1,arr2) // return arr1 = [1,2,3,4,5,6];
```

8. `for` loop in another way: 

```
num = 20;
for(let i = 0; num > 9; i++){
  num -= 2;
		console.log(`i: ${i}, num: ${num}`);
	}
```

Looping when `num>9` is true, breaks the sterotype `for(i=0;i<n;i++)` looping. 



