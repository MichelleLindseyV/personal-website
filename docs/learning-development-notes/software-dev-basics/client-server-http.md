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

HTTP cache stores a response associated with a request and reuses the stored response for subsequent requests.

Two main types of caches: **private caches** and **shared caches**.

- **Private cache:** a cache tied to a specific client - typically a browser cache.
- **Shared cache:** shared cache is located between the client and the server and can store responses that can be shared among users. Can be futher broken down into **proxy caches** and **managed caches**.

- **Proxy cache:** some proxies implement caching to reduce traffic out of the network. Must be controlled by appropriate HTTP headers, etc.
- **Managed cache:** explicitly deployed by service developers to offload the origin server and deliver content efficiently. Ex. revers proxies, CDNs, and service workers in combination with the Cache API. In most cases you can control the cache's behavior through the Cache-Control header and your own config files.

### Authentication

HTTP provides a general framework for access control and authentication.

**RFC 7235** define the HTTP authentication framework, which can be used by a server to challenge a client request and by a client to provide authentication information.

**Challenge and response flow:**

1. The server responds to a client with a 401 response status and provides information on how to authorize with a `WWW-Authenticate` response header containing at least one challenge.
2. A client that wants to authenticate itself with the server can then do so by including an `Authorization` request header with the credentials.
3. Usually a client will present a password prompt to the user and will then issue the request including the correct `Authorization` header.

**WWWW-Authenticate and Proxy-Authenticate headers:**

The `WWWW-Authenticate` and `Proxy-Authenticate` response headers define the authentication method that should be used to gain access to a resource. They specify which authentication scheme is used, so that the client trying to authorize knows how to provide the credentials.

```http
WWW-Authenticate: <type> realm=<realm>
Proxy-Authenticate: <type> realm=<realm>
```

`<type>` is the authentication scheme. `realm` is used to describe the protected area or to indicate the scope of protection.

Some common authentication schemes include:

- Basic
- Bearer
- Digest
- HOBA
- Mutual
- Negotiate/NTLM
- VAPID
- SCRAM
- AWS4-HMAC-SHA256

### Cookies

A cookie is a small piece of data a server sends to a user's web browswer. The browser can store cookies, create new cookies, modify existing ones, and send them back to the same server with later requests.

Cookies enable web applications to store limited amounts of data and remember state information.

Typically, a server will use the contents of HTTP cookies to determine whether different requests come from the same browser/user and then issue a personalized or generic response as appropriate.

**Cookies are mainly used for:**

- **Session management:** user sign-in status, shopping cart contents, game scores, or other user session-related details that the server needs to remember.
- **Personalization:** user preferences such as display language and UI theme.
- **Tracking:** recording and analyzing user behavior.

Today, modern storage APIs are recommended, such as the **Web Storage API (`localStorage` and `sessionStorage`) and IndexedDB. They are designed with storage in mind, never send data to the server, and don't come with other drawbacks of using cookies for storage.



## Resources

- [Client-server model](https://en.wikipedia.org/wiki/Client%E2%80%93server_model)
- 