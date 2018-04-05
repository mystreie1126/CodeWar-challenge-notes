# Sass-notes-1(04-04)

### 1.Solid color gradient with `linear-gradient()`

```
 background-image:linear-gradient(
  100deg,
  blue 20%,red 20%
  )
```
which means at 20% it is blue color, after 20% will be red, if ` blue 20%,red 30%` the 20% to 30% will be the red to blue gradient


### 2.Styling the `input` tag

**2.1 Styling the placeholder text **
```
<input type="text" placeholder="check this out">
input{color:red}
```
The `color:red` above will only affect the type field text within the input box.

`input::-webkit-input-placeholder{color:inhert; font-family:inherit;}`

But using **`::-webkit-input-placeholder`** to styling the placeholder text which is **only work in safari and chrome**
sudo element selected with `**::**` are oftern represent things in the browser.

**2.2 the font proeprties of the `input` tag and its placeholder text which are stand-alone and won't inherit from parent**

`input{color:inherit; font-family:inherit} //inherit from its parent `
`input::-webkit-input-placeholder{font-size:inherit} //inherit nothing `

**2.3 Normally when styling focus on the `input` tag, the `outline`will set to none, but for the accessbility usage, the input field has to be *focus visible*, by adding more visible feature:**
```
input:focus{
            outline:none;
            box-shadow: 0 1rem 2rem rgba($color-black,.2); 
            border-bottom: 3px solid red;
    }
```

**2.4 `:invalid` CSS pseudo-class represents any `input` or other `form` element whose contents fail to validate, and the `require` attributes in `input` tag represents  specifies that an input field must be filled out before submitting the form**

```
<input type="email" required>
input:invalid{color:red}
```

**2.5 `:placeholder-shown` selects the input element itself when placeholder text exists in a form input, it shows the state of the `input` when nothing has been typed yet.**


### 3. CSS combinators 

```
<section>
  <div class="test1 test">test1
      <h3>some text</h3>
  </div>   
  <div class="test2 test">test2</div>
  <div class="test3 test">test3</div>
  <div class="test3 test">test4</div>
</section>
```
**`section:hover > .test`** which select all the `test` class which are the **child** of `section` tag

**`section:hover h3`** which select the **Descendant** of the `section` tag

**`section:hover*` selects all the child within the `section` included the `h3`**

**`section:hover > *`** selects all the direct child which is only the `.test` class here.

**`.test:hover ~ .test`** which select the following child(s) who has class name `.test` 

**`.test:hover + .test`** which select the next following child who has class name `.test` 


### 4. `visibility:hidden` vs `opacity:0` vs `display:none`

**Property** | **take up space** |**consume click**|
-----------------|--------|--------|
**`visibility:hidden`**|Yes|No|
**`opacity:0`**|Yes|Yes|
**`display:none`**|No|No|


