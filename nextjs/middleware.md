A little walkthrough of expressJS first, although it is not used in Next much because of api routes in next js 14
- step - 1 ( Require Express )
`
const express = require('express');
`
- step - 2 (**create an install of express function**)
`
const app = express();
`
>The `express()` function returns a new instance of the Express application. This instance represents your web server and is used to define routes, middleware, and handle HTTP requests and responses.

You can think of `app` as your main application object. You'll use methods and properties on this object to configure routes, set up middleware, and define how your server should respond to different types of HTTP requests.

```
const express = require('express');
const app = express();

// this is a route handler ( agar 'GET' req hai toh kaise react krna hai )

app.get('/', (req, res) => {
  res.send('Hello, World!');
});

const port = 3000;
app.listen(port, () => {
  console.log(`Server listening on port ${port}`);
});

```