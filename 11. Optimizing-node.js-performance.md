# Optimizing Node.js Application Performance

## 1. Use the `process.hrtime()` method to measure execution time
You can measure the execution time of specific code blocks using `process.hrtime()`.

```javascript
const start = process.hrtime();
// Code you want to measure
const end = process.hrtime(start);
console.log(`Execution time: ${end[0]}s ${end[1] / 1000000}ms`);
2. Avoid Blocking the Event Loop
Ensure that your Node.js app doesn’t block the event loop. Use async methods and non-blocking calls to handle tasks like file I/O or database queries.

3. Optimize Dependencies
Review your project dependencies and remove any unused packages. Use tools like npm audit to identify vulnerabilities and performance issues.

4. Use Caching to Speed Up Responses
Caching is a great way to improve performance. Use in-memory caches (like Redis) for data that's frequently accessed.

### Steps to add it:
1. Open your repository on GitHub.
2. Create a new file for **Optimizing Node.js Application Performance**.
3. Copy and paste the content provided above into the new file.
4. Commit the changes (just like we did with the other files).
