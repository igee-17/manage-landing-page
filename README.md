```js
npm init
```
- creates package.json

- next install tailwind as a devDependency

```js
 npm install -D tailwindcss
```

- create tailwind.config.js file by:

```js
 npx tailwindcss init
```
- edit config file to specify where to look for tailwind classes

```js
 module.exports = {
  content: ["./*.html"],
  theme: {
    extend: {},
  },
  plugins: [],
};
```
- "./*.html" means all html files in root folder

- create 'input.css' file and add:

```js
 @tailwind base;
 @tailwind components;
 @tailwind utilities;
```
- in package.json, under scripts:

```js
 "scripts": {
    "build": "tailwindcss -i ./input.css -o ./css/main.css",
    "watch": "tailwindcss -i ./input.css -o ./css/main.css --watch"
  },
```


- in config file, screen sizes and default colors can be specified:

```js
 module.exports = {
  content: ["./*.html"],
  theme: {
    screens: {
      sm: "480px",
      md: "768px",
      lg: "976px",
      xl: "1440px",
    },
    extend: {
      colors: {
        brightRed: "hsl(12, 88%, 59%)",
      },
    },
  },
  plugins: [],
};

```
-----------------------------------------------------------------------------

TAILWIND CLASSES

- relative : sets poition to relative

- container : sets width of div to current viewport

- mx-auto : sets margin on x-axis left and right to auto

- p-6 : sets padding of 1.5rem (24px)

- flex : sets display to flex

- items-center : sets 'align-items' to 'center'

- justify-between: sets 'justify-content' to 'between'

- pt-2: sets 'padding-top' to '0.5rem' (8px)

- space-x-6 : sets 'margin-right' and 'margin-left' to 1.5rem, of children elements in a container

- class="hidden md:flex" : sets 'display' to hidden, then to flex on middle screen

- hover:text-red : sets 'hover' pseudoClass to 'color' 'red'

- rounded-full : sets 'border-radius' to '99999px'

- rounded-l-full : sets 'border-top-left-radius' and 'border-bottom-left-radius' to '99999px'

- max-w-sm : sets 'max-width' to '24rem'

- class="md:w-1/2" : on medium screen layout, sets 'width' to '50%'








