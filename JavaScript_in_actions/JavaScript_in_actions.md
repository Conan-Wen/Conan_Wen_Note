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

- 