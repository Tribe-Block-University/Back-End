# Tribe Block ExpressJS Tutorial

Welcome to the **ExpressJS** tutorial! In this comprehensive guide, we will cover everything you need to know to get started with ExpressJS, a minimal and flexible Node.js web application framework.

## Table of Contents

1. [Introduction to ExpressJS](#introduction-to-expressjs)
2. [Setting Up Your Project](#setting-up-your-project)
3. [Basic Routing](#basic-routing)
4. [Middleware in Express](#middleware-in-express)
5. [Handling HTTP Requests](#handling-http-requests)
6. [Serving Static Files](#serving-static-files)
7. [Error Handling](#error-handling)
8. [Connecting to Databases](#connecting-to-databases)
9. [Best Practices](#best-practices)
10. [Additional Resources](#additional-resources)

---

## Introduction to ExpressJS

ExpressJS is a fast, unopinionated, and minimalist web framework for Node.js that allows you to build web applications and APIs with ease. It is widely used for building server-side applications in Node.js and is the foundation for many popular web frameworks.

For more information on ExpressJS, you can refer to the [official documentation](https://expressjs.com/).

---

# Setting Up Your Project

### 1. Install Node.js and NPM
Before you begin, ensure you have **Node.js** and **npm** (Node Package Manager) installed. You can download Node.js from [here](https://nodejs.org/).

To check if Node.js and npm are installed, run the following commands in your terminal:
```
node -v
npm -v
```

## Initialize a New Project
Create a new directory for your project and initialize it using npm:
```red
mkdir my-express-app
cd my-express-app
npm init -y
```
## Install Express
Now, install ExpressJS as a dependency:
```
npm install express
```
## Create Your First Express App
Create a file named app.js in your project directory:
```
// app.js
const express = require('express');
const app = express();
const port = 3000;

app.get('/', (req, res) => {
  res.send('Hello World!');
});

app.listen(port, () => {
  console.log(`Server listening at http://localhost:${port}`);
});
```

## Run the App
### Start your application:
```
node app.js
```
Visit http://localhost:3000 in your browser to see the result.

# Basic Routing
Express uses routing to map HTTP requests to specific routes (endpoints) and define how they should be handled. In this section, we'll learn how to create routes and handle HTTP requests.
## Example: Handling GET and POST Requests
```
// Handling GET Request
app.get('/home', (req, res) => {
  res.send('Welcome to the Home Page');
});

// Handling POST Request
app.post('/submit', (req, res) => {
  res.send('Data submitted successfully');
});
```

## Route Parameters
Express allows you to define dynamic routes using route parameters.
```
app.get('/user/:id', (req, res) => {
  const userId = req.params.id;
  res.send(`User ID is: ${userId}`);
});
```

# Middleware in Express
Middleware functions are used to modify the request and response objects before passing them to the next handler in the stack.

## Example: Simple Middleware
```
// Middleware function
app.use((req, res, next) => {
  console.log('A request was made to the server');
  next(); // Proceed to the next middleware/route
});
```

## Using Built-in Middleware
Express includes several built-in middleware functions, such as express.json() to parse incoming JSON requests.
```
app.use(express.json());
```

# Handling HTTP Requests
## Request Object
The req object provides information about the HTTP request, such as headers, body, query parameters, and more.
```
app.get('/greet', (req, res) => {
  const name = req.query.name || 'Guest';
  res.send(`Hello, ${name}!`);
});
```

## Response Object
The res object is used to send a response back to the client.
```
app.get('/json', (req, res) => {
  res.json({ message: 'This is a JSON response' });
});
```

# Serving Static Files
Express can serve static files like images, stylesheets, and JavaScript files using the built-in express.static middleware.

## Example:
```
app.use(express.static('public'));
```
Now, you can store your static files (like images, CSS files) in the public folder, and they will be accessible by the browser.

# Error Handling
Error handling in Express can be done using middleware.

## Example: Basic Error Handling Middleware
```
// Catch-all error handler
app.use((err, req, res, next) => {
  console.error(err.stack);
  res.status(500).send('Something went wrong!');
});
```

# Connecting to Databases
Express is commonly used to build APIs that interact with databases. In this section, we'll connect to a MongoDB database using Mongoose.

## Example: Connecting to MongoDB
```
npm install mongoose
```
```
const mongoose = require('mongoose');

mongoose.connect('mongodb://localhost/my_database', { useNewUrlParser: true, useUnifiedTopology: true })
  .then(() => console.log('Connected to MongoDB'))
  .catch(err => console.log('Failed to connect to MongoDB:', err));
```

# Best Practices
* Use Environment Variables: Store sensitive information (like API keys and database URIs) in environment variables.
* Modularize Your Code: Break your code into smaller, reusable modules.
* Error Handling: Always handle errors properly to avoid crashes.
* Use Asynchronous Code: Avoid blocking the event loop with synchronous code.

# Additional Resources
* [MDN Web Docs: Express](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Express)
* [Official Express Documentation](https://expressjs.com/)
* [Node.js Documentation](https://nodejs.org/en/docs/)

Happy coding! 🎉
