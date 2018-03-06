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


### 3. In Sass,naming variables inside `calc()` function has to use `#{}`on the target varibale, this is called as [interpolate](https://github.com/sass/sass/issues/818):

```
$width = 100px;
calc(100% - #{$width});
```

### 4. Sass re-use ultility classes:
The ultility classes re-used for achieve a simple or some specific purposes, such as by adding the `text-align:center` to its child elements:
```
//adding .center-text class
<div class='center-text'>
  <p>some text</p>
</div>
```

the `center-text` class are resued within the `_utilities.scss` file:
```
.center-text:{text-align:center}
```
### 5. `@import` in sass and partial files:

In Sass, it always using underscore to naming the partial files like `_partial.scss`. The underscore lets Sass know that the file is only a partial file and that it should not be generated into a CSS file.

to import partial files as: **`@import foldername/partial`**  as the underscore and file extension name is not required.

