# Sass-notes-1

### 1.Sass attribute selector 

If there is need to style a part of the elements within the tag, there can use `[]` selector to style all of them:

```
[class^="col"]{
   background-color:red; 
} 
```
**`[class^="col"]`** means any class name start with `col` will be selected, Also:

**`[class$="col"]`** means any class name end with 'col' will be selcted, Also:

**`[class*="col"]`** means any class name contains 'col' will be selected.


### 2.`not()` sudo elements: 

```
.col{
   &:not(:last-child){
            margin-right:20px;
        }
}
```
This selects every child from `col`class except the last-child.

### 3. `calc()` function with `#{}` :question:
