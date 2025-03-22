# How to Add Logging and Debugging to Node.js Applications

## 1. Adding Simple Logs with `console.log()`
For basic debugging, you can use `console.log()` to print out the values of variables, track program flow, or inspect errors.

```javascript
console.log('This is a log message!');
2. Using the winston Logging Package
Winston is a popular logging library in Node.js for more advanced logging functionality.

Install winston:
npm install winston
Set up a logger in your application:
const winston = require('winston');

const logger = winston.createLogger({
  level: 'info',
  transports: [
    new winston.transports.Console(),
    new winston.transports.File({ filename: 'combined.log' })
  ],
});

logger.info('Information message');
logger.error('Error message');

3. Debugging Node.js Code
You can use Node's built-in debugging tool by running your application with the --inspect flag:
node --inspect app.js

Open Chrome and navigate to chrome://inspect to connect to the debugger.

Use breakpoints and inspect variables to step through your code.

Troubleshooting:
If you don’t see logs in the file, ensure that the file path is correct and writable by your application.

4. After you've made sure the content is correct and complete, scroll down to the bottom and click **Commit changes**.
