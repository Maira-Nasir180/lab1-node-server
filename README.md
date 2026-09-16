# lab1-node-server
# Node.js Server Setup - Lab 1

## 1. Introduction
This project demonstrates the setup of a basic web server using Node.js that displays "Hello Javascript" in the browser. It serves as a foundation for building scalable backend applications.

## 2. Check Prerequisites
The Node.js and npm versions were verified using the following commands to confirm proper installation:
<img width="413" height="196" alt="Screenshot 2026-09-16 090158" src="https://github.com/user-attachments/assets/28372047-3556-44a1-9fcd-4c85243fb229" />
## 3. Create Project Folder & Initialize Project

A dedicated project directory named `lab1` was created, and the project was initialized using `npm init -y`, which generated a `package.json` file. The server was then started using `node server.js`, and the terminal confirmed: "Server is running on port 3000".

<img width="429" height="334" alt="Screenshot 2026-09-16 090217" src="https://github.com/user-attachments/assets/d760a671-d511-4228-8831-fd018714ffc7" />

## 4. Create Server File (server.js)

A file named `server.js` was created containing the server logic. This code sets up an HTTP server that responds with "Hello Javascript":

```javascript
const http = require('http');
const PORT = 3000;
const server = http.createServer((req, res) => {
  res.writeHead(200, { 'Content-Type': 'text/html' });
  res.end('<h1>Hello Javascript</h1>');
});
server.listen(PORT, () => {
  console.log('Server is running on port 3000');
});
```

<img width="709" height="332" alt="Screenshot 2026-09-16 090230" src="https://github.com/user-attachments/assets/21db369f-f593-4dd6-9246-cf0566812b2c" />

## 5. Test in Browser

The server was tested by navigating to `http://localhost:3000` in the browser, where the message "Hello Javascript" was successfully displayed.

<img width="363" height="250" alt="Screenshot 2026-09-16 090253" src="https://github.com/user-attachments/assets/77e52724-45a7-4b72-a113-db5e0c88483e" />

## 6. Stopping the Server

The server was stopped by pressing `Ctrl + C` in the terminal window, which terminated the process and closed the server connection.

## Project Files

- `server.js` — Contains the server logic
- `package.json` — Contains project configuration and dependencies
