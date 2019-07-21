```
# Install dependencies for server
npm install

# Install dependencies for client
npm run client-install

# Run the client & server with concurrently
npm run dev

# Run the Express server only
npm run server

# Run the React client only
npm run client

# Server runs on http://localhost:5000 and client on http://localhost:3000
```
---

Add this code into **package.json** of the client(react):
```
"proxy": "http://localhost:5000"
```
this way you don't need to put that into fetch().

---

Add this for running client(react) from the root folder in **scripts** of package.json(root level):
```
"client": "npm start --prefix client"
or
"client": "cd client && npm start"
```

---

If you want to run both the server and the client in the same time, use **npm i concurrently** and add this to package.json:
```
"dev": "concurrently \"npm run server\" \"npm run client\""
```
---
To install client dependencies (package.json scripts - root folder):
```
"client-install": "cd client && npm install",
```