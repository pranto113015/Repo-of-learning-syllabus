# React Project File Installation Guide 2024

### Prerequisite to install React Js :

- **Node.JS** : Node. js is not a programming language; it is a runtime environment allowing you to execute JavaScript code on the server side, outside a web browser.

  [Download Link Node v20.16.0](https://nodejs.org/dist/v20.16.0/node-v20.16.0-x64.msi)

  This is a very simple process to setup. Click the link and download this file and install to manual process.

- **VS CODE** : Visual Studio Code, also commonly referred to as VS Code, is a source-code editor developed by Microsoft for Windows, Linux, macOS and web browsers.
  
  [Download Link for windows](https://code.visualstudio.com/Download#)

  This is a very simple process to setup. Click the link and download this file and install to manual process.


### Step to install react js :

- **Vite** : Vite is an extremely fast and lightweight web application build tool.

First create vite project by vs code terminal so first go to vs code and open the terminal and write this code

  ```sh
  $ npm create vite@latest 
  ```
Then choose the project name or by default show the name `vite-project` then enter then select a framwork for example show 

  ```sh
  vanilla
  vue
  react
  preact
  lit
  svelte
  others
  ```
Now i choose React and click `Enter`

Then select a `variant for example`

  ```sh
  Typescript
  Typescript+swc
  javascript
  javascript+swc
  ```
Now i choose javascript and click `Enter`

Now again open the terminal and write the code first enty the current folder so write code

  ```sh
  cd vite-project
  ```

Now this is right folder location and again write the code 
  ```sh
  npm install
  ```
and click `Enter` now some time waiting to some file and folder `node_moduls` come this folder.
Now if i am need to run  my project then open the terminal and write the code

  ```sh
  npm run dev
  ```

Then show the live link copy the link and past the browser to show the project like
  ```sh
   VITE v5.4.1  ready in 1002 ms

  ➜  Local:   http://localhost:5173/
  ➜  Network: use --host to expose
  ➜  press h + enter to show help
  ```
Now if we need hold project convert to small  fiel size thats mins production or deploy online live server then
go to the code editor terminal and write the code 

  ```sh
  npm run build
  ```
and click `Enter` then we will see a generate another folder name `dist` there have all of the code minimize version all together now we could deploy this file online.

Now we would discuss about created default react project file and folder each & every . we see whice file need and which file don't need

This react project file starting stage path is `src/main.jsx` after visitg  `src/main.jsx` then move the `src/App.jsx`by default `src/App.jsx` have some code so don't need that's why delete this unnecessary code just need this code look like

  ```jsx
  function App() {
  
    return (
      <>
      <h1>Hello World</h1>
      </>
    )
  }
  
  export default App
  ```

Now open `src/main.jsx` and go to top and delete unnecessary linkup  `import './index.css'` and delete the `index.css` file and also delete `App.css` file.

 - Now move the `assets` folder and create `images` folder to store the all image.
 - Now create folder `css` to store css file and delete the svg image.
 - Now again create `pages` folder inside the src folder to store different pages file and again create `component` folder inside the `src` folder to store manual created component.

**Now ready by default react project file.**

### Vs code extension to easily handle the react project :

 - Auto Close Tag
 - Auto Import - ES6, TS, JSX, TSX (VSCode Extension)
 - Auto Rename Tag
 - ESLint
 - Npm Intellisense
 - Path Intellisense
 - Postman `(need sign up) Postman is a global software company that offers an API platform for developers to design, build, test, and collaborate on APIs`
 - Prettier - Code formatter
 - Reactjs code snippets
 - Snipped (take screenshoots)
 - Stylelint (identify the css error)
 - Tailwind CSS IntelliSense (suggess tailwind css class)
 - Thunder Client (help rest api and this is similar of postman)
 - VSCode React Refactor
 - vscode-icons






 















  



