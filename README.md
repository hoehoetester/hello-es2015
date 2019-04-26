## Aad `package.json` file and initialize it

`yarn init -y`

## Add webpack

Add webpack modules follow

- webpack
- webpack-cli
- webpack-dev-server

`yarn add webpack webpack-cli webpack-dev-server -D`

## Add scripts to `package.json` file

```json
// package.json

...
"scripts": {
    "start": "webpack-dev-server --hot --inline --watch-content-base --content-base dist/ --open-page index.html"
}
...
```

## Add ES2015

Add babel dev moduels follow

- @babel/core
- @babel/polyfill
- @babel/preset-env

`yarn add -D @babel/core @babel/polyfill @babel/preset-env`

Create `.babelrc` file

```
// .babelrc

{
    "presets": ["@babel/preset-env"]
}
```

## Add `src` directory then add `index.js` and `helper.js`

```javascript
// index.js

import { log } from "./helper";

log("Hello World");
```

```javascript
// helper.js

export const log = msg => console.log(msg);
```

## Create `dist` directory and add `index.html`

```html
<!-- index.html -->

<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta http-equiv="X-UA-Compatible" content="ie=edge" />
    <title>Document</title>
  </head>

  <body>
    <script src="./main.js"></script>
  </body>
</html>
```

## Run scripts

`yarn start`
