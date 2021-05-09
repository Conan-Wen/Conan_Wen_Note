# 1 Greet User Based on Current Time

- **Requirements**

  - Greet User Based on Current Time.
  - Say "Good Morning", while current time is AM
  - Say "Good Afternoon", while current time is AM

- ```html
  <div id="greet"></div>
  
  <script>
      var greet = document.querySelector('.greet');
      //get current hour
      var date = new Date();
      var h = date.getHours();
      //Modify the greet based on current time
      if (h < 12) {
          greet.innerText = "Good Morning";
      } else {
          greet.innerText = "Good Afternoon";
      }
  </script>
  ```

# 2 Display/Hide Password

- **Requirements**

  - Display/Hide Password by click button.

- **Thinking**

  - Click button to Display/Hide password.
  - Change the status of button. Click once, modify the type of input to text. Click one more time, modify it to password.
  - algorithm, set a variable to remember the status. for example, set a flag, when it's 0, text. And 1, password.

- ```html
  <style>
      .box {
          position: relative;
          width: 400px;
          border: 1px solid #ccc;
          margin: 100px auto;
      }
      .box input {
          width: 370px;
          height: 30px;
          border: 0;
          outline: none;
      }
      .box button {
          position: absolute;
          top: 2px;
          right: 2px;
      }
  </style>
  
  <body>
      <div class ="box">
          <lable for=""><button id="btn">Display</button></lable>
          <input type="password" name="" id="pwd">
      </div>
      
      <script>
          var btn = document.getElementById("btn");
          var pwd = document.getElementById("pwd");
          
          var flag = 0;
          btn.onclick = function() {
              if (flag == 0) {
                  pwd.type = "text";
              	btn.innerText = "Hide";
                  flag = 1;
              } else {
                  pwd.type = "password";
                  btn.innerText = "Display";
                  flag = 0;
              }
          }
      </script>
  </body>
  ```


# 3 Close Element(div)

- **Requirements**

  - Close the element by click buttoun.

- **Thinking**

  - Use the display/hide in style.
  - display.none, hide element.
  - display.block. display element.
  - Create a button to control it.

- ```html
  <style>
      .box {
          position: relative;
          width: 74px;
          height: 88px;
          border: 1px solid #ccc;
          margin: 100px auto;
          font-size: 12px;
          text-align: center;
          color: #f40;
          display: block;
      }
      
      .box img {
          width: 60px;
          margin-top: 5px;
      }
      
      .close-btn {
          position: absolute;
          top: -1px;
          left: -16px;
          width: 14px;
          height: 14px;
          border: 1px splid #ccc;
          line-height: 14px;
          font-family: Arial, Helvetica, sans-serif;
          cursor: pointer;
      }
  </style>
  
  <body>
      <div class="box">
          QR code
          <img src="" alt="QRcode">
          <i class="close-btn">x</i>
      </div>
      
      <script>
          var btn = document.querySelector(".close-btn");
          var box = document.querySelector(".box");
          
          btn.onclick = function() {
              box.style.display = "none";
          }
      </script>
  </body>
  ```

# 4 Display/Hide Placeholder

- **Requirements**

  - Hide placeholder when cursor selected the input.
  - Display placeholder when cursor left the input.
  - Hide if input.value is default.
  - Display if input.value is empty.

- **Thinking**

  - Get focused event: onfocus
  - Lose focus event: onblur

- ```html
  <style>
      input {
          color: #999;
      }
  </style>
  
  <body>
      <input type="text" value="PlaceHolder">
      
      <script>
          var text = document.querySelector("input");
          
          text.onfocus = function() {
              if (this.value === "PlaceHolder") {
                  this.value = "";
              }
              this.style.color = "#333";
          }
          
          text.onblur = function() {
              if (this.value === "") {
                  this.value = "PlaceHolder";
              }
              this.style.color = "#999";
          }
      </script>
  </body>
  ```

# 5 Form Validator

- **Requirements**

  - If cursor left the input and the length of value isn't between 6 and 16. remind user correct input.

- **Thinking**

  - First, if input lose focus?
  - If input is correct, tell user his input is correct.
  - Or, tell user to correct his input.

- ```html
  <style>
      div {
          width: 600px;
          margin: 100px auto;
      }
      
      .message {
          display: inline-block;
          font-size: 12px;
          color: #999;
          padding-left: 20px;
      }
      
      .wrong {
          color: red;
      }
      
      .right {
          color: green;
      }
  </style>
  
  <body>
      <div class="register">
          <input type="password" class="ipt">
          <p class="message">Enter 6~16 digits password</p>
      </div>
      
      <script>
          var ipt = document.querySelector(".ipt");
          var message = document.querySelector(".message");
          
          ipt.onblur = function() {
              if (this.value.length<6 || this.value.length>16) {
                  message.className = "message wrong";
                  message.innerHTML = "X,Enter 6~16 digits password";
              } else {
                  message.className = "message right";
                  message.innerHTML = "O, correct value";
              }
          }
      </script>
  </body>
  ```

# 6 Register Multi-elements and Exclusive

- ```html
  <body>
      <button>button1</button>
      <button>button2</button>
      <button>button3</button>
      <button>button4</button>
      <button>button5</button>
      
      <script>
          var btns = document.getElementsByTagName("button");
          
          for (var i = 0; i < btns.length; i++) {
              btns[i].onclick = function() {
                  for (var i = 0; i < btns.length; i++) {
                      btns[i].style.backgroundColor = "";
                  }
                  this.style.backgroundColor = "pink";
              }
          }
      </script>
  </body>
  ```

# Modify Background

- **Thinking**

  - Change background to the image selected.
  - Use for statement to register event to each image.
  - Take the path of image to body.

- ```html
  <style>
      * {
          margin: 0;
          padding: 0;
      }
      
      body {
          background: irl(images/1.jpg) no-repeat center top;
      }
      
      li {
          list-style: none;
      }
      
      .baidu {
          overflow: hidden;
          margin: 100px auto;
          background-color: #fff;
          width: 410px;
          padding-top: 3px;
      }
  </style>
  
  <body>
      <ul class="theme">
          <li><img src="images/1.jpg"></li>
           <li><img src="images/2.jpg"></li>
           <li><img src="images/3.jpg"></li>
           <li><img src="images/4.jpg"></li>
      </ul>
      
      <script>
          var imgs = document.querySelector(".theme").querySelectorAll('img');
          
          for (var i = 0, i < imgs.length; i++) {
              img[i].onclick = function() {
                  documenr.body.style.backgroundImage = "url(" + this.src + ")";
              }
          }
      </script>
  </body>
  ```

# Table modify color

- ```javascript
  //get element
  var trs = document.qurySelector("tbody").querySelector("tr");
  //register event by for
  for (var i = 0; i < trs.length; i++) {
      trs[i].onmouseover = function() {
          this.style.backgroundColor = "pink";
      }
      
      trs[i].onmouseout = function() {
          this.style.backgroundColor = "white";
      }
  }
  ```

- 