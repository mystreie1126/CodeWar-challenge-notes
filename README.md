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






