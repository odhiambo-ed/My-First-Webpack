# My-First-Webpack
This is my first Webpack app
## Getting Started
1. Run `mkdir webpack` to create webpack dir.
2. Change dir `cd webpack`
3. Run `npm init -y` to create `package.json` file
4. Run `npm install webpack webpack-cli --save-dev` to instal webpack
5. In package.json file remove `"main": "index.js",`
6. In package.json file add `"private": true,`
7. Add `import _ from 'lodash';` on `index.js` file.
8. Add `<script src="main.js"></script>` in `index.html` file.
9. Run `npm install --save lodash`
10. Run `npx webpack`, which will take our script at `src/index.js` as the entry point, and will generate `dist/main.js` as the output.

### Using a Configuration
11. Create `webpack.config.js` file in the root directory.
12. Paste the code below in the `webpack.config.js` file
```
const path = require('path');

module.exports = {
  entry: './src/index.js',
  output: {
    filename: 'main.js',
    path: path.resolve(__dirname, 'dist'),
  },
};
```
13. Run `npx webpack --config webpack.config.js`

### NPM Scripts
14. Add this line `"test": "echo \"Error: no test specified\" && exit 1",` in package.json file.
14. Remove this line `"test": "echo \"Error: no test specified\" && exit 1"` in package.json file.
16. Add this line `"build": "webpack"`
17 Lastly run this `npm run build` and see if your code is running.
