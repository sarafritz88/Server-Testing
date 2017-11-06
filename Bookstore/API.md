Bookstore API

Book

Represents book details.

Book attributes:

id (String): Unique Identifier
title (String): Book Title
author (String): Author Name
year (Number): Publication Year
isbn (String): ISBN
pages (Number): Number of Pages
genre (Array(String)): List of Genres
Book Collection

Get All Books

GET /books

Response

Status: 200

[
  {
    "_id": "12345",
    "title": "The Hitchhiker's Guide to the Galaxy",
    "author": "Douglas Adams",
    "year": 1979,
    "pages": 180,
  },
  {
    "_id": "12346",
    "title": "Garden's of the Moon",
    "author": "Steven Erikson",
    "year": 1999,
    "pages": 712,
  },
  ...
]
Create a Book

POST /books

Request

Body

{
  "title": Deadhouse Gates",
  "author": "Steven Erikson",
  "year": 2000,
  "pages": 943,
}
Response

Status: 200

{
  "id": "12345"
  "title": "Deadhouse Gates",
  "author": "Steven Erikson",
  "year": 2000,
  "pages": 943,
}
Book

A single a Book object

Get a Single Book

GET /books/:id

Parameters

id	String	A hexadecimal string ID of the book to get
Response

Status: 200

{
  "id": "12345"
  "title": "Deadhouse Gates",
  "author": "Steven Erikson",
  "year": 2000,
  "pages": 943,
}
Status: 404

{
  "error": "Book not found"
}
Update a Book

PUT /books/:id

Parameters

id	String	A hexadecimal string ID of the book to get
Request

Body

{
  "title": "The Grapes of Wrath",
  "author": "John Steinbeck",
  "year": 1939
}
Response

Returns the updated entry

Status: 200

{
  "title": "The Grapes of Wrath",
  "author": "John Steinbeck",
  "year": 1939,
  "pages": 464,
}
Status: 404

{
  "error": "Book not found"
}
Delete a Book

DELETE /books/:id

Parameters

id	String	A hexadecimal string ID of the book to get
Response

Status: 200
{
  "success": "Deletion successful"
}
Status: 404
{
  "error": "Book not found"
}
