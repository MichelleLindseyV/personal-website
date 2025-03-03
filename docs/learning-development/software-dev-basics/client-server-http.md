---
title: "Client-server and HTTP Basics"
description: "Overview of the client-server model and HTTP basics"
---

# Client-Server and HTTP Basics

## Client-Server Model

The client-server model is a distributed application structure that partitions tasks or workloads between the providers of a resource or service, called servers, and service requesters, called clients.

Often clients and servers communicate over a computer network on separate hardware.

A server host runs one or more server programs, which share their resources with clients.

A client usually does not share any of its resources, but it requests content from a server.

## HTTP

Hypertext Transfer Protocol is an application-layer protocol for transmitting hypermedia documents, such as HTML. It was designed for communication between web browsers and web servers.

HTTP follows a classical client-server model, with a client opening a connection to make a request, then waiting until it receives a response from the server.

### Headers

HTTP headers are used to send metadata about a resource or an HTTP message, and to describe the behavior of the client or server.

- Requset
- Response
- Representation
- Payload

### Request Methods

Request methods indicate the purpose of the request and what is expected if the request is successful.

- `GET`
- `POST`
- `PUT`
- `PATCH`
- `DELETE`

### Response Status Codes

Status codes indicate the outcome of a specific HTTP request. They are grouped into five classes:

1. Informational
2. Successful
3. Redirections
4. Client errors
5. Server errors

### MIME Types

Multipurpose Internet Mail Extenstions - indicates the nature and format of a document, file, or assortment of bytes.

A MIME type most commonly consists of a *type* and a *subtype*, separated y a slash, with no whitespace in between.

```
type/subtype
```

The *type* represents the general category into which the data type falls, such as **video** or **text**.

The *subtype* identifies the exact kind of data of the specified type the MIME type represents. For example, the type **text** can have subtypes **plain**, **html**, or **calendar**.

### Caching



## Resources

- [Client-server model](https://en.wikipedia.org/wiki/Client%E2%80%93server_model)
- 