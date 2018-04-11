# Sass-notes(04-07)

### 1. radio button and check boxes can not be styled with CSS directly, normally to hide the `input` and styling it ajacent `label` element

```
 <input type="radio" class="form__radio-input" id="large"  name="radio-group">
  <label for="large" class="form__radio-label">
       <span class="form__radio-button"></span>   //empty span to styling the radio button
      large tour group
  </label>
 
 
 .form__radio-input:checked ~ .form__radio-label form__radio-button{opacity: 1} 
 ```
 
