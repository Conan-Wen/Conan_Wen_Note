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

![TheConstitutionsOfJS](C:\Users\none\Desktop\JavaScriptNote\img\TheConstitutionsOfJS.png)

- ECMAScript: JS basics, JS syntax
  - ![ECMAScript](C:\Users\none\Desktop\JavaScriptNote\img\ECMAScript.png)
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

![inputoutput](C:\Users\none\Desktop\JavaScriptNote\img\inputoutput.png)

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

![NamingConvention](C:\Users\none\Desktop\JavaScriptNote\img\NamingConvention.png)

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

  - ![SimpleData Types](C:\Users\none\Desktop\JavaScriptNote\img\SimpleData Types.png)

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

      - ![EscapeCharacter](C:\Users\none\Desktop\JavaScriptNote\img\EscapeCharacter.png)

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

    - ![TransformToString](C:\Users\none\Desktop\JavaScriptNote\img\TransformToString.png)

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

    - ![ConvertIntoNumber](C:\Users\none\Desktop\JavaScriptNote\img\ConvertIntoNumber.png)

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
        alert("the first number add the second number is " + (num1 + num2));
        ```

      - 
