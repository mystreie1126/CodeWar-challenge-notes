# css/sass-notes
1.`linear-gradient()` takes direction and color paramenters:
```
background:linear-gradient(blue,red); 
//default as blue on top, red on bottom
```
*which is same as:*
```
background:linear-gradient(180deg,blue,red);
//180deg as increasing, the blue color will turns right, red turns left
```
*and also it normally can combine with gradient property with image, such as:*
```
background:linear-gradient(to right,blue,red),url(some_img.jpg);
```


2.`background-size`main property includes [contain and cover](https://www.w3schools.com/cssref/css3_pr_background-size.asp)
```
*the contain is make sure the image is fully visible in the container*
*the cover will resize the background image to cover the entire container, even if it has to stretch the image or cut a little bit off one of the edges*
```

3.`background-position` [set the starting position of a background image](https://www.w3schools.com/cssref/pr_background-position.asp).
```
background-position:top // will stick the background on the top whatever the screen resize
```

4.`clip-path` property defines which part should be display and which part should be cut off,normally handy to use an online clip-path generator [tool](https://bennettfeely.com/clippy/)


5.`transform:translate(-50%,-50%)` technique to center an div content regarding its parent elements.
```
.parent{
  position:relative;
}
.child{
  position:absolute;
  transform:translate(-50%,-50%)
}
```
