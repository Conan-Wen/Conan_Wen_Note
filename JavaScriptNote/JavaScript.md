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

