### JavaScript Basic to Advance Topics List

- output in js
```js
    <script>
        alert("Pranto Kuamr");
        document.write("My Name Is Pranto Kumar");
        console.log("I'm Pranto Kumar") //only show console mode of browser
    </script>
```

- Keyword, Data Type and comment
  - String
  - Number
  - Boolean //True & False
    
- declare variables
```js
    <script>
        var name = "Pranto Kuamr";
        document.write(name);
    </script>
```

- number method | toFixed | toPrecision
```js
console.log(typeof(Number("23")));
console.log(Number(true));
```

```js
var num = 4.56878;
console.log(num.toFixed(3));
```
```js
var num = 4.56878;
console.log(num.toPrecision(4));
```

- add or concatenate strings
```js
document.write("Pranto" + " Kumar");
```
  
- Library functions for string
  ```js
  var text = "Pranto";
  document.write("Length of the word is : " + text.length);
  document.write(text.charAt(2)); //identify location wise character
  document.write(text.toUpperCase());
  document.write(text.toLowerCase());
  document.write(text.slice(2,4));
  ```
  
  ```js
  var text = prompt("Enter Your Name : "); //take user input
  document.write("Number of character :" + text.length);
  ```

  
- Arithmetic and assignment operator
  - Arithmatic(+,-,*,/,%) otther (**, ++, --)
  - Assignment (=,+=,-=,*=,/=,%=,**=)

- Make your own calculator
  
   - short program
  ```js
        var num1 = prompt("Enter The First Number: "); //user input function
        var num2 = prompt("Enter The Second Number: ");

        num1 = parseInt(num1, 10); //convert string to integer function
        num2 = parseInt(num2, 10);

        var sum = num1 + num2; // concatenate strings
        document.write("Sum is : " + sum + "<br/>"); //show output function

        var sub = num1 - num2;
        document.write("Sub is : " + sub);
  ```

- Area of various shapes
- how to make temperature converter
- Relational and Logical Operator
   - Relational operator ( >, >=, <, <=, ==, ===, !=, !==)
   - logical operator (&&, ||, !)
     
- if, else if, else
- Letter Grade Program (just for practise)
- Programs using logical operators
- Switch
- how to use for loop in javascript (part-1)
- how to use for loop in javascript (part-2)
- how to use while loop in javascript
- how to use do-while loop in javascript
- how to use break and continue
- Ternary operator
- Traditional function
- IIFEs and function expression
- how to create and use array
- How to loop an Array
- Array library methods -(push,pop,concat,shift,unshift,splice,slice,sort,reverse)
- one dimensional array | Task 8 (Important)
- two dimensional array | Task 9 (Important)
- how to create and use object
- Math Object
- Guessing Game
- Date object and date methods
    ```js
    var date = new Date();
    console.log(date);
    
    var year = date.getFullYear();
    console.log(year);
    
    var month = date.getMonth();
    console.log(month);
    
    var currentDate = date.getDate();
    console.log(currentDate);
    
    var currentDay = date.getDay();
    console.log(currentDay);
    
    var currentHour = date.getHours();
    console.log(currentHour);
    
    var currentMinutes = date.getMinutes();
    console.log(currentMinutes);
    
    var currentSeconds = date.getSeconds();
    console.log(currentSeconds);
    
    var currentMilliSeconds = date.getMilliseconds();
    console.log(currentMilliSeconds);
    ```
- DOM | select html elements
   ```js
   document.getElementById("heading1").innerHTML = "Hello";
   ```
- query selector
- Event Handler to onclick event
- Find, create, add, remove html elements
- DOM traversing & manipulating
- image slider
- Changing CSS style dynamically
- Event Listener
- Event Listeners with multiple elements
- how to play audio in javascript
- How to add and remove animation
- Keypress listener
- DOM Event | Event Object | onchange event
- DOM Event | Event Object | onsubmit event
    ```html
     <form action="">
        <div>
            <label for="name">Name :
                <input type="text" id="name" name="name" required autofocus>
            </label>
        </div>

        <div>
            <label for="email">Email :
                <input type="email" id="email" name="email" size="30">
            </label>
        </div>

        <div>
            <label for="password">Password :
                <input type="password" id="password" name="password" required minlength="4" maxlength="8">
            </label>
        </div>

        <div>
            <input type="submit" value="Signup">
        </div>
    </form>
    ```

    ```css
    div {
    margin-bottom: 1rem;
    }
    ```
    ```js
    const form = document.querySelector("form");
    const name = form.querySelector("div #name");
    const email = form.querySelector("div #email");
    const password = form.querySelector("div #password")

    form.addEventListener('submit', formHandler);

    function formHandler(e){
    e.preventDefault();

   const userInfo = {
    name : name.value,
    email : email.value,
    password : password.value,
   };
   console.log(userInfo);
   name.value ="";
   email.value ="";
   password.value ="";
   }
    ```
- DOM Event | Event Object | media events
- DOM Event | Event Object | scroll, resize, toggle
- DOM Event | MouseEvent
- DOM Event | KeyboardEvent
- DOM Event | FocusEvent
- DOM Event | ClipboardEvent
- DOM Event | DragEvent
- Browser Object Model (BOM) | location object
    - href
    - protocol
    - hostname
    - pathname
- Browser Object Model | Popup boxes
    - alert
    - confirm
    - prompt
- Browser Object Model | Timing events
    - setTimeOut()
    - setInterval()
- Browser Object Model | Create a Clock
- best practices for javascript coding
- how to handle error in JavaScript (part-1)
- 


 

























