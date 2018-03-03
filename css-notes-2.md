
# css/sass-notes-2

1.`em`, `%`(percentage), and `rem` units can be used on set font size or length.

*when setting `em` on font-size or length, its value **both depends on its parent's font-size***

*when setting `rem` on font-size or length, its value **both depends on the root font-size(default as 16px)***

*when setting `%` on font-size or length, the font-size value depends on its parent's **font-size**, the length value depends on its parent's **width***


2.:question: `transform` property changes default `z-index` value and the stacking content defination which are not solved yet. Original question at [here](https://stackoverflow.com/questions/49064186/does-css-transform-changes-the-z-index-property?noredirect=1#comment85135673_49064186)

:coffee:
**Attempt 1: tracking down css properties value with JavaScript using `getComputedStyle()`and`getPropertyValue()`
`getComputedStyle()` returns an object *report* that contains all the css values in the target element**. 
for example:
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
