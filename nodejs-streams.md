Node.js Streams
Node.js streams are a powerful way to handle large amounts of data efficiently. They allow you to process data as it is being read or written, rather than loading it all into memory at once.

Types of Streams:
Readable Streams: These streams are used to read data (e.g., fs.createReadStream).

Writable Streams: These streams are used to write data (e.g., fs.createWriteStream).

Duplex Streams: These streams can be both readable and writable (e.g., TCP sockets).

Transform Streams: These streams can modify the data as it is being read or written (e.g., compression or encryption streams).

Example Code: Creating a Readable Stream
const fs = require('fs');

// Create a readable stream
const readableStream = fs.createReadStream('input.txt', 'utf8');

readableStream.on('data', (chunk) => {
  console.log(`Received chunk: ${chunk}`);
});

readableStream.on('end', () => {
  console.log('Finished reading file');
});

Best Practices:
Always handle errors with .on('error', callback) to prevent unexpected crashes.

Use pipe() method for piping data between streams, which is efficient and easy to manage.
