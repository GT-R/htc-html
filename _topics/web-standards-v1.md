---
title:  Web Standards
name:   web-standards-v1
---

We're not going to spend a lot of time on background, but there are a few things that you should be aware of as you begin your journey into web development.  Highlights can be found here.  You will find more details in Chapter 1 of your textbook.

#### What is the W3C?
The [World Wide Web Consortium (W3C)](http://www.w3c.org) is a group that prototypes technology and recommends standards for the Web. They address topics such as web architecture, specifications for HTML and CSS, and guidelines for design and accessibility.  It is important to keep in mind however that these are recommendations and may or may not be followed by everyone in the same way.  

The biggest area where that this affects us is in regards to HTML and CSS support in web browsers.  The HTML5 specification has been available as a public draft since 2008, and was made an official recommendation in October of 2014.  However support for it in web browsers varies widely. ([Can I Use? HTML5](http://caniuse.com/#cats=HTML5)) It is easy to think this is the standard, so I should use it, but with web development we want to aim for the standard while still providing a good experience for our customers who may have old browsers.

#### Accessibility
As we learn to build web sites, we will call attention to accessiblity guidelines and best practices.  In 1996 the Department of Justice ruled that the ADA (Americans with Disabilities Act) also applies to the web, and this was followed up in 1998 with an amendment to Section 508 of the Federal Rehabilitation Act which requires the government to give those with disabilities access to electronic information that is comparable to the access available to others. Not surprisingly, the W3C is also very involved with accessibility on the web. Their Web Accessibility Initiative (WAI) provides guidelines for both web content developers and web browser developers to facilitate access to web resources for those with disabilities.  

#### Protocols
There are several key protocols (or communication rules) that support how the internet works.  You should be aware of these and know how they are relevant to the internet and web.

- TCP/IP (Transmissing Control Protocol / Internet Protocol) - the official communication protocol of the internet
- HTTP (Hypertext Transfer Protocol) - used by web browsers, supports requesting and sending files over the web
- FTP (File Transfer Protocol) - moving files from one place to another; often used for downloads
- SMTP (Simple Mail transfer Protocol) - sending email
- POP (Post Office Protocol) and IMAP (Internet Mail Access Protocol) - receiving email

#### Web Addresses
One way to get to a web site is to enter its URL (Uniform Resource Locator) into the address bar on your web browser.  A URL is made up of several parts.

- The protocol - generally this will be HTTP or HTTPS
- The domain name or IP
- The path to the requested file on that server
- The file name requested

<img src="{{ "/assets/topics/web-standards-url.png" | prepend:site.baseurl }}" 
    alt="Image illustrating the parts of a URL for this site
         (http://htc-ccis1301.github.io/htc-html/sessions/session1-class-v1.html.  
         The protocol is http; the domain name is htc-ccis1301.github.io;
         the path is /htc-html/sessions/; the file requested is session1-class-v1.html">

As we build links to tie our web pages to other pages on our own site and other sites, it is important to understand what a URL is referring to.
