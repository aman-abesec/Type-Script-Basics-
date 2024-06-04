# Type-Script-Basics


<details>
<summary>Data Type</summary>
<br>
  
```ts
let firstName: string = 'Aman';
let lastName: string = 'Singh';
let age: number = 22;
let isValideVoter: boolean=true;
console.log(firstName + lastName);

//When you doesn't define type then it add type any. You can avoide by adding flag noImplicitAny
let notDefined;
notDefined=10;
console.log(notDefined)
```
</details>

<details>
<summary>Function</summary>
<br>
  
```ts
  function isValidVoter(age:number = 18) {
    return age>18?true:false;
}
console.log(isValidVoter(22))

//Define type you are returning
function fullName(firstName: string,lastName:string, age:number) : string{
    return `Full name is ${firstName} ${lastName} Age is ${age}`;
}

console.log(fullName(firstName,lastName,age))

const isEven = (num : number) : boolean=>{
    return num %2 ===0;
}
console.log(isEven(8))


//Here void telling you are returning nothings
function errorMsg(str : string):void{
    console.error(errorMsg);
}

//Some function never return a value
function error(msg : string):never{
    throw new Error(msg);
}
  ```
</details>
