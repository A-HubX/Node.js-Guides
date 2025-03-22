1. Introduction to Node.js Modules
Node.js modules allow you to organize your code into reusable components. Modules in Node.js are key to making your code cleaner, more modular, and easier to maintain. Every file in Node.js is treated as a module, and you can export and import values between them.

2. Creating a Simple Module
To create a basic module, you use module.exports to export functionality from a file.

Example: 
// mathModule.js
module.exports.add = function(a, b) {
   return a + b;
};

3. Importing a Module
You can import a module into another file using require().

Example:
const math = require('./mathModule');
console.log(math.add(2, 3));  // Output: 5

4. Built-in Node.js Modules
Node.js comes with several built-in modules that you can use without needing to install anything. Common built-in modules include fs (file system), path, and http.

Example (using fs):
const fs = require('fs');
fs.readFile('file.txt', 'utf8', (err, data) => {
    if (err) throw err;
    console.log(data);
});

5. Creating an HTTP Server
Using the built-in http module, you can create a simple server.

Example:

const http = require('http');
const server = http.createServer((req, res) => {
    res.write('Hello, Node.js!');
    res.end();
});

server.listen(3000, () => {
    console.log('Server running on port 3000');
});

6. Exporting Multiple Functions or Objects
You can export multiple functions or objects from a single module.

Example:
// operations.js
module.exports = {
   add: function(a, b) {
       return a + b;
   },
   subtract: function(a, b) {
       return a - b;
   }
};

7. Using Third-Party Modules
You can install and use third-party modules via npm. For example, lodash is a popular utility library.

To install lodash, run:
npm install lodash

Then, you can use it as follows:
const _ = require('lodash');
console.log(_.capitalize('hello'));  // Output: 'Hello'

8. Module Caching
Node.js caches modules after they are loaded for the first time, ensuring they are executed only once during the application's lifetime. This mechanism prevents performance overhead by not reloading the same module multiple times.
