## DOM manipulation notes 1


#### **1.`getComputedStyle()`and`getPropertyValue()`**

tracking down css properties value with JavaScript using `getComputedStyle()`and`getPropertyValue()`,`getComputedStyle()` returns an object *report* that contains all the css values in the target element. 

**for example:below create an object-like report for all the css properties within the div tag**
```
let div_style = window.getComputedStyle(document.querySelector(div));

```
**And it also can track the sudo elements:**
```
let div_sudo_style = window.getComputedStyle(document.querySelector(div),':after');
//':after' is the second optional parameter when used this function, normally as known as sudo elements such :after or :before.
```
To get the exactly value from the css report object by using `getPropertyValue()`,for example:
```
let div_bg_style = window.getComputedStyle(document.querySelector(div)).getPropertyValue('background-color');
```


### **2.DOM selection**

#### **2.1 `children` vs `childNodes`**
children refer to all the `html`tags which are the elements </br> but `childNodes` include text between each tags which is given default by browser.
to clear the `text` childnode we can just write html tag next to another. 


#### **2.2 `createElement` and `createTextNode`**

To insert an element into the body, should be create element first and adding textnode inside,then updated to the body

```
let p = document.createElement('p');

var textNode = document.createTextNode('a new paragraph');

p.appendChild(textNode);

document.body.appendChild(p);

```

#### **2.3 access silbings and `firstChild`**

Silbings are the elements within the same parent. to access by using **`nextElementSibling`**

```
<ul>
  <li>test1</li>
  <li>test2</li>
</ul>

let silbing = document.querySelector('li'); // test1

**silbing.nextElementSibling;** //test2

let ul = document.querySelector('ul');

**ul.firstChild;** // return to 'text' because space between `<ul>`and first'<li>`tag
**ul.firstElementChild** //return test1 

sibling.parentNode; // return `ul` tag

```



