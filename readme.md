# What is Scope in Jaca Script?
## Scope in JavaScript is the area where a variable or a function exists and is accessible. It determines the visibility and lifetime of a variable or a function in your code. There are three main types of scope in JavaScript: global, local, and block scope.  (Module scope)
 ***(Область видимости в JavaScript — это область, в которой существует и доступна переменная или функция. Он определяет видимость и время жизни переменной или функции в вашем коде. В JavaScript существует три основных типа области видимости: глобальная, локальная и блочная.)***

 * <span style="color:yellowgreen;">__Global scope:__</span>
 The default scope for all code running in script mode.

 * <span style="color:red;">__Function scope:__</span> The scope created with a function.
  
  * <span style="color:#006FBE;">Block scope: </span>This scope restricts the variable that is declared

 ## Global scope: Variables or functions declared outside any function or block are global. They can be accessed and modified from anywhere in the code. Global variables are created when the script starts and deleted when the script ends.

 #### ___(Глобальная область: переменные или функции, объявленные вне любой функции или блока, являются глобальными. К ним можно получить доступ и изменить их из любого места кода. Глобальные переменные создаются при запуске скрипта и удаляются при его завершении.)___

 ___

 ## Function scope: Variables or functions declared inside a function are local to that function. They can only be accessed and modified within that function. Local variables are created when the function starts and deleted when the function ends.

 #### ___(Область действия функции: переменные или функции, объявленные внутри функции, являются локальными для этой функции. Доступ к ним и их изменение можно получить только внутри этой функции. Локальные переменные создаются при запуске функции и удаляются при ее завершении.)___

 ___

 ## Block scope: Variables declared with the keywords `let` or `const` inside a `{}` block are block-scoped. They can only be accessed and modified within that block. Block-scoped variables are created when the block starts and deleted when the block ends. 

 #### ___(Область действия блока: переменные, объявленные с ключевыми словами `let` или `const` внутри блока `{}`, имеют область действия блока. Доступ к ним и их изменение можно получить только внутри этого блока. Переменные в области блока создаются при запуске блока и удаляются при его завершении.)___

 ___

# Block Scope

 ## Variables declared inside a { } block cannot be accessed from outside the block:

 ### Example:
 ```
 {
  let x = 2;
}
// x can NOT be used here
```
## Variables declared with the <span style="color:red;">`var`</span> keyword can NOT have block scope.  Variables declared inside a `{ }` block can be accessed from outside the block.

### Example:
```
{
  var x = 2;
}
// x CAN be used here 
```

# Local Scope
## Variables declared within a JavaScript function, are <span style="color:red;">`LOCAL`</span> to the function:

### Example:
```
// code here can NOT use carName

function myFunction() {
  let carName = "Volvo";
  // code here CAN use carName
}

// code here can NOT use carName
```

## `Local` variables have `Function Scope:` They can only be accessed from within the function.

### Since local variables are only recognized inside their functions, variables with the same name can be used in different functions. Local variables are created when a function starts, and deleted when the function is completed.

#### ___(Поскольку локальные переменные распознаются только внутри своих функций, переменные с одинаковыми именами можно использовать в разных функциях. Локальные переменные создаются при запуске функции и удаляются при ее завершении.)___

___

# Function Scope
## JavaScript has function scope: Each function creates a new scope. Variables defined inside a function are not accessible (visible) from outside the function.

#### ___(В JavaScript есть область действия функции: каждая функция создает новую область действия. Переменные, определенные внутри функции, недоступны (видимы) снаружи функции.)___

## Variables declared with <span style="color:red;">`var`</span>, <span style="color:red;">`let`</span> and <span style="color:red;">`const`</span> are quite similar when declared inside a function.

#### ___(Переменные, объявленные с помощью `var`, `let` и `const`, очень похожи, если они объявлены внутри функции.)___



## They all have Function Scope:

```
function myFunction() {
  var carName = "Volvo";   // Function Scope
}
```

```
function myFunction() {
  let carName = "Volvo";   // Function Scope
}
```

```
function myFunction() {
  const carName = "Volvo";   // Function Scope
}
```
```
function myFunction() {
  const carName = "Volvo";   // Function Scope
}
```

# Global JavaScript Variables
## A variable declared outside a function, becomes <span style="color:red;">`GLOBAL.`</span>

### Example:
```
let carName = "Volvo";
// code here can use carName

function myFunction() {
// code here can also use carName
}
```

## A global variable has Global Scope: All scripts and functions on a web page can access it. 



