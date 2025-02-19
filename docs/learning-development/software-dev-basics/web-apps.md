---
title: "How Web Apps Work"
description: "Overview of how web applications work."
---

# How Web Apps Work

## Requests and Responses

Computers connected to the internet include clients and servers.

- **Clients:** typicl web user's internet-connected devices (laptop, phone, etc.) and web-accessing software available on those devices (typically browsers).

-**Servers:** are computers that store webpages, sites, or apps. When a client wants to access a webpage, a copy of the code is downloaded from the server onto the client machine, rendered by the browser, and displayed to the user.

- **Request:** when a device asks for a "resource," such as an image, HTML page, auth token, etc. Typicall requires some form of a connection to the internet to communicate with the server
- **Response:** a reply to the requests. When a server receives the requrest, it does something, and sends back a response. The response will containe the resource that was asked for by the client, such as HTML page, JSON data, etc. Could also contain a response communicating that the client isn't authorized to receive the resource.

## Other Important Tools

- **Internet connection:** allows data to be sent and received on the internet. 
- **Protocols:** Transmission Control Protocol (TCP) and Internet Protocol (IP) are the communication protocols that define how data should travel across the internet. Think of them like a transport mechanism.
- **Domain Name System (DNS):** it's like the address book for websites. When a web address is typed in a browser, the browser looks at the DNS for find the websites IP address - the actuall address of the server - before it can retrieve the website. The browser needs to find the server the website lives on, so it can send HTTP messages to the right place.
- **Hypertext Transfer Protocol (HTTP):** an application protocol that defines a language for clients and servers to speak to each other.
- **Files:** A website is made up of many different files (code, assets).

## DNS

Real web addresses are a series of numbers, not the memorable strings that make up a URL. This series of numbers is called an IP address and it represents a unique location on the web. The Domain Name Syste, uses special servers to match up a web address (URL) to the websites real (IP) address.

## URL Components

Uniform Resource Locators define the locations of unique resources on the internet. It is a web address plus a protocol.

The main parts include:

- **Protocol:** Such as `HTTPS`, which is the secure version of HTTP.
- **Domain Name:** Which represents the top-level location of the server you are connecting to. 
- **Path:** The path to the resource on the server that you're requestig access to.  

Proper identification of URL parts:

- **Scheme:** It is the first part of the URL that indicates which protocol the browser must use to request the resource (ex. HTTPS).
- **Authority:** It includes the domain and the port. The domain indicates which Web server is being requested (ex. www.google.com). The port indicates the technical gate used to access the resources on the web server (it is usually omitted if the web server uses the standard ports of the HTTP protocol; 80 ror 443).
- **Path to resource:** the path to the resource on the Web server.
- **Parameters:** key:value pairs that can be used to do extra things before returning the resource.
- **Anchor:** an anchor to another part of the resource itself. It represents a sort of bookmark inside the resourced, giving the browswer directions to show the content located at that bookmarked spot.

## Resources

- [Web standards](https://developer.mozilla.org/en-US/curriculum/core/web-standards/)