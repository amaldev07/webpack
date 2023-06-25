# webpack

do npm init to create package.json file
install web pack
    npm install webpack --save --dev
    --save --dev -> uses b/z webpack we dont need it for production, it is a development only dependency 

add the webpack build script to package.josn script section
"build": "webpack ./src/js/app.js -o dist/"
["build": "webpack src/js/app.js dist/bundle.js" 
this will give error as we didnt mention outputusing -o]
where  
    entry point=> src/js/app.js
    output path=> dist/ => it will automatically create a main.js file ins ide dist folder

So your script tab in package.json will be 
  "scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "build": "webpack ./src/js/app.js -o dist/"
  },

---------------------------
refer this bundle/main.js in html file instead of app.js and dom-loader.js
<!-- <script src="src/js/dom-loader.js"></script> -->
<!-- <script src="src/js/app.js"></script> -->
<script src="dist/main.js"></script>


