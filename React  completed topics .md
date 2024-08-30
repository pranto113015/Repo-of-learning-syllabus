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

- **useRef() Method** Create Persisted Mutable Values

  ```jsx
    import { useRef } from "react";
    
    function App() {
      let number = useRef(0);
      const change = () => {
        number.current++;
        console.log(number.current);
      };
    
      return (
        <div>
          <button onClick={change}>Click</button>
        </div>
      );
    }
    
    export default App;

  ```

- **useRef()** Caching expensive computations

    ```jsx
          import { useRef } from "react";
          
          function App() {
            let APIData = useRef(null);
            let myPTag = useRef();
          
            const fetchhData = async () => {
              const res = await fetch("https://dummyjson.com/products");
              APIData.current = await res.json();
            };
          
            const showData = () => {
              myPTag.current.innerText = JSON.stringify(APIData.current);
            };
          
            return (
              <div>
                <p ref={myPTag}></p>
                <button onClick={fetchhData}>Call API</button> <br />
                <button onClick={showData}>Show Data</button>
              </div>
            );
          }
          
          export default App;

    ```

- **useState() Method** Counter Example

  ```jsx
  import { useState } from "react";
  
  function App() {
    const [number, setNumber] = useState(0);
    const changeNumber = () => {
      setNumber(number + 1);
    };
  
    return (
      <div>
        <h1>Number : {number}</h1>
        <button onClick={changeNumber}>Click</button>
      </div>
    );
  }
  
  export default App;

  ```

- **useState() Method** Working With Object

  ```jsx
    import { useState } from "react";
    
    function App() {
      const [myObject, setMyObject] = useState({
        key1: "Name",
        key2: "Mobile",
        key3: "Gmail",
      });
    
      const updateObject = () => {
        setMyObject((prevOBJ) => ({
          ...prevOBJ,
          key1: "Name : Pranto Kumar",
          key2: "Mobile : 01992113015",
          key3: "Gmail : pranto113015@gmail.com",
        }));
      };
    
      return (
        <div>
          <h1>{myObject.key1}</h1>
          <h1>{myObject.key2}</h1>
          <h1>{myObject.key3}</h1>
          <button onClick={updateObject}>Click</button>
        </div>
      );
    }
    
    export default App;

  ```

- **useState() Method** Todo Example

   ```jsx
       import { useState } from "react";
      
      function App() {
        const [list, setList] = useState([]);
        const [item, setItem] = useState("");
      
        const AddToList = () => {
          list.push(item);
          setList([...list]); //spread operator
        };
      
        const RemoveItem = (index) => {
          list.splice(index, 1);
          setList([...list]);
        };
      
        return (
          <div>
            <table>
              <tbody>
                {list.length !== 0 ? (
                  list.map((element, index) => {
                    return (
                      <tr>
                        <td>{element}</td>
                        <td>
                          <button
                            onClick={() => {
                              RemoveItem(index);
                            }}
                          >
                            Remove
                          </button>
                        </td>
                      </tr>
                    );
                  })
                ) : (
                  <tr></tr>
                )}
              </tbody>
            </table>
      
            <input onChange={(e) => setItem(e.target.value)} placeholder="Item" />
            <button onClick={AddToList}>Add</button>
          </div>
        );
      }
      
      export default App;

   ```

- **useState() Method** Manage Form
  
   Nedd some default css so install and import the `milligram CSS framework`(this is provide some design by default without write any css class) so follow this command :
  
   Install with npm
   ```css
   npm install milligram
   ```
   After install now go to `app.jsx` file and import this code :

     ```jsx
     import "milligram/dist/milligram.css";
     ```
    Now practise code is :
    ```jsx
      import { useState } from "react";
      
      function App() {
        let [FormObj, SetFormObj] = useState({
          fName: "",
          lName: "",
          city: "",
          gender: "",
        });
      
        const InputOnChange = (porperty, value) => {
          SetFormObj((preObj) => ({
            ...preObj,
            [porperty]: value,
          }));
        };
      
        const FormSubmit = (e) => {
          e.preventDefault();
          alert(JSON.stringify(FormObj));
        };
      
        return (
          <div className="container">
            <form onSubmit={FormSubmit}>
              <input
                onChange={(e) => {
                  InputOnChange("fName", e.target.value);
                }}
                value={FormObj.fName}
                placeholder="First Name"
              />
              <br />
              <input
                onChange={(e) => {
                  InputOnChange("lName", e.target.value);
                }}
                value={FormObj.lName}
                placeholder="Last Name"
              />
              <br />
              <select
                onChange={(e) => {
                  InputOnChange("city", e.target.value);
                }}
                value={FormObj.city}
              >
                <option value="">Choose City</option>
                <option value="Dhaka">Dhaka</option>
                <option value="Rajshahi">Rajshahi</option>
              </select>
              <br />
              <input
                onChange={(e) => {
                  InputOnChange("gender", "Male");
                }}
                checked={FormObj.gender == "Male"}
                type="radio"
                name="gender"
              />
              Male
              <input
                onChange={(e) => {
                  InputOnChange("gender", "Female");
                }}
                checked={FormObj.gender == "Female"}
                type="radio"
                name="gender"
              />
              Female
              <br />
              <button type="submit">Submit</button>
            </form>
          </div>
        );
      }
      
      export default App;

    ```
- **useEffect() Method**
  
    ```jsx
    import { useEffect } from "react";
    
    function App() {
      useEffect(() => {
        console.log("Hello useEffect");
      }, [0]);
    
      return (
        <div>
          <p>Practise of useEffect method</p>
        </div>
      );
    }
    
    export default App;
  ```

- **useEffect() Method** Fetch Example

   ```jsx
      import { useEffect, useState } from "react";
      
      function App() {
        let [data, setData] = useState();
      
        useEffect(() => {
          //JavaScript Promises s
          fetch("https://dummyjson.com/products/1")
            .then((res) => res.json())
            .then((json) => setData(json));
        }, []);
      
        return <div>{JSON.stringify(data)}</div>;
      }
      
      export default App;

   ```

- **useEffect() Method** Fetch Async Await Example

  ```jsx
    import { useEffect, useState } from "react";
    
    function App() {
      let [data, setData] = useState();
    
      useEffect(() => {
        (async () => {
          let response = await fetch("https://dummyjson.com/products/1");
          let json = await response.json();
          setData(json);
        })();
      }, []);
    
      return <div>{JSON.stringify(data)}</div>;
    }
    
    export default App;
  ```

### REACT ROUTER DOM

- The react-router package is the heart of React Router and provides all the core functionality for both react-routerdom and react-router-native.
- The react-router-dom package contains bindings for using React Router in `web applications`(this is use for web aplication).
- The react-router-native package contains bindings for using React Router in React `Native applications` (this is use for mobile aplication).

  Now we work web application so install the react-routerdom (this for web applicaton) . So follow the command to install :

  ```sh
  npm i react-router-dom
  ```

 Now practise code are : (using this practise code topics covered :BrowserRouter, Routes, Route, NavLink, ClassName, css, Component, pages and acitvelink condition by ternary operator)

 main.jsx
 ```jsx
  import { StrictMode } from "react";
  import { createRoot } from "react-dom/client";
  import App from "./App.jsx";
  import "./assets/css/style.css";
  
  createRoot(document.getElementById("root")).render(
    <StrictMode>
      <App />
    </StrictMode>
  );

 ```

 App.jsx
 ```jsx
  import { BrowserRouter, Routes, Route } from "react-router-dom";
  import Homepage from "./pages/Homepage";
  import Pofilepage from "./pages/Pofilepage";
  import Producpage from "./pages/Producpage";
  import Notfound from "./pages/Notfound";
  
  function App() {
    return (
      <div>
        <BrowserRouter>
          <Routes>
            <Route path="/" element={<Homepage />} />
            <Route path="/pofile" element={<Pofilepage />} />
            <Route path="/product" element={<Producpage />} />
            <Route path="*" element={<Notfound />} />
          </Routes>
        </BrowserRouter>
      </div>
    );
  }
  
  export default App;

 ```

  component  Menu.jsx
 ```jsx
    import React from "react";
    import { NavLink } from "react-router-dom";
    
    const Menu = () => {
      return (
        <div>
          <ul>
            <li>
              <NavLink
                className={({ isActive }) =>
                  isActive ? "active_item " : "pending_item "
                }
                to="/"
              >
                Home
              </NavLink>
            </li>
            <li>
              <NavLink
                className={({ isActive }) =>
                  isActive ? "active_item " : "pending_item "
                }
                to="/pofile"
              >
                Pofile
              </NavLink>
            </li>
            <li>
              <NavLink
                className={({ isActive }) =>
                  isActive ? "active_item " : "pending_item "
                }
                to="/product"
              >
                Product
              </NavLink>
            </li>
          </ul>
        </div>
      );
    };
    
    export default Menu;

 ```


  assets css style.css
 ```css
     .active_item {
        color: green;
    }
    
    .pending_item {
        color: red;
    }
 ```

  pages Homepage.jsx
 ```jsx
    import Menu from "../component/Menu";
    
    const Homepage = () => {
      return (
        <div>
          <Menu />
          <h1>This is home page</h1>
        </div>
      );
    };
    
    export default Homepage;

 ```



 pages Producpage.jsx
 ```jsx
    import React from "react";
    import Menu from "../component/Menu";
    
    const Producpage = () => {
      return (
        <div>
          <Menu />
          <h1>This is product page</h1>
        </div>
      );
    };
    
    export default Producpage;

 ```


 pages Pofilepage.jsx
 ```jsx
  import React from "react";
import Menu from "../component/Menu";

const Pofilepage = () => {
  return (
    <div>
      <Menu />
      <h1>This is pofile page</h1>
    </div>
  );
};

export default Pofilepage;

 ```











