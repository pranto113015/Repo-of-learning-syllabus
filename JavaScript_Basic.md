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
- 
  
 

























