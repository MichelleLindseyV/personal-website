---
title: "How Web Apps Work"
description: "Overview of how web applications work."
---

# How Web Apps Work

## How the Web Works

### Requests and Responses

Computers connected to the internet include clients and servers.

- **Clients:** typicly web user's internet-connected devices (laptop, phone, etc.) and web-accessing software available on those devices (typically browsers).

- **Servers:** are computers that store webpages, sites, or apps. When a client wants to access a webpage, a copy of the code is downloaded from the server onto the client machine, rendered by the browser, and displayed to the user.

- **Request:** when a device asks for a "resource," such as an image, HTML page, auth token, etc. Typicall requires some form of a connection to the internet to communicate with the server
- **Response:** a reply to the requests. When a server receives the requrest, it does something, and sends back a response. The response will containe the resource that was asked for by the client, such as HTML page, JSON data, etc. Could also contain a response communicating that the client isn't authorized to receive the resource.

### Other Important Tools

- **Internet connection:** allows data to be sent and received on the internet. 
- **Protocols:** Transmission Control Protocol (TCP) and Internet Protocol (IP) are the communication protocols that define how data should travel across the internet. Think of them like a transport mechanism.
- **Domain Name System (DNS):** it's like the address book for websites. When a web address is typed in a browser, the browser looks at the DNS for find the websites IP address - the actuall address of the server - before it can retrieve the website. The browser needs to find the server the website lives on, so it can send HTTP messages to the right place.
- **Internet Service Provider (ISP)**: the middle man between the client and the servers. It's usually a "cable company". It's their job to do the DNS lookup to ask what IP site you're trying to visit is configured to.
- **Hypertext Transfer Protocol (HTTP):** an application protocol that defines a language for clients and servers to speak to each other.
- **Files:** A website is made up of many different files (code, assets).

### DNS

Real web addresses are a series of numbers, not the memorable strings that make up a URL. This series of numbers is called an IP address and it represents a unique location on the web. The Domain Name Syste, uses special servers to match up a web address (URL) to the websites real (IP) address.

### URL Components

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

### How a Webpage is Retreived and Displayed

1. You type a URL inot your browser
2. The browswer parses the information containd in the URL, including the protocol, domain name, and the resource.
3. The browser communicates with your ISP to do a DNS lookup of the IP address for the web server that hosts the URL. DNS contacts a Root Name Server which replies with the IP address of a name server. This address is sent back to your DNS service, which does another outreach to the ".com" name server.
4. Once the ISP receives the IP address of the destination server, it send it to your web browser.
5. Your browswer taks the IP address and the given port number from the URL and opens a TCP socket connection. The web browser and server are finally connecgted.
6. Your web browswer sends an HTTP requrest to the web server for the main HTTP web page if the given URL.
7. The web server receives the request and looks for that HTML page. If the page exists, the server prepares the response and sends it back to your browswer. Otherwise, returns 404 error, "Page Not Found".
8. Your web browser takes the HTML page it receives and then parses through it doing a full head to toe scan looking for other assets that are listed, such as images, CSS files, JavaScript files, etc.
9. For each asset listed, the browser repeats the entire process, making additional HTTP requests to the server of each resource.
10. Once the browser has finished loading all of the other assets that were listed in the HTML page, the page will finally be loaded in the browswer window and the connection closed.

#### Rendering

Browswers have a rendering engine responsible for displying the content of a web page. The rendering enging receives the content of the resources and then an HTML parsing algorithm tells the browswer how to parse the resources. Once parsed, it generates a tree structure of the DOM elements. The nodes of the DOM tree can be manipulated using a scripting language like JavaScript.

### Domain Names

Domain names provide a human readable address for any web server available on the internet.

- **Top-Level Domain (TLD):** TLDs tell users the general purpose of the service behind the domain name. Examples include `.com`, `.org`, `.net`, and so on. Some TLDS like the previous onese listed on't have to meet any particular criteria, but there are coundtry specific TLDs, like `.us`, `.fr`, which can require the service be hosted in the given country or provided in a specific language, or organization specific like `.gov` or `.edu`.

- Using your systems shell you can verify a domain by entering `whois` followed by the `domain-name`. For example:

```bash
whois google.com
```

### Intro to Publishing a Website

Most companies will buy web hosting and a domain name. Web hosting is rented file space on a hosting company's web server. You put website files on their server and the server provides website content to website visitors. A sdomain name is the unique web address that you can rent for as many years as you like from a domain registrar.

If your hosting and domain are from separate companies, you'll need to do some work to point the domain name to the correct server. Generally, this means logging into your domain registrar's website and setting your domain's nameservers to the ones provided by your hosting company.

#### GitHub or Google App

Both provide you the ability to publish your website.

- GitHub offers GitHub Pages
- Google App Engine is a powerful platform that lets you build and run applications on Google's infrastructure.

## HTML, CSS, JavaScript



## Web Standards Model

## How Browsers Load Webpages

## Resources

- [Web standards](https://developer.mozilla.org/en-US/curriculum/core/web-standards/)