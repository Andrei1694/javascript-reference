# NodeJS & Express

## Section 5
* What is Express.js ?
* Using Middleware
* Working with Requests & Responses
* Routing
* Returning HTML Pages


### What is Express.js?
It's a framework build on Node.js that let's you focus on business logic. A framework is a set of functions, tools & rules that help your application.
For parsing an incoming request we had to mannualy parse the body of the request, but with express.js we can install another package that can easily be hooked into our project that will then do the parsing for us.

### Installing express.js

Production dependancy
`javascript
npm install --save express
`
### Importing and using express

Importing express
const express = require('express');

The express package exports a function, and therefore we execute it as a function and this will initialize a new object.

const app = express();

The framework will store and manage a lot of things for us behind the scenes.

Now the app here actually also happens to be a valid request handler, so you can pass app here to create the server

const server = http.createServer(app);
server.listen(3000);

### Using Middleware
PICTURE
In the end middleware means that an incoming request is automatically funneled(canalizat) through a bunch of functions
by expressjs, so instead of just having one request handler, you will actually have a possibility of hooking in multiple
functions which the request will go through until you send a response. This allows you to split your code into multiple blocks or pieces instead of having one huge function that does everything.

app.use(middleware function);
app.use((req, res, next)=>{});
The next 
Intoarcete la clip

### How Middleware works
We should call next() if we dont send a response back to the user  because otherwise, the request will just die and will not
continue to the next middleware. Express.js dosen't send a default response.

res.send() allows instead of setting a header which we still can do and writing which we also still can do, so we can still
send responses as before but instead of doing this, there is a new utility function we can use, send. Send allows us to send a response and actually this allows us to attach a body which is of type any.

res.send("<h1>Hello</h1>);

you will see that under headers, the content type is automatically set to text html here.
So this is done for you,
this is another feature provided by express here. The send method by default here
since we send some text here simply sets an html content type,
you can still set one manually with set header of course, so you can always override this expressjs
default but you can also rely on the default where the default response header is text html.
