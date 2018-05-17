# CSS flex-box notes 

### 1. `flex-basis`vs`width` deatails at [here](https://stackoverflow.com/questions/34352140/what-are-the-differences-between-flex-basis-and-width)

content –> width –> flex-basis (limited by max|min-width) 

### 2. `align-items` vs `align-content` details at [here](https://stackoverflow.com/questions/27539262/whats-the-difference-between-align-content-and-align-items)

### 3. `flex-box` not only can be applied into child elements, but also can be applied to its child contents

```
<span>text</span>
span{display:flex; justify-content:center}
```
the `text` content sit in the center of its container 


