# API

## 1 Relevance between Web APIs and JS basic

- ![1-1](\img\1-1.png)

- JS basic
  - basic syntax stipulated by ECMAScript standard.
  - Can't do interactivity.
- Web APIs
  - stipulated by W3C.
  - Mainly learn DOM and BOM. 

Web APIs is one of the apply of JS. Realize interactivity by JS basic.

## 2 API and Web API

### 2.1 API

API (Application Programming Interface, 应用程序编程接口), defined a number of functions in advance.

> In [computing](https://en.wikipedia.org/wiki/Computing), an **application programming interface** (**API**) is an [interface](https://en.wikipedia.org/wiki/Interface_(computing)) that defines interactions between multiple [software applications](https://en.wikipedia.org/wiki/Software_application) or mixed [hardware](https://en.wikipedia.org/wiki/Computer_hardware)-software intermediaries.[[1\]](https://en.wikipedia.org/wiki/API#cite_note-1) It defines the kinds of [calls](https://en.wikipedia.org/wiki/System_call) or requests that can be made, how to make them, the [data formats](https://en.wikipedia.org/wiki/Data_type) that should be used, the conventions to follow, etc. It can also provide extension mechanisms so that users can extend existing functionality in various ways and to varying degrees.[[2\]](https://en.wikipedia.org/wiki/API#cite_note-Fisher1-2) An API can be entirely custom, specific to a component, or designed based on an industry-standard to ensure [interoperability](https://en.wikipedia.org/wiki/Interoperability). Through [information hiding](https://en.wikipedia.org/wiki/Information_hiding), APIs enable [modular programming](https://en.wikipedia.org/wiki/Modular_programming), allowing users to use the interface independently of the implementation.

Programmer could realize some functions by API, without learning how did it.

- Example
  - ![1-2](\img\1-2.png)

### 2.2 Web API

Web API is the API provided by browser to operate browser or elements on Web page. such as BOM, DOM.

# DOM

DOM (Document Object Model, 文档对象模型), API recommended by W3C, to process extensible markup language (HTML or XML).

By DOM, we could change the content, construct, pattern of web page.

## 1 brief introduction

### 1.1 DOM Tree

- ![2-1](\img\2-1.png)

- Document
  - One page called one document
- element
  - All the tag is element.
- Node
  - All the content in the page could be called node. Such as tag, attribute, text, comment.

All above could be regard as object.

## 2 Get/Access Element

### Get Normal Element

- getELementById()

  - Get elements by id.

  - Return Element Object.

  - ```html
    <div id="time">2021-5-7</div>
    <script>
    	var timer = document.getELementById("time");
        console.log(timer);
        console.log(typeof timer); //-->object
    </script>
    ```

  - document.getELementById(). Because all the elements belong to document.

- getELementsByTagName()

  - Get elements by tag name.

  - Return the set of objects. stored in Arraylike.

    - ```html
      <li>Hello</li>
      <li>Hello</li>
      <li>Hello</li>
      
      <script>
      	var lis = document.getElementsByTagName('li');
          console.log(lis);
      </script>
      ```

  - getELementsByTagName() could be used not on by document, but also element.

    - ```html
      <ol id="list">
          <li>Hello</li>
      	<li>Hello</li>
      	<li>Hello</li>
      </ol>
      
      <script>
          var ol = document.getELementById('ol');
      	var lis = ol.getElementsByTagName('li');
          console.log(lis);
      </script>
      ```

- getElementsByClassName()

  - Get elements by class name.

  - Return the set of objects. stored in Arraylike.

    - ```html
      <div class="box">Box</div>
      
      <script>
          var boxes = document.getElementsByClassName('box');
      </script>
      ```

- querySelector()

  - Return the first element selected by the parameter.

  - ```html
    <div class="box">Box1</div>
    <div class="box">Box2</div>
    <div id="nav">
        <ul>
            <li>Home Page</li>
            <li>Products</li>
        </ul>
    </div>
    
    <script>
        var firstBox = document.querySelector('.box'); //-->Box1
        
        var nav = document.querySelector('#nav');
        
        var li = document.querySelector('li'); //--><li>Home Page</li>
    </script>
    ```

- querySelectorAll()

  - Have the same usage with querySelector(), but it could return all elements selected by the parameter.

### 2 Get Special Element (body, HTML)

- Get body element.

  - ```html
    <script>
        //get body element
    	var bodyEle = document.body;
    </script>
    ```

- Get HTML element.

  - ```html
    <script>
        //get HTML element
    	var htmlEle = document.documentElement;
    </script>
    ```

## 3 Event

Using JavaScript could make dynamic page, because event could be observed by JS.

- Three elements of event

  - Event sources
    - The element will trigger event. Such as bottom.
  - Event type
    - How did the element trigger event. Such as onclick.
  - Event handler
    - What will do after event triggered. Usually define event hander by assigning to a function.

- example

  - ```html
    <button id="btn">greet</button>
    
    <script>
    	var btn = document.getElementById('.btn');
        btn.onclick = function() {
            alert("Hello, World!")
        }
    </script>
    ```

### 4.1 Execute Event

- Three steps

  - Get sources
  - Registered Events (Bind Events)
  - Add Event Handler

- Example

  - ```html
    <div id="div123">123</div>
    
    <script>
        //Get sources
    	var div = document.querySelector('.div');
        //Registered Events (Bind Events)
        div.onclick = function() {
            //Add Event Handler
            console.log("123 was selected")
        }
    </script>
    ```

- Other mouse event

  - ![3-1](\img\3-1.png)

