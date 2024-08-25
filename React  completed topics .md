# React completed topice :

[Learnign Source Link](https://www.youtube.com/watch?v=6wilewRV3xQ&t=2434s)

### REACT JS basics
  - React is a popular JavaScript library used for building user interfaces.
  - It was developed by Facebook and is now maintained by a community of developers.
  - React uses a component-based architecture, where UI elements are broken down into reusable and modular pieces.

### COMPONENT CONCEPT
- Components are independent and reusable bits of code.
- They serve the same purpose as JavaScript functions, but work in isolation and return HTML
- Components come in two types, Class components and Function components

### Tools you need to install
- NODE JS
- Visual Studio Code 

### CREATE & RUN REACT APP USING VITE
- ViteJS is a modern build tool and development server that aims to optimize the front-end development experience.
```sh
npm create vite@latest
```
- ASSET BUNDLING

### WHY VITE

- Faster build times: Vitejs uses esbuild, which is a blazing fast compiler that can build projects in a fraction of the time that it takes other build tools.
- Hot reload: Vitejs has hot reload, which means that your code will be updated in real time as you make changes, so you can see the results of your changes immediately
- Small bundle size: Vitejs bundles are typically much smaller than bundles created by other build tools, which can improve performance and reduce bandwidth usage.
  
### ESSENTIAL Vite Commands
### REACT PROJECT Structure
- Distribution
- Node Modules
- Public
- Source
- Package.json
- Vite Config

### MY FIRST FUNCTIONAL COMPONENT

In React, a functional component is a type of component that is defined using a JavaScript function.

- They are easier to read and write.
- They are simpler and lighter, making them faster to render.
- They do not require the use of the "this" keyword, making them less error-prone.
- They can take advantage of React's Hooks, which allow you to use state and other features without using class components.

### JSX JAVASCRIPT XML
- JSX is a syntax extension for JavaScript that allows you to write HTML-like code in your JavaScript code
- It is commonly used in React applications to define the structure and content of UI components.
- JSX is not a separate language, but a preprocessor that converts the HTML-like code into plain JavaScript.
- It enables you to use JavaScript expressions within your HTML-like code, making it easier to dynamically generate content.
- JSX can improve code readability and maintainability by allowing developers to write declarative, intuitive code.

### JSX CONVENTIONS
- You need to return a single parent element in JSX
- You can implement JS directly in JSX
- All Tags Self-close in JSX
- ClassName and HTMLFor, not class and for in JSX
- Write all HTML Attributes in camelCase in JSX
- Write Inline Styles as Objects in JSX

### JSX Inline if else
### Immediately invoked 
- Function expressions inside your JSX
### JSX Loop Inside
```jsx
const Hero = () => {
  const city = ["Dhaka", "India", "Kolkata", "London", "Japan", "South korea"];
  return (
    <div>
      <ul>
        {city.map((item, i) => {
          return <li key={i.tostring}>{item}</li>;
        })}
      </ul>
    </div>
  );
};

export default Hero;

```
### JSX Loop Inside Why we use map
### CONDITIONAL RENDERING 
- Using an if…else Statement
    ```sh
    const LoginStatusBtn = (status) => {
    if (status) {
      return <button>Logout Btn</button>;
    } else {
      return <button>Login Btn</button>;
    }
  };
  
  const IfElse = () => {
    return (
      <div>
        <h1>Login Status</h1>
        {LoginStatusBtn(true)}
      </div>
    );
  };
  
  export default IfElse;
  ```
- Using Switch Statement
    ```sh
    const Switch = () => {
    const status = false;
  
    switch (status) {
      case true:
        return <button>Logout Btn</button>;
      case false:
        return <button>Login Btn</button>;
      default:
        return null;
    }
  };
  
  export default Switch;
    ```
- Using Ternary Operators
    ```sh
  const Ternary = () => {
      let status = true;
      return (
          <div>
                <h1>Using Ternary Operators</h1>
              {
                  status?
                  <button>Logout Btn</button>
                  :
                  <button>Login Btn</button>
              }
          </div>
      );
  };
  
  export default Ternary;
    ```
- Using Logical && Operators
- Using Immediately Invoked Function
### PASSING PROPS TO A COMPONENT
- The term 'props' is an abbreviation for 'properties'
- Used for passing data from one component to another.
- Props are being passed in a uni-directional flow means one
- way from parent to child
- Props data is read-only, which means that data coming from
- the parent should not be changed by child components
### PASSING PROPS
- Passing simple data
- Passing with object data
- Passing function
  - App.jsx (Parent File)
    
      ```sh
      import { Fragment } from "react";
    import Header from "./component/Header";
    
    function App() {
      const alartFunction = () => {
        alert("Say Hello!");
      };
    
      return (
        <Fragment>
          <Header chidBtnClick={alartFunction} />
        </Fragment>
      );
    }
    export default App;
     ```
  - Header.jsx (Child File)

    ```sh
    const Header = (props) => {
      return (
        <div>
          <button onClick={props.chidBtnClick}>Submit</button>
        </div>
      );
    };
    export default Header;
    ```

### RESPONDING TO EVENTS

- Adding event handlers
  
    ```jsx
      function handleClick() {
      alert("Yor Clicked Me!");
    }
    
    const Footer = () => {
      return (
        <div>
          <button onClick={handleClick}>Click Me</button>
        </div>
      );
    };
    
    export default Footer;
  
    ```
    
- Preventing default behavior

    ```jsx
        const PostFormData = (event) => {
        event.preventDefault();
        //  todo
        alert("Your form submitted");
      };
      
      const Footer = () => {
        return (
          <div>
            <form onSubmit={PostFormData}>
              <input placeholder="name" />
              <button type="submit">Submit</button>
            </form>
          </div>
        );
      };
      
      export default Footer;
    ```

### REACT HOOK

- **useRef() Method** Changing HTML Elements

    ```jsx
      import { useRef } from "react";
      
      const Footer = () => {
        let myHeadLine = useRef();
        const change = () => {
          myHeadLine.current.innerText = "Hellow useRef";
        };
      
        return (
          <div>
            <h1 ref={myHeadLine}></h1>
            <button onClick={change}>Click</button>
          </div>
        );
      };
      
      export default Footer;

    ```

- **useRef() Method** Method Working With Attributes

     ```jsx
      import { useRef } from "react";
      
      const Footer = () => {
        let myImg = useRef();
      
        const change = () => {
          myImg.current.src = "https://placehold.co/600x400?text=Hello+World";
          myImg.current.setAttribute("height", "200px");
          myImg.current.setAttribute("weight", "300px");
        };
      
        return (
          <div>
            <img ref={myImg} src="https://placehold.co/600x400" alt="sample_img" />
      
            <button onClick={change}>Click</button>
          </div>
        );
      };
      
      export default Footer;

     ```

- **useRef() Method** Working With Input Element
  
     ```jsx
        import { useRef } from "react";
        
        function App() {
          let firstName,
            lastName,
            mobileNumber = useRef();
          const change = () => {
            let fName = firstName.value;
            let lName = lastName.value;
            let mNumber = mobileNumber.value;
        
            alert(
              "Name : " + fName + " " + lName + " , " + "Mobie Number : " + mNumber
            );
          };
        
          return (
            <div>
              <label>First Name : </label>
              <input ref={(a) => (firstName = a)} placeholder="First Name" />
              <br />
              <br />
              <label>Last Name : </label>
              <input ref={(a) => (lastName = a)} placeholder="Last Name" />
              <br />
              <br />
              <label>Mobile Number : </label>
              <input ref={(a) => (mobileNumber = a)} placeholder="Mobile Number" />
              <br />
              <br />
              <button onClick={change}>Click & Show</button>
            </div>
          );
        }
        
        export default App;

     ```

- **useRef() Method** Working With Add Remove CSS Class

   Before this method practise need install the bootstrap by npm that simplify the css. so open the vs code terminal and follow the command and run the bootstrap :

   ```sh
     npm i bootstrap@5.3.3
   ```
  After run the file then bootstrap file connect with the main.jsx file so write this code main.jsx file header section :

        ```jsx
          import "bootstrap";
          import "bootstrap/dist/css/bootstrap.css";
        ```
      
  Now practise code

  
        ```jsx
        import { useRef } from "react";
      
      function App() {
        let myHeadLine = useRef();
        const change = () => {
          myHeadLine.current.classList.remove("text-primary");
          myHeadLine.current.classList.add("text-danger");
        };
      
        return (
          <div>
            <h1 className="text-primary" ref={myHeadLine}>
              This is head line
            </h1>
            <button onClick={change}>Click & Change</button>
          </div>
        );
      }
      
      export default App;

  ```
  



























