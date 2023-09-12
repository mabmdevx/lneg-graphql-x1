#lneg-graphql-x1

Original Source: https://github.com/WebDevSimplified/Learn-GraphQL
Youtube: https://www.youtube.com/watch?v=ZQL7tL2S0oQ

Run the GraphQL Server
======================
node server.js

Sample Queries
==============

List of Books
-------------
query {
  books {
    id,
    name,
    author {
      id,
      name
    }
  }
}

A single book
-------------
query {
  book(id:1) {
    id,
    name,
    author {
      id,
      name
    }
  }
}

List of Authors
---------------
query {
  authors {
    id,
    name,
    books {
      id,
      name
    }
  }
}

A single author
---------------
query {
  author(id:1) {
    id,
    name
  }
}

Mutation
========

Add a book
----------
mutation {
  addBook(
    name: "XYZ Book",
    authorId: 1
  ){
    id,
    name
  }
}

Add an author
-------------
mutation{
  addAuthor(name: "James"){
    id,
    name
  }
}