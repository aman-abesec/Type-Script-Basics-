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


<details>
<summary>Objects</summary>
<br>
  
```ts
const User ={
    name:'Aman',
    email:'xyz@gmail.com',
    isActive:true
}

function createUser({name: string,ispaid:boolean}){

}
createUser({name: 'Aman', ispaid:false})

function createCource():{name:string, price:number}{
    return {name:'B.tech', price:670}
}

//Odd Beavaiour
// createUser accept two object but three was given inside object
let obj={name:'Aman', ispaid:false,email:'xyyy@gmail.com'}
createUser(obj);
```
</details>

<details>
<summary>Aliases</summary>
<br>

```ts
type User={
    name:string;
    email:string;
    isActive:boolean;
}

function createUser(user : User) : void{
    console.log(user.name)
}
```
</details>

<details>
<summary>Read Only and Optional</summary>
<br>

```ts
type dbSchema = {
    readonly _id : number,
    firstName: string,
    lastName: string,
    mobNumber : number,
    isSuperAdmin ?: boolean //Here questmark telling its optional
}

let firstData:dbSchema = {_id:1234,firstName:'Aman',lastName:'Singh',mobNumber:89887668,isSuperAdmin:true}
let secondData:dbSchema = {_id:1235,firstName:'Akash',lastName:'Singh',mobNumber:8787887668}
console.log(firstData._id)

type cardNumber = {
    cardNumber : number
}

type cardDate = {
    cardDate : string
}

type cardDetails = cardNumber & cardDate & {
    cvv : number
}

let amCDetails : cardDetails = {cardDate : '12-01-2009',cardNumber:6787878,cvv:787}
console.log(amCDetails)
```
</details>

<details>
<summary>Array</summary>
<br>

```ts
const fruits : string[] = ['apple','mango','banana']
const num : Array<number> = [1,2,3,4,5]

type Point = {
    x:number,
    y:number
}

let allPoints : Point[] =[{x:9,y:89}]

let rgba: number[][] = [[0,0,0],[9,89,90]]

```
</details>
