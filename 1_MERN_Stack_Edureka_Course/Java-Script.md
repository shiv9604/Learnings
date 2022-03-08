# Java-Script

javaScript is scripting language made for interpretate the some logic at the browser side soo reduce the traffic to the server for the small small task and to reduce the run time of the website.

### Variables in the javaScript

We declare the variables in the javascript with the keyword "var".

**Ways to declare the variables in the javascript** -

1. var =

### Data Types in JavaScript

There are 2 types of datatypes in javascript.

- **Premetive** - Those datatypes are the root datatypes of the languauge which stores in the stack in memory.

- **Non-Premetive** - Derived data types which get stored in the Heap space.

**Premetive Data types** : -

1. string = "" written in this symbol which are basically the alphabates.

2. number = 12 normally written in the numeric values.

3. Boolean = these data types only contains only 2 values like true and false which are conditional data types.

4. Undefined = Undefiend represents variable declaration but the value is undefined.

5. NULL = Null represents no value at all.

**Non-Premetive Data Types** : -

1. array = ["a",b,c] combination of data types grouped together to store in single variable is called as array.

2. Object = {key:value} Object are basically the key value pair in which we can store the data related to real world like the details of the person and all together.

3. Regular Expression = Represents regualr expression.

### Functions in the javaScript

If we need to repeat any functionality again and again in the certain task or project you just group that functionality in a block make it dynamic soo it will be worked in the same logic but in the different situations.

We declare function as mentioned below :

```
function thisFunc(){
    // Code
    return code;
}
```

The function declaration is done with the keyword **"function"** and **thisfunc** is the name associated with the function and and in the **(parameters)** we pass the parameters which we going to use inside the function.

The return written in the function returns the value to the function but whenever the return keyword is used we need to assign the function to the variable or we need to do the **console.log(function)** then only we can get the result.

### Scope in javaScript

There are 2 types of scope in the javascript as followed :

- **Global Scope** -
  Global scope is in which our variables will get stored in our memory and we can use them throughout the code.

- **Local or Block Scope** -
  Local scope is the block scope in which the variables will not get stored in the memory they will be limited to its **scope {}** like they will be temp variable just to perform the functionality and it will be accesible in that blocks only or inside the function.

### String Concatination in the javascript

We can concat the strings in the javascript with the many ways but we most usable is with console.log("string",var) and with the **"" + ""**.

### Incremental and decremental oprators in the javascript

1. **Pre and Post increment oprators**

- ++value :- It will increment the value first and then print

- value++ :- It will print the value first and then it will print it.

2. **Pre and Post increment oprators**

- ++value :- It will increment the value first and then print

- value++ :- It will print the value first and then it will print it.

### Arithmatic Oprators in the javaScript

- **+** :- Additional oprators used for addition and concatination.

- **-** :- Substraction oprator used for substraction.

- **"*"** :- Multiplication oprator used for multiplication.

- **/** :- Divide oprator used for divisional oprations.

- **%** :- Its modulus oprator which gives us the remainder of the division.

### Assignment oprators

- **=** :- This is the assignment oprator in the javascript which assigns the values to the variables or else.

- **+=** :- This oprators add the asasigned value to the variable.

- **-=** :- This oprators substracts the assigned value to the variable.

- ***=**  :- This oprators Mutiplies the assigned value to the variable.

- **/=**  :- This oprators divides the assigned value to the variable.

### Ternary Oprators in the javascript

`condition ? true : false`

Ternary oprators which have 3 values in it thats why its called as ternary oprator and its used to do the small comparison based on true false statements.

**We can use it single line if else statements**

Ex : `a>6 ? console.log(true) : console.log(false)` = It will returns true.

### Logical and comparision oprators in the javascript
	
- `==`	**Equal to** :- true if the operands are equal.


    Ex : 	5==5; //true
 
- `!=`	**Not equal to** :- true if the operands are not equal	

    Ex: 5!=5; // false
 
- `===`	**Strict equal to** : -  true if the operands are equal and of the same - type	

    Ex : 5==='5'; //false
 
- `!==`	**Strict not equal to** :- true if the operands are equal but of  different type or not equal at all	

    Ex : 5!=='5'; //true
 
- `">"`	**Greater than** :- true if the left operand is greater than the  right operand	

    Ex : 3>2; //true
 
- `>=`	**Greater than or equal to** :- true if the left operand is greater - than or equal to the right operand	

    Ex : 3>=3; //true
 
- `<`	**Less than** :- true if the left operand is less than the right - operand	

    Ex : 3<2; //false
 
- `<=`	**Less than or equal to** :- true if the left operand is less than or equal to the right operand	
    
    Ex : 2<=2; //true

### Conditional (and, or, not) oprator

- `&&` :- And oprator used to check the mutiple true conditions in if else statements.

- `||` :- Or oprator used to check the at least one true conditions in if else statements.

- `!` :- Not oprator is used to inverse the output of the statement.

### If else statments in the javascript

If else statements in the javascript is used to check the conditions in our code and what we want to execute if some specific condition get executed and if not then what to execute as like mentioned below.

Ex :
```
let name = "shiv";
if(name=="shiv"){
    conosle.log("this is the right person")
} 
else{
    conosle.log("this is not the right person")
}
``` 
In the above example we are checking the name and executing the right code if it will be true and what if it will be false.

### Ways of outputs in the javascript

1. **Console Output**  - We can get the output in the console by  using conosle methods like `conosle.log("hi there")`.

2. **Document Output** - We can get the output on our webpage by using document methods like `document.write("hi there")`.

3. **Alert** - We can get output in the alert as which appers on the webpage on the top like a pop up by using methods `alert("hi there")`.

4. **Dynamic content on the webpage (innerHTML)** - We can show the dynamic data on the website in the perticular element as well through the javascript by using the `document.getElementById("")`


### Inputs of outputs in the javascript

1. **Window Input** - We can take window input from the alert by using ` let output = window.prompt("Enter the name : ")`.

2. **HTML Form** - We can take input by using HTML form and by using `input.value` and this is the best and ideal way to take input from the user in the feild of web developement.
 

### Arrays in javascript
1. **How to acess the values of array** :- In the arrays we can acess the values of array by its own index in the array.
```
var hobbies = ["reading","swiming"]
console.log(hobbies[0]) // It wil return the reading.
```

2. **Array Properteis** - 

    1. `arr.length` - return the length of the array.

    2. `arr.concat(anotherArray)` - It will concat the array on which the method is called.

3. **Array methods** - 
    
    1. `arr.push()` - It will push the value in the array at the end of the array.

    2. `arr.pop()` - It will remove the last element of the array.

    3. `arr.toString()` - It will convert the arry with its specific index in a single string.

    4. `arr.find(()=>{})` - The find() method returns the first element in the provided array that satisfies the provided testing function. If no values satisfy the testing function, undefined is returned.

    5. `arr.filter(()=>{})` - It creates a new array which pass the conditions like mentioned below.
        ```
        let arr = [10,11,22,45,65,87,231,12]

        let mature = arr.filter(res=>{
            return res>=18 
        })
        console.log(arr)
        console.log(mature)
        ```
    6. `arr.map(()=>{})` - It can create the new array by applying modificatinos to it soo too fetch the already available data we use the filter and if we wanna update the data and return it to new array we need to use the map function.
        ```
        let arr = [10,11,22,45,65,87,231,12]

        let agesUpdatedFilter = arr.filter(res=> res+5)
        let agesUpdatedMap = arr.map(res=> res+5)

        console.log(agesUpdatedFilter) // It will return the new array as it is bcoz we cant update the existing the values in the filter method.
        console.log(agesUpdatedMap)// It will return the new array with addition of 5.        
        ```
    7. `arr.sort((a,b)=>a-b)` - It will sort the numerical values and we can use the plain sort function for the alphabetical sorting.
        ```
        let arr = [10,11,22,45,65,87,231,12]

        let sorted = arr.sort((a,b)=>a-b)

        console.log(sorted) // [10, 11, 12, 22,45, 65, 87, 231]

        ```
    
    8. `arr.reverse` - It will reverses the values of the arry.
        
    9.  `arr.slice(start,end)` - It will return a new array with the sliced elements without affecting the orignal array.


### Objects in javascript


### Classes in the javascript
Classes are the real world things or objects which holds their properties and their functionalities calles as methods are called as objects.

We can declare a class by using the below syntax : 
```
class Employee{
    constructor(name,salary){
        // properties
        this.name = name, 
        this.salary = salary
    }

    // Methods
    greet(){
        console.log("Good Morning",this.name)
    }
}
```
- we declare the classes with the keyword `class`.

- `constructor(){}` is the things which assign the external values to the class dynamically by using keyword `this` keyword to the obj whos its property of.

-  When we write the function in the class we dont need to use the keyword `function` we can decalre the methods like `greet () {conosle.log(name)}`.


