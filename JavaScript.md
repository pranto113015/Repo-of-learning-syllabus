# JavaScript Topics


## Js part-1 (Basic)
- Introduction to js
  - what is js?
  - what are the way to add js?
      - inline js
      - internal js
      - external js
  - setting up the environment
  - output : alart(),confirm(),console
  - comment : single line comment,multiple line comments


- Tokens
  - keywords,
  - puncuators,
  - backslash characters : \n,\t,
  - variables : var,let,const
  - data types :number, string, boolean, null, undefined, object, symbol
  - truthy vs falsy values,


## Js part-2 (Basic)
- operators : Arithmetic (+,-,*,/,%), Assignment, Comparision (>,<,<=,>=,==,===), Logical(&&, ||, !), unary(+,-,++,--)



## Js part-3 (Basic) 
- Control statement
  - conditional control statement : if, else, elseif, switch
  - loop control statement : for, while, do while, (break, continue), (while vs do while ) 
- Array, String, Object
  - for of, for in


## Js part-4 (Basic)
- function vs method
   - Function (traditionla vs arrow) 
   - Mathod - Number, Math, Date, Array(push,pop,shift,unshift), string methods

  
 
## Js part-5 (Intermediate Part-1)
- ES6,ES7
   - Template literals
   - var, let, const
   - Arrow function
   - Module
   - Spread operator, Rest parameters
   - Destructure
   - Default value


## Js part-6 (Intermediate Part-2)
- ES6
   - Higher order functions : foreach(), map(), filter(), reduce(), some(), every(), sort()
     
     ```javascript
      // higher order build in function : forEach()
      const persons = ['Pranto', 'Jamal', 'Rahim', 'Topon'];
      
      persons.forEach((persons, i) => {
          console.log(`${i} : ${persons}`);
      })
     ```
     
     ```javascript
     // higher order build in function : map()
      const numbers = [1,2,3,4,5];
      const squaredNumber = numbers.map((number) => {
          return number * number;
      })
      console.log(squaredNumber);
     ```

     ```javascript
     // higher order build in function : filter()
       const products = [
      { id: 1, name: 'pranto kumar', price: 1500 },
      { id: 2, name: 'Lal kumar', price: 3000 },
      { id: 3, name: 'Gali hasan', price: 7000 },
       ]
      const filteredproducts = products.filter((product) => product.price >= 1500 && 
     product.price <= 3000);
     console.log(filteredproducts);
     ```

   - Exception handling
   - callback functions : Asynchronous vs Synchronous, callback
- Error handling



## Js part-7 (Intermediate Part-3)
- Asynchronous va Synchronous
- Asynchronous programming : async, await, then, catch, callback
- Api calling
- JSON


## Js part-8 (Intermediate Part-4)
- localstorage
- DOM and Event handler


  
## Js part-9 (Intermediate Part-5)
- oop
- A simple back app
  
  
## Js part-10 (Advanced)
- Testing

## Js part-11 (Advanced)
- Project : E-comerce front-page


















