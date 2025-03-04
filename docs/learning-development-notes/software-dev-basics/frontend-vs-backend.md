---
title: "Frontend versus Backend"
description: "Comparing and contrasting the frontend and backend."
---

# Frontend vs. Backend

The frontend and backend are two critial parts of any application.

- Frontend includes what users can see and interact with, such as links, images, text, etc. This is what allows them to interact with an application.
- Backend is comprised of the data and infrastructure that make the application work. It is where the application stores and processes data for end users.

## Frontend

- What a user sees and interacts with. This includes things like images, banners, text, links, buttons, navidation menus, etc.
- This is also refered to as the graphical user interface (GUI).
- **Document object model (DOM):** according to MDN web docs, the DOM "is the data representation of the objects that comprise the structure and content of a document on the web."
- Frontend languages include **HTML** (page structure), **CSS** (styling), and **JavaScript** (dynamic functionality; DOM manipulation).
- Responsiveness and performance are the two main objectives of the frontend.

### Document Object Model

- A programming interface for web documents.
- Represents the page so that programs can chance the document structure, style, and content.
- The DOM represents the document as nodes and objects.
- As an object-oriented representation of the web page, it can be modified with a scripting language like JavaScript.
- The DOM is built using multiple APIs that work together.
- The DOM was designed to be independent of any particular programming language, making the structural representation of the document available from a single, consistent API.
- The `document` and `window` objects are the object interfaces you'll generally use the most often in DOM programming.
- `window` object represents something like the browser.
- `document` object is the root of the document itself.
- `element` inherits from the generic `Node` interface, and together they provide many of the methods and properties you use on individual elements.



## Backend

The backend, also refered to as the *server side*, manages a web application's overall functionality.

- When a user interacts with the frontend, a request is sent to the backend in HTTP format, where it then processes the request and returns a response.

When processing a request, the backend generally interacts with:

- Database servers to retrieve or modify relevant data
- Microservices that perform a subset of the tasks your user requested.
- Third-party APIs to gather additional information or perform additional functions.

### HTTP

According to MDN, "HTTP is a protocol for fetching resources such as HTML documents. It is the foundation of any data exchange on the Web and it is a client-server protocol, which means requests are initiated by the recipient, usually the Web browswer. A complete document is typically constructed from resources such as text content, layout instructions, images, videos, scripts, and more."

- Messages sent by the *client* are called *requests*.
- Messages send by the *server* are called *responses*.

**HTTP requests consist of:**
- HTTP methods; `GET`, `POST`, `OPTIONS`, `HEAD`.
- The path of the resource to fetch.
- The version of the HTTP protocol.
- Optional headers that convey additional information for the servers.
- A body, for some methods like `POST`, which contain the resource sent.

**HTTP responses consist of:**
- The version of the HTTP protocol they follow.
- A status code, indicating if the request was successful or not, and why.
- A status mesage, a non-authoritative short description of the status code.
- HTTP headers, like those for requests.
- Optionally, a body containing the fetched resource.



#### HTTP Flow

1. **Open a TCP connection.** The TCP connection is used to send a request, or several, and receive an answer. The client may open a new connection, reuse an existing connection, or open several TCP connections to the servers.

2. **Send an HTTP message.** HTTP messages are human-readable. With HTTP/2, these simple messages are encapsulated in frames, making them impossible to ready directly, but the principle remains the same.

3. **Read the response sent by the server.**

4. **Close or reuse the connection for further requests.**

### Concurrency

The backend often needs to handle thousands of requests simultaneously. 

Several strategies include:

- **Multi-threading** to manage CPU processing of tasks.
- **Asynchronous programming**, such as callbacks and promises.
- **Event-driven programming**, where the backend listens to multiple events and runs the appropriate even handlers concurrently.
- **Locking and synchronization techniques** so multiple users can access the same resource simultaneously without inconsistencies.



## Comparisons

### Caching

Caching temporarily stores copies of application files, making them easier to retrieve the next time they're needed. It can be used to improve an application's load time and performance.

- **Frontend:** the client application caches data like a header image the first time a user access it. The next time, the frontend loads the cached files to improve performance.
- **Bakcend:** caching is used to reduce the load on the application server. What you store in the backend cache depends on the application. Cached content includes static pages, database query results, API responses, session data, images, and videos.

## References

- [Frontend VS Backend - What's the Difference?](https://www.freecodecamp.org/news/frontend-vs-backend-whats-the-difference/)
- [What's the Difference Between Frontend and Backend in Application Development?](https://aws.amazon.com/compare/the-difference-between-frontend-and-backend/)
- [Front-End vs. Back-End: What's the Difference?](https://www.computerscience.org/bootcamps/resources/frontend-vs-backend/)
- [Frontend vs Backend](https://www.geeksforgeeks.org/frontend-vs-backend/)
- [Introduction to the DOM](https://developer.mozilla.org/en-US/docs/Web/API/Document_Object_Model/Introduction)
- [An overview of HTTP](https://developer.mozilla.org/en-US/docs/Web/HTTP/Overview)