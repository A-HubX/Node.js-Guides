# How to Install and Set Up Node.js

## Prerequisites:
- Windows, macOS, or Linux
- Internet connection

## Steps:
### 1. Install Node.js
Visit the [official Node.js website](https://nodejs.org/en/) and download the LTS version for your operating system.
### 2. Verify Installation
After installation, open your terminal or command prompt and type the following command to check if Node.js and npm (Node Package Manager) are installed correctly:

node -v npm -v

You should see the installed version of both Node.js and npm.

### 3. Create a Simple Node.js Server
1. Create a new directory for your project:
mkdir my-node-server cd my-node-server

2. Initialize a new Node.js project:
npm init -y

3. Create a file called `app.js` and add the following code to start a basic HTTP server:
```javascript
const http = require('http');

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello, World!\n');
});

server.listen(3000, () => {
  console.log('Server running at http://localhost:3000/');
});
4. Run the server:
node app.js
You can now open your browser and visit http://localhost:3000/ to see the message "Hello, World!"

Troubleshooting:
Node.js not recognized: Ensure you’ve added Node.js to your system’s PATH.

---

### **2. Troubleshooting Node.js Issues**

**Goal:** Show you know how to troubleshoot **Node.js** issues, which will be useful in a technical support role.

**Document Name:** "Troubleshooting Common Node.js Issues"

**Content:**
- Common errors and how to fix them (like module not found, port already in use, etc.)
- Solutions to some of the most frequent Node.js problems.

**Example Markdown:**
```markdown
# Troubleshooting Common Node.js Issues

## 1. Error: "Cannot find module"
### Solution:
This error occurs when you try to require a module that hasn’t been installed or is missing. 
To resolve:
- Ensure the module is installed using `npm install <module-name>`.
- If it’s a custom module, verify the file path is correct.

## 2. Error: "Port is already in use"
### Solution:
This error occurs when the port you are trying to bind your server to is already in use by another process.
To resolve:
- Kill the process using the port:
  - **Linux/macOS:** `lsof -i :<port_number>`
  - **Windows:** Use Task Manager to end the process.
- Change the port in your application’s code to another available port.

## 3. Error: "npm ERR! code EACCES"
### Solution:
This error occurs when there are permission issues while installing packages globally.
To resolve:
- Run the install command with elevated permissions:
  - **Linux/macOS:** `sudo npm install -g <package-name>`
