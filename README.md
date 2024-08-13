RESTful API server with two endpoints
Create the data.
Write a handler to return all items.
Write a handler to add a new item.
Write a handler to return a specific item.

#API endpoints
/books

1.
GET – Get a list of all books, returned as JSON.
POST – Add a new book from request data sent as JSON.
/books/:id

GET – Get an book by its ID, returning the book data as JSON.

go mod init - creates a go.mod file where dependencies will be listed for tracking.

2.
design data structures for handling data.
nb:  storing data in memory means that the set of albums will be lost each time server stops, then recreated when server starts.
Logic to prepare a response
Code to map the request path to your logic

gin.Context is the most important part of Gin. It carries request details, validates and serializes JSON.
Call Context.IndentedJSON to serialize[convert an object into that string] the struct into JSON and add it to the response.
