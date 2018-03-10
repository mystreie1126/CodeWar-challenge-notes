# css-notes-1

### 1.`linear-gradient()` takes direction and color paramenters:
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
:coffee:**NOTE:**

*Because **`linear-gradient()`** belong to the **`image`** data type, they can only be used where images can be used. For this reason, **`linear-gradient()`** won't work on **background-color** and other properties that use the **`color`** data type*

Normally use at:
```
background-image: linear-gradient(),ulr(image.jpg);
//or background: linear-gradient();
```
So `color:linear-gradient()` won't work

:coffee:**text gradient color recipe:**

```
background:linear-gradient();  //bg color as gradient effect
color:tranparent;              //text color totally transparented to its background
-webkit-background-clip:text; //clip the background to its container the text
```

:coffee:**-webkit-background-clip**:

default as `-webkit-background-clip: border-box`, won't work using `background-clip` only...

but also as know as `-webkit-background-clip: content-box`,

`-webkit-background-clip: padding-box` and` z-webkit-background-clip: text`.


### 2.`background-size`main property includes [contain and cover](https://www.w3schools.com/cssref/css3_pr_background-size.asp)
```
*the contain is make sure the image is fully visible in the container*
*the cover will resize the background image to cover the entire container, even if it has to stretch the image or cut a little bit off one of the edges*
```

### 3.`background-position` [set the starting position of a background image](https://www.w3schools.com/cssref/pr_background-position.asp).
```
background-position:top // will stick the background on the top whatever the screen resize
```

### 4.`clip-path` property defines which part should be display and which part should be cut off,normally handy to use an online clip-path generator [tool](https://bennettfeely.com/clippy/)


### 5.`transform:translate(-50%,-50%)` technique to center an div content regarding its parent elements.
```
.parent{
  position:relative;
}
.child{
  position:absolute;
  transform:translate(-50%,-50%)
}
```
### 6.:question: `backface-visibility` [details](https://developer.mozilla.org/en-US/docs/Web/CSS/backface-visibility)

### 7. `:link` and `:visited` sudo class
`a:link` represents the element states which not been vistited, `a:visited`shows the state of elements already visited

### 8. `text-align:center` work with `display:inline` and `display:inline-block` elements, `divs`will work like text when they have`inline-block` properties.

### 9. `box-shadow` [details](https://markusstange.wordpress.com/2009/02/15/fun-with-box-shadows/)

### 10. sudo class vs sudo elements: sudo class are known as: `:hover`,`:active`. sudo elements are:`::before`,`::first-line`
*sudo elements lets you style a specific part of that element(s). sudo class changes the elements state*

