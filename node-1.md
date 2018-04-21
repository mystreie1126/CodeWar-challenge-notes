## NodeJs study notes


#### **1.calling `fs` module for create files:**
```
const fs = require('fs');
fs.appendFile('name of the file', 'content of the file',(errorCallback)=>{
  console.log(errorCallback);
});
```

read file:
```
let read = fs.readFileSync('db.json'); //read a json file
let obj = JSON.parse(read);
```
**`fs.readFileSync()`** returns everything in the file as string 

write to file:
```
fs.writeFileSync('db.json');
```
when **`fs.readFileSync()`** and **`fs.writeFileSync()`** dealing with files, the return value for both 
are strings

#### **2.npm package:nodemon are commonly used on server:**

