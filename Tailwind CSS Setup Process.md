# Tailwind CSS Environment Setup


### Prerequisite :
Tailwind CSS requires **Node.js 12.13.0 or higher**.


### Using PostCSS
Now follow this step :

**Step 1 :** First Created the project name folder then open this folder by visual studio code editor then writing the following code visual studio code terminal.

```sh
npm init -y
```
After execute this command automatic will created the `package.json` file

**Step 2 :**   

```sh
npm install -D tailwindcss postcss autoprefixer vite
```
After execute this command automatic will created the file `package-lock.json` and folder `node_modules`

**Step 3 :**   

```sh
npx tailwindcss init
```
After execute this command automatic will created the file `tailwind.config.js` 

**Step 4 :**   

```sh
npx tailwindcss init -p
```
After execute this command automatic will created the file `postcss.config.js` 

**Step 5 :** Open the `tailwind.config.js` file and customize this line `content: ["./src/**/*.{html,js}"],` code. This is actually used for  location what file use tailwind css.

```sh
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{html,js}"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

**Step 5 :** Now we will create the `main.css` file inside the project folder. After completing this css file copy this code.

```sh
@tailwind base;
@tailwind components;
@tailwind utilities;
```

**Step 6 :** Now open the `package.json` file then go to the scripts key and create the new key look like bellow :

```sh
"scripts": {
 "start": "vite"
 },
```

**Step 7 :** Now we will create the `index.html` file inside the project folder then make the html boilerplate and link up the css file inside the header section look like bellow :

```html
<!doctype html>
<html>
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Using PostCSS</title>
  <link href="./main.css" rel="stylesheet">
</head>
<body>
  <h1 class="text-3xl font-bold underline">
    Hello world!
  </h1>
</body>
</html>
```

**Step 8 :** Now if you run the project then go to terminal and write the command.

```sh
npm start
```
After execute this command will provide the local port address. Now click address will open the project by default browser. `Done`










