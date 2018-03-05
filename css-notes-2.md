# CSS-notes-2


### 1.`em`, `%`(percentage), and `rem` units can be used on set font size or length.

*when setting `em` on font-size or length, its value **both depends on its parent's font-size***

*when setting `rem` on font-size or length, its value **both depends on the root font-size(default as 16px)***

*when setting `%` on font-size or length, the font-size value depends on its parent's **font-size**, the length value depends on its parent's **width***

:coffee:
**Note: When applying value with `letter-spacing` or `word-spacing`properties, try not using `%` as the 
measurment unit.And both properties are relative to its current font-size value**

### 2.:question: `transform` property changes default `z-index` value and the stacking content defination which are not solved yet. Original question at [here](https://stackoverflow.com/questions/49064186/does-css-transform-changes-the-z-index-property?noredirect=1#comment85135673_49064186)

:coffee:
**Attempt 1: tracking down css properties value with JavaScript using `getComputedStyle()`and`getPropertyValue()`,`getComputedStyle()` returns an object *report* that contains all the css values in the target element. 
for example:**
```
let div_style = window.getComputedStyle(document.querySelector(div));
//this will create an object-like report for all the css properties within the div tag
```
And it also can track the sudo elements:
```
let div_sudo_style = window.getComputedStyle(document.querySelector(div),':after');
//':after' is the second optional parameter when used this function, normally as known as sudo elements such :after or :before.
```
To get the exactly value from the css report object by using `getPropertyValue()`,for example:
```
let div_bg_style = window.getComputedStyle(document.querySelector(div)).getPropertyValue('background-color');
```
### 3.CSS inherit trick.
**`property:inherit`,most text related properties are all inherit by default, something like `margin` or `padding` are not:**
```
//giving box-sizing inherit property
*{
  box-sizing:inherit;
 }
body{
 box-sizing:border-box;
}
//now every box-sizing value are inherit with "border-box"
```

**common inherit practice:**
```
parent{
  font-size:20px;
  line-height:200%; //line-height is 40px
}
child{
  font-size:25px;  //as line-height is inherited, so this value in child is still 40px unless it was re-declared
}
```
### 4. `box-sizing:border-box`

Normally the default height and width of the element is padding+border+content

but with using `box-sizing:border-box`,the height and width of the element will be the content itself.

### 5. `inline-block` vs `block` vs `inline`

`iblock` | `inline-block`|`inline`|
-----------------|--------|--------|
100% parent width|occupy only content's space|occupy only content's space|
Vertically one after another|No line breaks|No line breaks,No height and widths and left and right paddings and margins|

### 6. when adding `float` property on the elements, the elements can be considered as inline-block elements. 

So when calling `float:left` on a group of box, is same as calling `display:inine-block`. And the `clearfix` is only useful when all the contained elements are floated, the clearfix recipe as:

```
tag::after{
  content:'';
  display:table;
  clear:both:}
```

