# Express Tutorial

Express can be used to handle requests to the api of our application, it can also be used as middleware which could help us to pass json to the front end of the application.



Each express file requires the following head segment:

```
const express = require("express")
```



To make a new route, a route must be specified in the server.js file like:

```
const exampleRouter = require("./routes/example")
app.use("/example", exampleRouter)
```





And create a matching new file in the routes folder with the name of your route (in this case example). 

In this file you need to add the header segment above as well as declare the router:

```
const express = require ('express')
const exampleRouter = express.Router()
```



At the end of the file you must export it:

```
module.exports = exampleRouter
```



In this file you can specify new methods for the api related to the pathway. This is done in the following format:app.get("/test1", (req, res) => {

```
    const test1 = {

    "text" : "Hello World"

    }

    res.send(test1)

})



App.[request type](“path from route”, (req, res, next(optional)) => {

    *method*

}
```


Req contains info from the request

Res contains info regarding to the response



You can use <:text> to specify a path that will take some argument in the path such as in the following example if i used the path localhost:3000/test2/1, then the output json would contain 1. The statement re1.params.`<id>` will get you the value from the path with tag id.

```
app.get("/test2/:id", (req, res) => {

    const test2 = {

    "text" : req.params.id

    }

    res.send(test2)

})
```


If you want more detailed explanation, i found the following sources helpful:

10min:

[RESTful APIs in 100 Seconds // Build an API from Scratch with Node.js Express](https://www.youtube.com/watch?v=-MTSQjw5DrM)

30min:

[Build A REST API With Node.js, Express, &amp; MongoDB - Quick](https://www.youtube.com/watch?v=fgTGADljAeg&t=371s)

1hr:

[How to build a REST API with Node js &amp; Express](https://www.youtube.com/watch?v=pKd0Rpw7O48&t=1699s)

**
