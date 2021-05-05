# Computer programming basics

​																																					--**Chenhang Wen**

## 1. Programming Language

### 1.1 Programming

Computer do as code which is written programmer.

### 1.2 Computer Language

machine language. 0 and 1

### 1.3 Programming Language

1. assembly language
2. high-level language

### 1.4 Compiler

Translate programming language to machine language.

## 2. Computer Basics

### 2.1 Computer Organization

1. hardware
   - input
   - output 
   - CPU
   - storage
   - memory
2. software
   - operation system: Windows, Linux
   - application: VScode, Word

### 2.2 Data Storage

1. Computer use binary system to express data.
2. Computer store data in binary system.

### 2.3 Units

- bit: 0 or 1
- Byte: 1B = 8 bit
- KB: 1KB = 1024 B
- MB: 1MB = 1024 KB
- GB: 1GB = 1024 MB
- TB: 1TB = 1024 GB

### 2.4 Programming Run

1. load code in storage to memory.
2. CPU execute order from memory.

# The Beginning of JavaScript

## 1 About JavaScript

### 1.1 History

Created by Brendan Eich in1995.

### 1.2 What is JavaScript

- A scripting language run in the client. 

### 1.3 The functions of JS

- Form Validation
- Web Effects
- Server Development (Node.js)
- Graphical User Interface (Electron)
- APP (Cordova)
- IOT (Ruff)
- Game Development (cocos2d-js)

### 1.4 The relationship of HTML/CSS/JS

- HTML/CSS: markup language -- descriptive langue
- JS: scripting language -- programming language

### 1.5 How browser run JS

- Rendering Engine: to parse HTML and CSS. for example, blink in chrome, or webkit.
- JS Engine: load JS code and execute. for example, V8 in chrome. Compile JS code to machine language. And JS code will be executed line by line.

### 1.6 The Constitutions of JS

![TheConstitutionsOfJS](\img\TheConstitutionsOfJS.png)

- ECMAScript: JS basics, JS syntax
  - ![ECMAScript](\img\ECMAScript.png)
- DOM, BOM: JS API
  - DOM (Document Object Model). Control elements (size, position, color) on the webpage.
  - BOM (Browser Object Model). For example, pop-up box, page skip.

### 1.7 Try to Write JS

#### JS has three places could write.

- Write inline

  - ```html
    <input type="button" value="submit" onclick="alert('submited successfully')">
    ```

- Write in <script></script>

  - ```html
    <script>alert('HELLO')</script>
    ```

- Write out of HTML

  - ```html
    <script src=""></script>
    <!--write .js path in src-->
    ```

#### JS comment

```javascript
//Single-Line comments

/*
	Multi-Line comments
*/
```

#### JS input/output

![inputoutput](\img\inputoutput.png)

```javascript
prompt('Tell me your age: ');
alert('Thank you!');
console.log('User told his/her age!')
```

# Variable

## 1 Variable Brief

### 1.1 What is variable

A named container of data. Use the name of container to get the data.

### 1.2 Variable in memory

- Variable applies for some pace to store data.
- Find the data by the name of variable.

## 2 How to use variable

Two steps: declare variable, assign

### 1.1 Declare variable

```javascript
//Decalre Variabal
var age; //decalre a variable named age
```

- var is one of the keywords in JS, means variable.

### 1.2 Assign

```javascript
age = 10; //assign 10 to age(variable)
```

- = means assign.

### 1.3 Variable initialization

```javascript
var age = 18; //decalre variable with assigning
```

### Example

requirements:

1. popup an input box: remind user to input name.
2. popup a dialog box: return the name user gave.

```javascript
var username = prompt('name: ');
alert(name);
```

## 3. Variable Syntax

### 1.1 Update variable

Variable can be assigned a new value, and previous value will be covered. Variable will keep value last time assigned.

```javascript
var age = 18;
console.log(age);
age = 81;
console.log(age);
```

### 1.2 Assign multi-variables at the same time

```javascript
var name = "Conan",
    age = 20,
    email = "xxx@gamil.com";
```

### 1.3 Special case

- Declare without assigning.

  - ```javascript
    var age;
    console.log(age) //-->undefined
    ```

- Without declaring and assigning.

  - ```javascript
    //use directly
    consle.log(age) //-->error
    ```

- Assign without declaring.

  - ```javascript
    age = 10;
    console.log(age) //-->10
    ```

## 4. Variable Naming Convention

![NamingConvention](\img\NamingConvention.png)

* Try not use 'name' to name a variable. Because the 'name' often has meaning or value in Browser.

# Data Type

## 1 Data Type Brief

Different data needs different size of space to storage.

### 1.1 Variable's data type

JS is weakly typed and dynamic language. It means you needn't declare variable in advance, the type of data will be determined while code is running.

```javascript
var x = 10; //x is int
var x = "10" //x became str now
// it will rise an error in other programming languages, like JAVA
```

### 1.2 Classification of data type

- **Simple data types** (Number, String, Boolean, Undefined, Null)

  - ![SimpleData Types](\img\SimpleData Types.png)

  - Number:

    - Octonary and Hexadecimal

      -  ```javascript
      var num1 = 012; //Octonary number system, add 0 before the number.
      var num2 = 0x9; //Hexadecimal, add 0x before the number.
    
    - MAX_VALUE and MIN_VALUE
    
      - ```javascript
        //the max value of Number
        console.log(Number.MAX_VALUE);
        //the min value of Number
        console.log(Number.MIN_VALUE);
        ```
      
    - Special value
    
      - ```javascript
        alert(Infinity); //Infinity
        alert(-Infinity); //-Infinity
        alert(NaN); //Not a number
        
        console.log(Number.MAX_VALUE * 2); //-->Infinity
        console.log(Number.MIN_VALUE * 2); //-->-Infinity
        console.log("123" - 100); //-->NaN
        ```
    
    - isNaN()
    
      - determine if a data is Number, if yes return false, else return true.
    
      - ```javascript
        console.log(isNaN(12)); //-->false
        conssole.log(isNaN("12")); //-->true
        ```
    
  - String

    - enclosed by "" or ''

    - escape character

      - ![EscapeCharacter](\img\EscapeCharacter.png)

    - .length

      - return the length of string.

      - ```javascript
        var str = "Hello";
        console.log(str.length); //--> 5
        ```

    - String Concatenation

      - ```javascript
        console.log("Hello " + "word"); //-->Hello word
        
        console.log("Hello " + 2021); //-->Hello 2021
        
        console.log(12 + 12); //-->24
        
        console.log("12" + 12); //-->1212
        ```

    - example

      - ```javascript
        //ask user's age and give a feedback
        var age = prompt('tell me your age: ');
        var str = "you are " + age + " years old";
        alert(str);
        ```

  - Boolean

    - Boolean has two values, true and false.

      - ```javascript
        var flag1 = true; // -->true
        var flag0 = true; //-->false
        ```

    - the number value of Boolean.

      - ```javascript
        //true is also regrarde as 1
        //false is also regrarde as 0
        
        console.log(flag1 + 1); -->2
        console.log(flag0 + 1); -->1
        ```

  - Undefined and Null

    - A variable is declared without assigning, it will be assigned Undefined or Null.

      - ```javascript
        var str;
        console.log(str);
        
        var variable = undefined;
        console.log(variable + "?"); //-->undefined?
        
        console.log(variable + 123); //-->NaN
        ```

      - ```javascript
        var space = null;
        
        console.log(space + "?"); //-->null?
        console.log(space + 1); //-->1
        ```

- **Complex data types** (Object)

- **Get the Type of Data**

  - typeof

    - ```javascript
      var num = 10;
      console.log(typeof num); //-->number
      
      var str = "Hello world";
      console.log(typeof str); //-->string
      
      var flag = true;
      console.log(typeof flag); //-->true
      
      var vari = undefined;
      console.log(typeof vari); //-->undefined
      
      var timer = null;
      console.log(typeof timer); //**-->object
      ```

- **Data type conversion**

  - Convert into String

    - ![TransformToString](\img\TransformToString.png)

    - ```javascript
      //convert number into string by .toString()
      var num = 10;
      var str = num.toString();
      console.log(str); //-->10
      console.log(typeof str); //-->String
      
      //convert number into string by String()
      console.log(String(num)); //-->10
      
      //convert number into string by +
      //also called implicit conversion
      console.log(num + ''); //-->10
      ```

  - Convert into Number

    - ![ConvertIntoNumber](\img\ConvertIntoNumber.png)

      - ```javascript
        //parseInt(String)
        var num = 18;
        console.log(parseInt(num)); //-->18
        console.log(parseInt('3.14')); //-->3
        console.log(parseInt('3.94')); //-->3 round down
        console.log(parseInt('120px')); //-->120 truncate the rest after the number
        
        //parseFloat(String)
        console.log(parseFloat('3.14')); //-->3.14
        
        //Number()
        var str = "123";
        console.log(Number(str)); //-->123
        
        // by - *
        //also called implicit conversion
        console.log('12' - 0); //-->12
        console.log('123' - '120'); //-->3
        console.log('123' * 1); //-->123
        ```

    - example

      - ```javascript
        /*
        calculate ages
        requirements:
        	1.popup a input box, ask user birth year.
        	2.calculate the ages and return it to user.
        */
        
        var year = prompt('tell me your birth year: ');
        var age = 2021 - year;
        alert('u r ' + age + 'years old.');
        ```

      - ```javascript
        /*
        add method
        requirements:
        	1.ask user two numbers.
        	2.add the two number and return it.
        */
        
        var num1 = prompt('tell me the first number: ');
        var num1 = prompt('tell me the second number: ');
        var result = parseFLoat(num1) + parseFLoat(num2);
        alert("the first number add the second number is " + result);
        ```
    
  - Convert to Booelan
  
    - Boolean()
      - ![ConvertToBoolean](\img\ConvertToBoolean.png)
### 1.3 Column

  Computer can't undestand other languages except machine language. So we need to translate other languages to machine languages. Conpiler is used to do this.

- Interpreted Languages and Compiled Languages
  - ![InterpretedLanguagesAndCompiledLanguages](\img\InterpretedLanguagesAndCompiledLanguages.png)
  - Interpreted Languages
    - the program is interpreted line by line when it is running. e.g. JavaScript
  - Compiled Languages
    - Compiled before run. generate intermediate code. e.g. Java and its intermediate code .class
- Identifier, Keyword, Reserved word
  - Identifier
    - The name that programmer gave variable, or filed, or function, or parameter.
  - Keyword
    - The words have been used by JS. We can't use it as the name of variable or something else.
    - e.g.: break, case, cath, continue, default, delete, do, else, finally, for, function, if, in, instanceof, new, return, switch, this, try, typeof, var, void, while, with and etc....
  - Reserved word
    - Also called keyword, means reserved keyword. It may be not a keyword now, but probably used later.
    - e.g.: boolean, bytr, char, class, const, debugger, double, enum, export, extends, fimal, float, goto, implements, import, int, interface, long, mative, package, private, protected, public, short, static, super, synchronized, throws, transient, volatile and etc...

  # JavaScript Operator

Operator is called 运算符 or 操作符. It is used to implement assigning, comparing, arithmetical operation.

## 1 Common Operator

- **arithmetical operation**

  - ![ArithmeticalOperation](\img\ArithmeticalOperation.png)

  - ```javascript
    // + add
    console.log(1 + 1); //-->2
    
    // - subtract
    console.log(1 - 1); //-->0
    
    // * multiply
    console.log(1 * 1); //-->1
    
    // / divide
    console.log(1 / 1); //-->1
    
    // % remainder
    console.lo g(5 % 3); //-->2
    ```

  - 不确定尾数 (Uncertain Mantissa ?)

    - Don't compare two float numbers direcrtly

    - ```javascript
      //for example
      console.log(0.1 + 0.2); //-->3.000000000000000004
      console.log(0.07 * 100); //-->7.000000000000001
      ```

- **Expression and Return Value**

  - Expression
    - Consist of number, operato, variable...
    - All expression will return value. e.g. 1 +1 return 2.

- **Increment Operator and Decrement Operator**

  - pre-increment / pre-decrement.

    - ++variable --variable

    - do add/substract operation before returned value

    - ```javascript
      var a = 10;
      console.log(++a + 10); //-->21
      console.log(a); //-->11
      ```

  - post-increment / post-decrement

    - variable++ variable--

    - do add/substract operation after returned value

    - ```javascript
      var a = 10;
      console.log(a++ + 10); //-->20
      console.log(a); //-->11
      ```

- **Comparison Operator**

  - ![ComparisonOperator](\img\ComparisonOperator.png)

  - Special Case

    - ```javascript
      // == could convert data type
      console.log(18 == "18"); //-->true
      
      // === and !== require two value are equal noy only in value but also in data type.
      console.log(18 === "18"); //-->false
      ```

- **Logical Operator**

  - ![LogicalOperator](\img\LogicalOperator.png)

  - and &&

    - return true only as both expression return true.

  - or ||

    - return ture if one of sides return ture or both true.

  - not !

    - return true when expression is false. and return false when expression true.

  - Short-circuit evaluation

    - >**Short-circuit evaluation**, **minimal evaluation**, or **McCarthy evaluation** (after [John McCarthy](https://en.wikipedia.org/wiki/John_McCarthy_(computer_scientist))) is the semantics of some [Boolean operators](https://en.wikipedia.org/wiki/Logical_connective) in some [programming languages](https://en.wikipedia.org/wiki/Programming_language) in which the second argument is executed or evaluated only if the first argument does not suffice to determine the value of the expression: when the first argument of the `AND` function evaluates to `false`, the overall value must be `false`; and when the first argument of the `OR` function evaluates to `true`, the overall value must be `true`.
      >
      >----'Short-circuit evaluation' Wikipedia (access 2021/05/02)

    - In &&

      - expression1 && expression2

      - if the first expression (expression1) is true, it will return the value of the second expression (expression2).

      - if the first expression (expression1) is false, it will return the value of the first expression (expression1).

      - ```javascript
        //example
        console.log(123 && 456); //-->456
        console.log(0 && 456); //-->0
        console.log(0 && (1+2) && (456*123)); //-->0
        ```

    - In ||

      - expression1 && expression2

      - if the first expression (expression1) is true, it will return the value of the first expression (expression1).

      - if the first expression (expression1) is false, it will return the value of the second expression (expression2).

      - ```javascript
        //exmaple
        console.log(123 || 456); //-->123
        console.log(123 || 456 || (456+123)); //-->123
        console.log(0 || 456 || (456+123)); //-->456
        ```

    - Special case

      - ```javascript
        //In this case, num++ will not be executed
        var num = 0;
        console.log(123 || num++); //-->123
        console.log(num); //-->0
        ```

  - Assigning Operator

    - ![AssigningOperator](\img\AssigningOperator.png)

    - ```javascript
      // =
      var num = 10;
      console.log(num); //-->10
      
      // +=, -=, *=, /=, %=
      var num = 10;
      num += 2;
      console.log(num); //-->12
      ```

## 2 Operator Precedence

![OperatorPrecedence](\img\OperatorPrecedence.png)

- Practice

  - ```javascript
    console.log(4 >= 6 || 'human' == 'avatar' && !(12 * 2 == 144) && true ); //-->ture
    
    var num = 10;
    console.log( 5 == num/2 && (2 + 2 * num).toString() === '22'); //-->true
    ```

# Control Flow

Control our code run as a kind of order. There are three structures in control flow. Sequential Structure, Branch Structure, Loop structure.

![ControlFlow](\img\ControlFlow.png)

## 1 Sequential Structure

The code in Sequential Structure will be executed one by one by sequential order.

![SequentialStructure](\img\SequentialStructure.png)

## 2 Branch Structure

The order of code executed depends on different condition. Different routes will get different return.

![BranchStructure](\img\BranchStructure.png)

### 2.1 if statement

- if statement

  - The code will be executed while the condition is true.

  - ```javascript
    if (condition) {
        //code
    }
    ```

- if else statement

  - The code1 will be executed while the condition is true. And the code2 will be executed while the condition is false.
  
  - ```javascript
    if (condition) {
        //code1
    }else {
        //code2
    }
    ```
  
- Multi-branch statement

  - if, else if, else. the code will be executed if the condition before it is true

  - ```javascript
    if (condition1) {
        //code1
    }else if (condition2) {
        //code2
    } else if (condition3) {
        //code3
    } else {
        //code4
    }
    
    //if one of the condition is checked and it's true. The rest of the condition will not be ckecked.
    //only one section will be executed
    ```

  - example

    - **!!!!!!!!!!!!!!!! It is similar with app.use() in Node.js.** In Express, app.use() will catch the request, and won't pass it without next().

    - ```javascript
      var score = prompt('your socre: ');
      if (score >= 90) {
          alert('A');
      } else if (score >= 80) {
          alert('B');
          //if this was executed, that mens score must be less than 90.
      } else {
          alert('C');
      }
      ```

### 2.2 switch statement

- A kind of Multi-branch statement

  - if expression is equal to the value behind the case, the section of this case will be executed. However, it will not stop executing without break even it catch the value equal to expression. default section will be executed as there is no value equal to expression.

  - ```javascript
    switch(expression) {
        case value1 : 
            //code1
            break;
        case value2:
            //code2
            break:
        default:
            //code3
    }
    
    //switch statement check value by ===
    ```


## 3 Loop Strcuture

 Could repeatedly executed code.

### 3.1 for loop

consist of Loop Body（循环体）, Terminal Condition（终止条件）

```javascript
for (initialize variable; condition expression; operator) {
    //Loop Body
}

//condition expression is Terminal Condition
```

- example

  - ```javascript
    for (var i=1; i<=100; i++) {
        console.log('Hello world!');
    }
    ```

  - ```javascript
    //softcoding
    var num = prompt('How many times you want me to greet?: ');
    for (var i=1; i<=num; i++) {
        console.log("Hello World");
    }
    ```

- double loop

  - the inner loop will be executed all while external loop was executed one time.

  - ```javascript
    //example1
    var str = '';
    for (var i=1; i<=5; i++) {
        for (var j=!; j<=5; j++) {
            str += '*';
        }
        str += '\n';
    }
    console.log(str);
    ```

  - ```javascript
    //example2
    var str = '';
    for (var i=1; i<=9; i++) {
        for (var j=1; j<=i; j++){
            str += j + '*' + i + "=" + i*j + '\t';
        }
        str += '\n';
    }
    ```

### 3.2 while loop

- Be executed until codition wan't true.

- ```javascript
  while (condition expression) {
      //Loop Body
  }
  ```

- example

  - ```javascript
    var num = 1;
    while (num <= 100) {
        console.log('Hello World');
        num++;
    }
    ```

### 3.3 do while loop

- Will be executed at least one time.

- ```javascript
  do {
      //Loop Body
  } while (condition)
  ```

## 4 Ternary Expression

Ternary Expression is the expression consist of Ternary operator.

- condition ? expression1 : expression2;

- if the condition is true, it will return the value of expression1, or it will return th value of expression2.

- ```javascript
  var num = 10;
  console.log('if num bigger greater than 5?: ');
  console.log( num>5? 'YES':"NO");
  ```


## 5 Breakpoint Debug

google for details

![BreakpointDebug](\img\BreakpointDebug.png)

## 6 Contine and Break

### 6.1 Contine

jump out of current loop, and contine the next loop

- ```javascript
  for (var i=1; i<=5; i++) {
      if (i == 3){
          continue;
      }
      console.log(i);
  }
  //--> 1, 2, 4, 5
  ```

### 6.2 Break

jump out of all loops.

- ```javascript
  for (var i=1; i<=5; i++) {
      if (i == 3){
          break;
      }
      console.log(i);
  }
  //--> 1, 2
  ```

# Array

A set of data. 

***Accurately, it should be called as Linked List. It has a different data structure with the array such as in JAVA. You could learn more by studying data structure.

Linked List is usually used in script languages.

## 1 Introduction

### how to creat an array

```javascript
//Create an array as an Object by new keyword.
var arr = new Array();

//Create an array by []
var arr1 = [];
var arr2 = [1, 'hello', true, 3.14, arr1];
// the data in array such as 1, 'hello' is called element
```

## 2 Get the array element

the index of array begin with 0.

### 2.1 Array Index

Get the element in Array by using index by the form of Array[index].

Also called accessed the element in array.

- ```javascript
  //example
  var arr2 = [1, 'hello', true, 3.14, arr1];
  console.log(arr2[1]); //-->'hello'
  console.log(arr2[100]); //-->undefined
  ```

### 2.2 Traverse Array

go through the array.

- ```javascript
  //example
  var arr = ['red', 'green', 'blue'];
  for (var i=0; i<3; i++) {
    console.log(arr[i]);
  }

## 3 Get the length of array

### 3.1 Array.length

- ```javascript
  //example
  var arr = ['red', 'green', 'blue'];
  for (var i=0; i<arr.length; i++) {
    console.log(arr[i]);
  }
  ```

### 3.2 Get the max in array

- It's algorithm. Learn more by studying algorithm.

  - ```javascript
    var arr = [2, 6, 1, 77, 52, 25, 7];
    var max = arr[0];
    for (var i=1; i<arr.length; i++) {
        if(arr[i] > max) {
            max = arr[i];
        }
    }
    cosnole.log('max: ' + max);//-->77
    ```

### 3.3 Add new elements

- By expanding the length of array

  - ```javascript
    var arr = ['red', 'green', 'blue'];
    console.log(ar.length); //-->3
    arr.length = 5;
    console.log(arr); //appended two empty elements
    console.log(arr[4]); //-->undefined
    ```

- Add/Update element directly

  - ```javascript
    var arr = ['red', 'green', 'blue'];
    arr[3] = 'pink';
    console.log(arr[3]); //-->pink
    arr[0] = 'yellow';
    console.log(arr[0]); //-->yellow
    ```

- Practice

  - ```javascript
    //Create a arry [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
    var arr = [];
    for (var i=1; i<10; i++) {
        arr[i] = i + 1;
    }
    cosnole.log(arr);
    ```

  - ```javascript
    //pick up the number greater than 10. and put them in a new array
    var arr = [2, 0, 6, 1, 77, 0, 52, 0, 25, 7];
    var newArr = []; //newArr.length == 0;
    for (var i=0; i<arr.length; i++) {
        if (arr[i] >= 10) {
            newArr[newArr.length] = arr[i];
            //Needn't newArr.length++
            //newArr.length auto updata
        }
    }
    console.log(newArr);
    ```

## 4 Array Sort

- Bubble sort (algorithm)

  - There are more understandable video in YouTube or Bilibili.

    - https://www.bilibili.com/video/BV13J411L72U?from=search&seid=10489636615108067625

  - ```javascript
    var arr = [5, 4, 3, 2, 1];
    
    for (var i=0; i<arr.length; i++) {
        for (var j=0; j<arr.lenght-1; j++) {
            if (arr[j] > arr[j+1]) {
                var tmp = arr[j];
                arr[j] = arr[j+1];
                arr[j+1] = temp;
            }
        }
    }
    ```


# Function

A code block that packaged the code would be repeatedly executed.

```javascript
//example, get the sum
function getSum(num1, num2) {
    var sum = 0;
    for (var i=num1, i<=num2; i++) {
        sum += i;
    }
    console.log
}

getSum(1, 100);
getSum(10, 50);
getSum(1, 1000);
```

## 1 How to use function

Two steps, firstly declare function, secondly invoke function.

```javascript
//declare function
function functionName (parameter) {
    //Function Body
}

//invoke function
functionName();
```

## 2 Function Parameter

### 2.1 Formal Parameter and Actual Parameter

Formal parameter, Actual parameter.

Formal parameter, the parameter in function declaring.

Actual Parameter, the parameter in function invoking.

![Parameter](\img\Parameter.png)

- **The numbers of Formal Parameter and Actual Parameter**

  - ![NumberOfParameter](\img\NumberOfParameter.png)

  - ```javascript
    //match the numbers of Formal Parameter and Actual Parameter
    function getSum(num1, num2) {
      console.log(num1 + num2);
    }
    
    getSum(1, 2); //-->3
    getSum(1, 2, 3); //-->3
    getSum(1); //--> 1 + undefined -->NaN
    ```

### 2.2 Return Value

- Form

  - ```javascript
    function FunctionName(parameter) {
        //Function Body
        return Value
    }
    ```

- Example

  - ```javascript
    function getSum(num1, num2) {
      return num1 + num2;
    }
    
    console.log(getSum(1, 2)); //-->3
    console.log(getSum(1, 2, 3)); //-->3
    console.log(getSum(1)); //--> 1 + undefined -->NaN
    ```

- The code after return will not be executed.

  - ```javascript
    function getSum(num1, num2) {
        return num1 + num2;
        alert('This code will not be executed.');
    }
    
    console.log(getSum(1, 2)); //-->3
    ```

- return only can return one value

  - ```javascript
    function fn(num1, num2) {
        return num1, num2;
    }
    
    console.log(fn(1, 2)); //-->1

- Return multiple values by using array.

  - ```javascript
    function fn(num1, num2) {
        return [num1, num2];
    }
    
    console.log(fn(1, 2)); //-->[1, 2]
    ```

- The function without return will return undefined.

  - ```javascript
    function getSum(num1, num2) {
      console.log(num1 + num2);
    }
    
    console.log(getSum(1, 2)); //--> undefined
    ```

### 2.3 aruguments

- arguments catch all the actual parameterss and put them in ArrayLike by default.

- ```javascript
    //example
    function fn() {
        console.log(arguments);
    }
    
    fn(1, 2, 3);//-->[1, 2, 3]
    ```

- ArrayLike

  - Has length field like Array.

  - Store data by index.

  - Array doesn't have the methods of array. e.g. pop(), push().

  - ```javascript
    //example return the max of parameters
    function getMax() {
        var max = arguments[0];
        for (var i=1; i<arguments.length; i++) {
            if (arguments[i] > max) {
                max = arguments[i];
            }
        }
        return max;
    }
    
    console.log(getMax(11, 2, 34, 444, 5, 100)); //-->444
    ```


## 3 reverse

- use fuction to do reverse

  - ```javascript
    function reverse(arr) {
        var newArr =[];
        for (var i=arr.length-1; i>=0; i--) {
            newArr[newArr.length] = arr[i];
        }
        return newArr;
    }
    ```

## 4 Bubble sort

- Use function do buble sort

  - ```javascript
    function sort(arr) {
        for (var i=0; i<arr.length; i++) {
            for (var j=0; j<arr.length-i-1; j++) {
                if (arr[j] > arr[j+1]) {
                    arr[j] = arr[j+1];
                    arr[j+1] = temp;
                }
            }
        }
        return arr;
    }
    ```

## 5 mutually invoke

- ```javascript
  function f1() {
      //f1 body
  }
  
  function f2() {
      f1(); //It'S OK
  }
  ```

## 6 Anonymous Functions

Another way to declare function without function name.

- ```javascript
  var func = function(aru) {
      console.log("Hello " + aru);
  }
  
  func("Conan"); //-->"Hello Conan"
  
  /*
  	(1)func is the name of varibale, not the name of fucntion
  	(2)This way also could pass parameters
  */
  ```

# Scope

The scope that variable or function can effect.

Two kinds of scope --> Global Scope, Local Scope.

- Global Scope
  - Will effect on all script or .js
- Local Scope
  - Only effect on sections of code. such as in function

## 1 Varibale

- Global Variable

  - will be kept in memory until the program was shut down. waste memory resources.

  - ```javascript
    var num = 10; //Global variable
    
    function fn() {
        console.log(num);
    } //-->10
    ```

- Local Varibale

  - will be destroied when isn't used. save memory resources.

  - ```javascript
    function func() {
        var num1 = 10; //Local variable
    }
    
    console.log(num1) //-->error: num1 is not defined
    ```

- special case

  - ```javascript
    function func() {
        var num = 10; //Local variable
        num2 = 20; //Global variable
    }
    
    console.log(num2); //-->20
    
    //The variable without declaring in function will be global variable
    ```

## 2 Block Scope

Block Scope is added in ES6.

Block means... the section of {}, you could learn more by studying JAVA

for example The varibale in {} (block) is block scope, will effect only in current block.

You needn't worry about this in JavaScript.

## 3 Scope chain

Inner varibale access external variable.

- ```javascript
  //example
  function f1() {
      var num = 123;
      
      function f2() {
          console.log(num);
      }
      
      f2();
  }
  
  var num = 456;
  
  f1(); //-->123
  ```

# Hoisting

I don't know if this called hoisting. Its name in chinese is called 预解析.

## 1 Start with Example

Hoisting is difficute to explain for me. So let's start with some example.

- ```javascript
  //normally code
  var num = 10;
  console.log(num); //-->10
  ```

- ```javascript
  //how about I declare the variable later?
  console.log(num);
  var num = 10; //--> undefined
  ```

- ```javascript
  //how about I invoke the function before I declare it?
  fn();
  
  function fn() {
      console.log("Hello world!");
  }
  ```

- ```javascript
  //Change the way of declaring function and try again.
  fun(); //error: fun is not a function
  
  var fun = function() {
      console.log("Hello world!");
  }
  ```

## 2 How JS engine run JS code

JS engine run js code by two steps. hoisting and executed code.

- (1) Hoisting. take the var varibale and function in current scope to the front of the scope.
- (2) Executed the code in order.

## 3 Variable Hoisting and Function Hoisting

- Variable Hoisting
  - Hoist variable declaring ahead of other code, but do not hoist varibale assigning.
- Function Hoisting
  - Hoist variable declaring ahead of other code, but do not invoke.

## 4 Practice Example

- ```javascript
  //example1
  var num = 10;
  fun();
  function fun() {
      console.log(num); //-->undefined
      var num = 20;
  }
  ```

- ```javascript
  //example2
  var num = 10;
  function fn() {
      console.log(num); //-->undefined
      var num = 20;
      console.log(num);//-->20
  }
  ```

- ```javascript
  //example4
  f1();
  console.log(c);
  console.log(b);
  console.log(a);
  function f1() {
      var a = b = c = 9;
      console.log(a);
  	console.log(b);
  	console.log(c);
  }
  
  /*
  	var a = b = c = 9; is different with var a = 9; b = 9; c = 9;
  	
  	var a = b = c = 9; equal to 
  	c = 9; //global variable
  	b = c; //global variable
  	var a = b; //global variable
  	
  	var a = 9; b = 9; c = 9; equal to
  	var a = 9;
  	var b = 9;
  	var c = 9;
  */
  ```

- ```javascript
  //example3
  var a = 18;
  f1();
  function f1() {
      var b = 9;
      console.log(a); //-->undefined
      console.log(b);//-->9
      var a = '123';
  }
  ```

# Object

It's a really abstract  concept. you'd better to learn more by studying object oriented programming language such as JAVA.

consist of fields and methods.

- differences between fields and variables
  - variables need to be declared, fields needn't.
  - method is more like the function in Object.

## 1 How to create and use Object

by literal {} , by new Object, by construtor.

### 1.1 By Literal {}

- ```javascript
  var obj = {};
  ```

- ```javascript
  //create object
  var obj = {
      username = 'Conan',
      age = 18,
      sayHi: function() {
          console.log("Hello!");
      },
  }
  
  //the fields and function in Object should be stored by key-value pairs. like key : value,
  
  //use object
  console.log(obj.username); //-->Conan
  console.log(obj['age']); //-->18
  obj.sayHi(); //-->"Hello!"
  ```

### 1.2 By new Object

- ```javascript
  var obj = new Object();
  
  obj.username = 'Conan';
  obj.age = 18;
  obj.sayHi = function() {
      console.log('Hello!');
  }
  
  console.log(obj.username); //-->Conan
  console.log(obj['age']); //-->18
  obj.sayHi(); //-->"Hello!"
  ```

### 1.3 By constructor

Abstract the common fields or functions, and package them into a function. The function（函数） is called constructor（构造函数）.

- Form

  - ```javascript
    //create constuctor
    function ConstructorName(value) {
        this.fields = value;
        this.method = function() {
            //method body
        }
    }
    
    //create an object by above constructor
    new ConstructorName(value);
    ```

- Example

  - ```javascript
    //User constructor
    function User(username, age){ //constructor name begin with capital
        this.username = username;
        this.age = age;
        this.greet = function() {
            return 'Hello! My name is ' + this.username + "!"
        }
    }
    
    //use object
    var user1 = new User('Conan', 18);
    console.log(typeof user1); //-->object
    console.log(user1.greet()); //-->'Hello! My name is Conan!'
    ```

## 2 new keyword

The steps of new keyword run :

1. 'new ConstructorName' could create a null object.
2. this keyword will point to the object.
3. executed the code in constructor to add value and method to the object.
4. finally return the object.

## 3 traverse object

'for in' statement is used to traverse object.

- form

  - ```javascript
    for (variable in object) {
        //code
    }
    ```

- example

  - ```javascript
    //example
    var obj = {
        username = 'Conan',
        age = 18,
        sayHi: function() {
            console.log("Hello!");
        },
    }
    
    for (var key in obj) {
        console.log(key); //--> username, age sayHi
        console.log(obj[key]); //-->'Conan', 18, function sayHi
    }
    ```

# Built-in Objects

Three types of object, custom object, built-in object, browser object.

Custom object and Built-in object is basics belong to ECMAScript. But browser object is only for JS.

The built-in Object, for example, Math, Date, Array, String.

## 1 Use Document

It's  really important because I can't list them all and you can't remember them all.

Useful Document

- MDN

### How to use Document

1. Read what this method could do.
2. Read the meanings of parameters and their types.
3. Read the meanings of return value and types.
4. Test it by a demo.
5. Read the example.

## 2 Math

Math object doesn't have constructor, so we needn't use it by new keyword. Just use it directly.

**The class which couldn't be used to created instance, is called utility class.** Learning more by Studying Class.

- example

  - ```javascript
    //Math.PI
    cosnole.log(Math.PI); //-->3.1415926...
    
    //Math.max()
    console.log(Math.max(1, 99, 3)); //-->99
    ```

- Other fields and methods in Math Object.

  - Math.PI    //PI

  - Math.floor()     //round down

  - Math.ceil()    //round up

  - Math.round()    //round

    - ```javascript
      Math.round(1.5) //-->2
      Math.round(-1.5) //-->-1
      ```

  - Math.abs    //absolute value
  - Math.max()    //maximum
  - Math.min()    //minimum

- random()

  - ```javascript
    Math.random() //take the value of [0, 1)
    ```

  - more usage by reading the document

## 3 Date

> JavaScript **`Date`** objects represent a single moment in time in a platform-independent format. `Date` objects contain a `Number` that represents milliseconds since 1 January 1970 UTC.
>
> ---Date MDN (access 2021/05/05)

Date objects use constructor to create object.

- Usage

  - ```javascript
    var date = new Date();
    console.log(date); //get current time without parameter
    
    var date1 = new Date(2019, 10 ,1);
    console.log(date1); //return Nov
    
    var date2 = new Date('2019-10-1 8:8:8');
    console.log(date2); //return oct
    ```

- Date Format

  - ![DataFormat](\img\DataFormat.png)

- Timestamp

  - get the millisecond past from 1st,  Jan, 1970.

  - ```javascript
    //by valueOf() or getTime()
    var date = new Date();
    console.log(date.valueOf());
    console.log(date.getTime());
    
    //by +new Date(),Usual writing style
    var date1 = +new Date();
    console.log(date);
    
    //by Date.now(), new way in H5
    console.log(Date.now());
    ```

  - 

- In action

  - count down

  - ![DateAction](\img\DateAction.png)

  - ```javascript
    function countDown(time) {
        var nowTime = +new Date();
        var inputTime = +new Date(time);
        var times = (inputTime - nowTime)/1000; //times variable is the second of the rest of time.
        var day = parseInt(times / 60 / 60 / 24); //the rest day
        var hour = parserInt(times / 60 / 60 % 24); //hours
        var minute = parseInt(times / 60 % 60); //minutes
        var second = parseInt(times % 60); //seconds
        return day+'days' + hour+'hours' + minute+'minutes' + second+'seconds';
    }
    
    console.log(countDown('2022-5-5 0:0:0'));
    ```

## 4 Array

- review

  - ```javascript
    //empty array
    var arr1 = new Array(); 
    
    //empty array but its lenghth is 2
    var arr2 = new Array(2);
    
    //equal [2, 3]
    var arr3 = new Arrat(2, 3);
    ```

### 4.1 Determine Type

- instanceof
  - instanceof keyword is used to determine if the data is a instance of the Object.

  - ```javascript
    var arr = [];
    var obj = {};
    
    console.log(arr instanceof Array); //--> true
    console.log(obj instanceof Array); //--> false
    ```

- Array.isArray()

  - ```javascript
    var arr = [];
    var obj = {};
    
    console.log(Array.isArray(arr)); //--> true
    console.log(Array.isArray(obj)); //--> false
    ```

### 4.2 Create/Delete elements

- ![ArrayCD](\img\ArrayCD.png)

- push()

  - add one or multipe elements at the end of Array.

  - ```javascript
    var arr = [1, 2, 3];
    
    console.log(arr.push(4)); //-->push() return the length of new Array
    console.log(arr); //-->[1, 2, 3, 4]
    ```

- unshift()

  - add one or multipe elements at the head of Array.

  - ```javascript
    var arr = [1, 2, 3];
    
    console.log(arr.unshift(0)); //-->unshift() return the length of new Array
    console.log(arr); //-->[0, 1, 2, 3]
    ```

- pop()

  - delete the last element of Array. Only can delete one element.

  - ```javascript
    var arr = [1, 2, 3];
    
    console.log(arr.pop()); //-->pop() return the element deleted
    console.log(arr); //-->[1, 2]
    ```

- shift()

  - delete the first element of Array. Only can delete one element.

  - ```javascript
    var arr = [1, 2, 3];
    
    console.log(arr.shift()); //-->shift() return the element deleted
    console.log(arr); //-->[2, 3]
    ```

### 4.3 sort

- ![ArraySort](\img\ArraySort.png)

- reverse()

  - reverse the array

  - ```javascript
    var arr = [1, 2, 3];
    
    arr.reverse();
    console.log(arr); //-->[3, 2, 1]
    ```

- sort()

  - sort the array

  - ```javascript
    var arr = [2, 3, 1];
    
    arr.sort();
    console.log(arr); //-->[1, 2, 3]
    ```

  - Special case

    - ```javascript
      var arr = [13, 4, 77, 1, 7];
      
      arr.sort();
      console.log(arr); //-->[1, 13, 4, 7, 77]
      //it sort the elements by the first of the number, then second number
      ```

    - ```javascript
      //ascending sort
      var arr = [13, 4, 77, 1, 7];
      
      arr.sort(function(a, b) {
          return a - b;
      });
      console.log(arr); //-->[1, 4, 7, 13, 77]
      ```

    - ```javascript
      //descending sort
      var arr = [13, 4, 77, 1, 7];
      
      arr.sort(function(a, b) {
          return b - a;
      });
      console.log(arr); //-->[77, 13, 7, 4, 1]
      ```

### 4.4 index

- ![ArrayIndex](\img\ArrayIndex.png)

- indexOf()

  - find the element and return its index. If it not exist, it will return -1. And only return the first value's index.

  - indexOf(key, [StartIndex])

  - ```javascript
    var arr = ['red', 'green', 'blue', 'pink'];
    console.log(arr.indexOf('blue')); //-->2
    
    var arr1 = ['red', 'green', 'blue', 'pink', 'blue'];
    console.log(arr.indexOf('blue')); //-->2
    
    var arr = ['red', 'green', 'pink'];
    console.log(arr.indexOf('blue')); //-->-1
    
    var arr1 = ['red', 'green', 'blue', 'pink', 'blue'];
    console.log(arr.indexOf('blue', 3)); //-->4
    ```

- lastIndexOf()

  - find the element from the last one and return its index. If it not exist, it will return -1. And only return the first value's index.

  - ```javascript
    var arr = ['red', 'green', 'blue', 'pink'];
    console.log(arr.lastIndexOf('blue')); //-->2
    
    var arr1 = ['red', 'green', 'blue', 'pink', 'blue'];
    console.log(arr.lastIndexOf('blue')); //-->4
    
    var arr = ['red', 'green', 'pink'];
    console.log(arr.lastIndexOf('blue')); //-->-1
    ```

### 4.5 Removing Duplicate Elements

- ![RemovingDuplicateElements](\img\RemovingDuplicateElements.png)

- ```javascript
  //can't recommond, but it's also a way. I think it's better to use in or not in.
  
  function unique(arr) {
      var newArr = [];
      for (var i=0; i<arr.length; i++) {
          if (newArr.indexOf(arr[i]) === -1) {
              newArr.push(arr[i]);
          }
      }
      return newArr;
  }
  ```

### 4.6 convert into String

- ![Convert IntoString](\img\Convert IntoString.png)

- toString()

  - ```javascript
    var arr = [1, 2, 3];
    
    console.log(arr.toString()); //--> '1, 2, 3'
    ```

- join()

  - ```javascript
    var arr = [1, 2, 3];
    
    console.log(arr.join()); //--> '1, 2, 3'
    console.log(arr.join('-')); //--> '1-2-3'
    ```

- slice(), splice()

  - ![Convert IntoString2](\img\Convert IntoString2.png)
  - toUpperCase()
  - toLowerCase()
  - google for them please. especially for splice().

### 4.7 String Object

- Start with example

  - ```javascript
    var str = 'Hello';
    console.log(str.length); //-->5
    ```

- Only Object has fields and method.

  - Why String have length field?

  - Wrappers

    - wrap the Simple data type to complex data type

  - ```javascript
    //It's effect like these
    var temp = new String('Hello');
    str =  temp;
    temp = null;
    ```

- Wrappers also work on Number and Boolean

- String is Immutable

  - ```javascript
    var str = 'Hello';
    var Str = '你好';
    
    //It seems we change the value of str. But it just change the pointer/address.
    //It will take lots of memory resouces if you change the value often.
    //In JAVA, there is a garbage collection. so you don't need worry about it.
    ```

  - Learn pointer more by Studying C or JAVA.

- find all index of key in Array

  - ```javascript
    var str = 'aobocodoeo';
    
    var index = str.indexOf('o');
    var num = 0;
    while (index !== -1) {
        console.log(index);
        num++;
        index = str.indexOf('o', index + 1);
    }
    console.log('the number of o:  ' + num);
    ```

- return the character by index

  - ![Character](\img\Character.png)

  - charAt()

    - ```javascript
      var str = 'Hello';
      
      console.log(str.charAt(2)); //-->e
      
      for (var i=0; i<str.length; i++) {
          console.log(str.charAt(i));
      }
      ```

  - charCodeAt()

    - return the ASCII code of the character.

  - str[]

    - ```javascript
      var str = 'Hello';
      
      console.log(str.[2]); //-->e
      
      for (var i=0; i<str.length; i++) {
          console.log(str[i]);
      }
      ```

- count the number of every character.

  - ```javascript
    var str = 'aobocodoeobacdef';
    
    var count = {};
    
    for (var i=0; i<str.lenght; i++) {
        var chars = str.chartAt(i);
        if (count[chars]) {
            count[chars]++;
        } else {
            count[chars] = 1;
        }
    }
    
    //you also can find the max in count
    var max = 0;
    var ch = '';
    for (key in count) {
        if (count[key] > max) {
            max = count[key];
            ch = key
        }
    }
    console.log(max);
    ```

- String operation methods

  - ![StringMethods](\img\StringMethods.png)

  - ```javascript
    //concat()
    console.log('Hello, '.concat('world!')); //--> Hello, world!
    
    //substr()
    console.log('Hello'.substr(2, 2)); //-->ll
    ```

- replace()

  - replace the character to another one. Only can replace the first one.

  - ```javascript
    var str = 'Hello, ella';
    console.log(str.replace('e', 'a')); //-->Hallo, ella
    ```

  - ```javascript
    //change all character
    var str = 'aobocodoeo';
    
    while (str.indexOf('o') !== -1) {
        str = str.replace('o', '*');
    }
    console.log(str); //-->'a*b*c*d*e*'

- split()

  - split the String by the character gave as parameter

  - ```javascript
    var str = 'red, pink, blue';
    console.log(str.split(',')); //-->['red', 'pink', 'blue'];
    ```

# Simple Data Type and Complex Data Type

- Simple data type, is also called value type.
  - saved in stack.
  - Store true value. e.g. string, number, boolean, undefined, null.
  - Interstingly, if you use typeof null, it will return object. It said it's a miss during design JavaScript.

- Complex data type is also called reference type.
  - saved in Heap.
  - Store address/pointer in Stack, and Store true value in Heap. the adress/pointer in Stack point to Heap.
  - Created by new keyword. e.g. Object, Array, Date
- Stack and Heap
  - ![StackAndHeap](\img\StackAndHeap.png)

- transfer parameter

  -  Simple data type

    - ```javascript
      function fn(a) {
          a++;
          console.log(a);
      }
      
      var x = 10;
      
      fn(x); //--> 11
      console.log(X); //-->10
      
      //the value of x wasn't changed.
      //between Simple data type. Use true value to transfer parameter.
      ```

    - It will not change the value of variable.

  -  Complex data type

    - ```javascript
      function Person(name) {
          this.name = name;
      }
      
      function f1(x) {
          console.log(x.name); //--> Conan
          x.name = 'abc';
          console.log(x.name); //--> abc
      }
      
      var user = new Person('Conan');
      console.log(user.name); //--> Conan
      f1(user);
      console.log(user.name); //--> abc
      
      //the value of user.name was changed.
      //between Complex data type. Use pointer to transfer parameter.
      ```

    - 