# Angular

### Installation
- First install nodejs into your system to use npm module.
- Installation of cli module (Angular)
    **`npm install -g @angular/cli`**

### Creating Your First Angular App
 - **`ng new my-app`**

### Running Your Default Template
1. First bring your terminal to the current directory by 
- `cd foldername/foldername`
2. To run our Angular-App 
- `ng serve`

3. To run and open your app in browser 
- `ng serve --open` OR `ng serve --o`

### Important Angular CLI Commands

- **`npm install -g @angular/cli`** - To install angular cli in your system globally.

- **`ng new my-Angular-App`** - To Create new project in angular

- **`ng serve`** - To run your ANGULAR application.

- **`ng help`** - It will provide us the some angular basic CLI commands which are necessary.

- **`"ng generate component newComponent" Shortform :- ("ng g c newComponent")`** - It will create new component in our angular project.

- **`"ng generate module newComponent" Shortform :- ("ng g m newComponent")`** - It will create new Module in our angular project.

- **`"ng genrate class newclass"`** - It creates class for us with 2 files 1.classname.ts & 2.classname.spec.ts

- **`"ng build"`** - it will create our application for the production and it will create the dist folder in your directory and it we can run our application on the serve by putting that folder on the server.


### Angular File Structure

**In Angular we get bunch of files like node_modules,src,angular.json,package.json,tsconfig.json etc** 

**But we need to focus on src folder which contains all the working files in the angular**

**In src folder you will get:** 

Global Files : 

- **index.html** -  which will be single page file and 

- **style.css** - for global styling of the files

- **main.ts** - which will contain all the global typeScript code. 

In `src/app` folder App-Files : 

- **app.component.html** - Which will contain HTML code for the main app component which is included in **index.html**

- **app.component.css** - Which will contain CSS code for the main app.

- **app.component.ts** - Which will contain TypeScript code for the main app.

- **app.component.ts** - Which will contain TypeScript code for the main app.

- **app.component.spec.ts** - Which will contain TypeScript code for the testing of the app.

- **app-routing.module.ts** - Which will contain TypeScript code for the routing of the main app.

### Using js/ts code inside the HTML (Interpolation)

We can execute ts code inside the HTML inside **{{title}}**
We can use the interpolation for the class and all the attributes as well.

Which things we can't use inside the interpolation : 
- `title="newBlog"` we cant assign any value to the varibale.

- We can't use typeof, Increment(`num++`), Decrement(`num--`), **New** Keyword.


### Angular Components

It will create component all 4 files in components folder.
 
 **`ng generate component 
 foldername/component-name`**

In the default files component.html will contain only code will be `<p>Component works</p>`

We dont need to import the each and every component inside our **app.component.ts** file like react or other frameworks.

1.  **Types of Component**

    1. **inline-style component** - 
     
        we can genrate inline-style component by command **`ng generate component myComponent --inline-style`** in which we can skip css file and we can add css in **component.ts** file where url's are declared inside the [`.class{color:red}`].

    2. **inline-template component** - 
    
        we can genrate inline-template component by command **`ng generate component myComponent --inline-template`** in which we can skip HTMl file and we can add HTML in **component.ts** file where url's are declared inside the **[`<h1>This is the header</h1>`]**.

    3. **inline-style and inline-template component** - 

        we can genrate inline-style and inline-template component by command **`ng genrate component myComponent --inline-style --inline-template`** in which we can skip both HTML and CSS file and and we can write HTML&CSS in **component.ts** file.

2.  **Loading-Component In APP**

    To load the component in the **app.component.html** we need to use it like HTML tag **<app-component></app-component>** and component will be automatically loaded inside our app. 

3. Taking or using Input in the component

    If we want to use attributes to the component tag like **`<app-component text="Add" ></app-component>`**

    - First we need to initialize the input in the component.ts file 
        ```
        import {Input} from '@angular/core'
        @Input() text:string;
        ```
    - Then we can use that variable inside the component's html file for the value and then we can pass it value by attribute in **app.component.html** as like mentioned below.
    ```
    // Button Component Ts
    <button 
    [ngStyle]="{'background-color': color, color:fontcolor}"
    class="btn"
    (click)="onclick()"
    >{{text}}</button>

    // App Component Ts
    <app-button color="purple" text="Add" fontcolor="white"></app-button>
    ```

4. **Inline CSS in Components**

    For that we need to use ngdirective to use inline styline as mentioned below : 

    **[ngStyle] = "{'property-property':'value'/variable,property:'value'}"**


### Modules in Angular
Modules are the group of components or a complete functionality like **user-authentication** in which it can contain login,register,forgotpwd,etc.

Modules are not reusable but components containing inside a model we can use that components.

1. **How to genrate module** 

    We can generate module by using command  **`ng generate module user-auth`** in which we get only 1 file in folder ***user-auth.module.ts***.

    In ***user-auth.module.ts*** file it will have some imports,declarations in which in ***imports:[CommonModule]*** contains the module names and ***declarations:[log-in]*** it will contain components declarations.

2. **How to generate component in module**

    We can genrate component in module by using command **`ng generate component folderName/componentName`**

    BUT

    when we create component in some module it will declare inside ***created module*** not in ***app.module.ts*** 

3. **For using that component created inside any module**
    
    As We know...
    when we create component in some module it will declare inside ***created module*** not in ***app.module.ts*** 

    soo.. 

    We need to register that component inside the ***app.module.ts*** file and then we can use it.

4. **How to register module in app.component.ts**

    First of all we need to import that module like **`import {UserAuthModule} from './user-auth/user-auth.module'`** and we need to register that module in the **imports:[UserAuthModule]**.

5. **Using that component inside the app anywhere**

    If we use the component it will throw an error bcoz angular doesn't know the component exists.

    SOO... 
    
    We need to export that component to the angular app by **exports:[LoginComponent]** below the imports and then the component is globally available in your angular app.

### Functions in Angular

The most important point in functions in angular is we are declaring functions inside the class as we know angular is class based framework soo we dont need to use **function** keyword while declaring the function and let,var and all while declaring the variables.

EX: 
```
getName(name:string,name2:string)
{
    console.log(name)
    console.log(name2)
}
```
In the angular before 11 we didn't got errors or we was not compulsed to define the data types but in the angular 12 strict mode is on soo we need to use the datatypes as per typescript in angular 12.


### Styling in Angular
**Types of Styling in Angular** : 

- **global styling** - which we do in style.css and which is applicable to all elements we styled in global styling.

- **external styling** - which we do in component.css file.

- **Internal styling** - which we do inside the component.html file in `<style></style>` tag.

- **inline style** - which we do in inline element in basic style attribute.

###  If-Else Statements in Angular (*ngIf)

*ngIf is the functionality of the angular in which we can check the conditino inside the component.html page in html attribute `<p *ngIf=true>Visible</p>`.

it will show the element onlyif condition will true.

Types of If-Else Statements - 

- **Simple if statement** : 

    **`<h1 *ngIf="true">This is a heading</h1>`**


    in this statement the element will be visible on the screen when the condition will be true.

- **IF statement with varibale** : 


    **`<h1 *ngIf="showStatus">This is a  heading</h1>`** 

    in this statement **showStatus** can be a variable or condition in the **component.ts** file it will be visible when that variable or function will be true.

- **if with else statement(ng-template)** - 
    ```
    <p *ngIF="showStatus else elseblock"></p>
    <ng-template #elseblock>
    <p>That paragraph tag is not visible.</p>
    </ng-template>
    ``` 
    in this statement if showStatus will be true it will execute own p block else it will execute elseblock.

- **if else block with both ng-template** -     
    ```
    <p *ngIf= "showcondition; then ifblock else elseblock"></p>

    <ng-template #elseblock><h1>Else Condition.</h1></ng-template>

    <ng-template #ifblock><h1>If Condition</h1></ng-template>
    ``` 
in this statement we will give **;** to the showStatus and we will put keyword **then ifblock else elseblock**.

- **else-if in Angular** - In Angular we dont have elseif soo we need to use **[ngIf]="color=='red'"** multiple times.


- **if else block with both ng-template with checking strings or values** -
    ```
    <p *ngIf= "showcondition=='shiv'; then ifblock else elseblock"></p>
    <ng-template #elseblock><h1>Else Condition.</h1></ng-template>
    <ng-template #ifblock><h1>If Condition</h1></ng-template>
    ```
    in this statement we are checking the value of **showCondition=='shiv'** **then ifblock else elseblock** it  will check the value fo showCondition if it will true it will execute if block else it will execute else block.


### IF else statement with [ngIF] attribute - 

- **For case if with else, we can use **ngIf** and **ngIfElse**.** : 
    ```
    <ng-template [ngIf]="condition" [ngIfElse]="elseBlock">
    Content to render when condition is true.
    </ng-template>

    <ng-template #elseBlock>
    Content to render when condition is false.
    </ng-template>
    ```
- **For case if with then, we can use ngIf and ngIfThen**. : 

    ```
    <ng-template [ngIf]="condition" [ngIfThen]="thenBlock">
    This content is never showing</ng-template>
    
    <ng-template #thenBlock>
    Content to render when condition is true.
    </ng-template>
    ```
- **For case if with then and else, we can use ngIf, ngIfThen, and ngIfElse.** : 
    ```
    <ng-template [ngIf]="condition" [ngIfThen]="thenBlock" [ngIfElse]="elseBlock">
  This content is never showing</ng-template>
    
    <ng-template #thenBlock>
    Content to render when condition is true.
    </ng-template>

    <ng-template #elseBlock>
    Content to render when condition is false.
    </ng-template>
    ```

### Switch Case in Angular

We use **switch case** when we have multiple condition more than 3-4 then we usually use the switchcase.
ex : - Days of week(7),Months of year(12)

In angular we have attributes which are usefull for the switchcase as followed : 
- **[ngSwitch]** - It will create a switchcase its a initialization of switchcase.

- **[ngSwitchCase]** - We can use this on the case.

- **[ngSwitchDefault]** - We can use this on the default case.

Uses of all the attributes are mentioned below : 
```
<div [ngSwitch]="color">
  <h1 *ngSwitchCase=" 'red' " style="color: red;">red color</h1>
  
  <h1 *ngSwitchCase=" 'green' " style="color: green;">green color</h1>

  <h1 *ngSwitchCase=" 'yellow' " style="color: yellow;">yellow color</h1>

  <h1 *ngSwitchCase=" 'purple' " style="color: purple;">purple color</h1>
  
  <h1 *ngSwitchCase=" 'orange' " style="color: orange;">orange color</h1>

  <h1 *ngSwitchDefault style="color: black;">Default color</h1>
</div>
```

### Loops in Angular (*ngFor)

ngFor* is the functionality of the angular which we can use inside the HTML as like for loop as mentioned below.

**Simple For loop over an array** : 

In the code mentioned below we just initialized an array in **component.ts** file and we are itrating over that an array are we are printing the values in the h1 tag as mentioned below.
```
//array specified in .ts file.
names ={"sam","mad","ron","shiv"}

//How to run a for loop on the array and print its value inside the HTML.
<h1 *ngFor = "let item of names"> The username is : {{item}}</h1>
```

**For loop on array of objects** :

In the code mentioned below we just initialized an array of objects in **component.ts** file and we are itrating over that an objects of array
and accessing the values of that objects and we are printing the values in the p tag as mentioned below.

```
//Array mentioned in component.ts file

users=[
    {name:'shiv',password:'shiv@123'},
    {name:'raj',password:'raj@123'},
    {name:'dan',password:'dan@123'},
    {name:'john',password:'john@123'},
    {name:'doe',password:'doe@123'}
  ]

<div *ngFor="let user of users">
  <hr>
  <p>Username : {{user.name}}</p>
  <p>Password:{{user.password}}</p>
</div>
```

**Nested For loop on array of objects** :

In the code mentioned below we just initialized an array of objects in **component.ts** file and we are itrating over that an objects of array
and accessing the values of that objects and the array of the object value as well and we are printing the values in the p tag as mentioned below.

```
//Array mentioned in component.ts file 

 users=[
    {name:'shiv',password:'shiv@123',socialprofiles:['gmail','linkedin','twitter']},
    {name:'raj',password:'raj@123',socialprofiles:['youtube','linkedin','twitter']},
    {name:'dan',password:'dan@123',socialprofiles:['tinder','linkedin','twitter']},
    {name:'john',password:'john@123',socialprofiles:['happen','linkedin','twitter']},
    {name:'doe',password:'doe@123',socialprofiles:['omg','linkedin','twitter']}
  ]

<div *ngFor="let user of users">
  <hr>
  <p>Username : {{user.name}}</p>
  <p>Password:{{user.password}}</p>
    <h3>Social Pofiles : </h3>
    <p *ngFor="let profile of user.socialprofiles"> <li> {{profile}}</li></p>
</div>
```

Here we are just using **let item of user.socialprofiles** for nested array thats it not the rocket science in that.

### Style Binding
We can use style binding for dyamic styling like if we want to give the styling like colors and all from our component.ts file then we use style binding.'

We need to use the style binding **`<h1 [style.color]="fontColor" >Heading Tag 1</h1>`** rather than **`<h1 style="color:white" >Heading Tag 1</h1>`**.

Ex:
```
// Variables from the component.ts file.
fontColor = "teal"
backgroundColor=""
  bgc(){
    this.backgroundColor="teal"
    this.fontColor = "white"
  }

// component.html
<div>
  <h1 [style.color]="fontColor" [style.backgroundColor]="backgroundColor">Heading Tag 1</h1>
  <button (click)="bgc()">Chage the background-Color</button>
</div>
```

### Toggle Button or Events in Angular

Toggle event is the event which toggles some opration like to show or hide a content as mentioned below : 

```
// TypeScript Code
 display = false
  toggle(){
    this.display=!this.display
  }

// HTML Code
<h1 *ngIf="display">Heading</h1>
<button (click)="toggle()" class="btn btn-primary">Toggle Button</button>
```
**!this.display** - called negation in angular which makes the opposite of current state.

### Adding Bootstrap with single line of command : 

- **npm install bootstrap** - it will install bootstrap in your node modules.
- Then you need to add the bootstrap styling and js path to to the **build** array in angular.json.

- For CSS - **"./node_modules/bootstrap/dist/css/bootstrap.min.css"**
- For JS - **"./node_modules/bootstrap/dist/js/bootstrap.js"**

### 2 way binding in Angular

In angular 2 way binding update the properties realtime and display them without reloading.

For 2 way binding we need to use **[(ngModel)]** for binding the properties.

- First we need to import **FormsModule** from **'.@angular/forms'** and we need to initialize it in the imports.

- then we need to create an property with which we want to bind the input value with it. 

- Simply just display that property in required tag like **{{value}}**.

```
// app.html
    <div class="container my-5 p-5 border w-25">
    <h3>Two Way binding in angular</h3>
    <input type="text" class="form-control my-4" [(ngModel)]="inputValue">
    <h5>{{inputValue}}</h5>
    </div>
// app.ts
    inputValue:any;
```

### Template refrence Variable

Template refrence variable nothing different than providing the id to the input field like **#inputBox**.

And After that we can acess its each and every value like name,placeholder,class,value and soo on.

```
// app.html
<div class="container my-5 p-5 border w-25">
    <h3>Template refrence variable</h3>
    <input type="text" class="form-control my-4" #inputBox>
    <button class="btn btn-sm btn-primary" (click)="getVal(inputBox.value)">Get the value</button>
    
    <h5>{{value}}</h5>
</div>

// app.ts
 value:string=""
  getVal(item:HTMLInputElement)
  {
    console.warn(item);
    this.value=item
  }
```

### Basic Pipes in Angular
Pipes are those things in angular which is used to update or modify the strings dates and all with very easy easy rather than normal.

We can use the basic pipes for strings as mentioned below - 
Ex :
```

<h1>{{title | uppercase}}</h1>

<h1>{{title | lowercase}}</h1>
```

We can use the basic pipes for dates as mentioned below - 
Ex:
```
<h2>{{today | date}}</h2>

<h2>{{today | date : "fullDate"}}</h2>
```

### Advance Pipes

**Pipes for strings**
How to pass parameters to the pipes and use the multiple pipes on the single element as mentioned below- 
Ex:
```
<h1>{{title | slice : 1 : 21 | uppercase}}</h1>
```
For multiple parameters or passing parameters we use **":"** and for multiple pipes we use **"|"**.

**Pipes for objects**
For printing the full array data which we can't print with just putting **{{userDetails}}** we can use the pipe **json** as mentioned below.

```
<h2>{{userDetails | json | uppercase}}</h2>
```
**Pipes for Numbers**
In the numbers pipes we can pass the parameters like how much values to show before points and after points like **2.2-3** it means that before point show 2 values and after point show 2 or max 3 values as like mentioned below. - 

```
<h3>{{0000223.564000 | number : '2.3'}}</h3>
```
**Pipes for currency**
We can show currency symbol before our value in numbers by just using currency pipe and passing value to it as per our requirement of symbol.

```
<h3>{{3 | currency : 'USD'}}</h3>
```
We can pass the all currency values like USD,GBP,INR soo on. 

### Making Custom pipe in Angular

Command For Creating custom pipe in angular - **`ng g p pipes/customPipe`**

Always create your pipes in specific folder and keep it organized.

After creating pipe you will get 2 files only which will be **component.ts** and **spec.ts** and our work will be totally in .ts file.

- **How to call that custom pipe** - 

As mentioned below you will get the name of pipe and you need to use that name in your pipe.
```
// pipe.ts
@Pipe({
  name: 'usdInr'
})
```

```
@Pipe({
  name: 'usdInr'
})
export class UsdInrPipe implements PipeTransform {

  transform(value: number, ...args: number[]): unknown {
    const[x]= args;  
    return value*x;
  }

}
```
- By default that return value is set to be null so you need to make it as value so it will print the value.

- **How to pass arguements to custom pipes** - 

    1. As mentioned above we can pass the arguement to the pipe like normal **pipe : arg**.

    2. That passed arguement will be come in **..args array**
    which is `...args: number[]`.
    3. You need to take the arguement value by using const or let and we are multiplied the value with the value.
    ```
    const[x]= args;  
    return value*x;
    ```

### Angular Forms

Angular forms are different than others as like mentioned below.


**<u>Most imp in the angular forms we cannot connect angular with the databases like SQL,MongoDB etc like others.Rather than that we need to connect with the database with the help of api in angular.We call the API's throught the forms and API automatically send data to database.</u>**

**Types of forms**
- Template Driven Form :- In template driven forms most of the work will complete in the HTML file only like form,data,validation etc.

- Reactive Form :-  In reactive forms most of the work will complete in the TypeScript file only like form,data,validation etc.

1. **Template Driven Form** - 








































<!--### Custom attribute in Angular
Custom attribute is nothing but the we are taking input from the user and for that we need to use the **@Input** which we need to import from angular core and we can initialize the custom attribute as menioned.

```
import {Input} from {@angular/core}
@Input todo: string;
```

### Angular Events
In Angular Events we dont need to create function we need to create method which will be created as mentioned below.

```
<button class="btn btn-danger btn-sm my-3" (click)="todoDelete()">Delete</button>

todoDelete(){
    console.log("Todo Deleted");
  }
```

### Events Emitter in Angular

Event emitter is used to mostly handle the events in between components.
Like we send the event to the parent component and it will be processed over there. 


### Events in Angular

We specify the event type inside the brakcet and the functions for that inside the semicolon as like mentioned below.

`<button (click)="onClick()"></button>`

### Creating Custom Event in Angular

Import the Ouput and EventEmitter as mentioned below.

And we need to initialize the our custome event in component.ts file like 
```
import { Component, OnInit,Input, Output,EventEmitter} from '@angular/core';
@Output() btnClick = new EventEmitter
```
In the **button.component.ts** we need to add 

```
   onclick(){
    // console.log('Button Clicked');
    this.btnClick.emit(); 
}
``` 
And we need to keep that `(click)="onclick()"` event on the button.component.html file in button tag.

Then we can use that custom event in the **header.component.ts** in the `**<app-button (btnclick)="toggleAddtext()"></app-button>**` and we need to declare that functino in main **app.component.ts** file.

Basically in the **button.component.html** file we can use the function which declared in the **that.component.ts** file and it further follows for each and every component. -->
