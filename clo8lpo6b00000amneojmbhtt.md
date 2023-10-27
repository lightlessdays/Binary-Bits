---
title: "Why the extra 's' after http?"
datePublished: Fri Oct 27 2023 12:40:21 GMT+0000 (Coordinated Universal Time)
cuid: clo8lpo6b00000amneojmbhtt
slug: why-the-extra-s-after-http
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698410393807/fe502b78-4f54-4f59-891d-5e322880fac8.png
tags: internet

---

If you are a frequent user of the internet, you must have seen two kinds of websites: one that starts with `https://...` and the other that starts with `http://`. So, what is the difference between these two kinds of websites?

Before we get into the differences, let’s first talk about website security. Anytime you visit a website, you send information to that site’s server. This information can include things like your IP address, what browser you’re using, and what pages on the site you’re visiting. This information is sent in plain text, meaning anyone monitoring your traffic can see it.

If you’re using a public Wi-Fi network, this information can be intercepted by someone else on the network. This is why using a secure connection is essential when sending sensitive information, like credit card numbers or passwords.

Every link you click that starts with HTTP uses a basic protocol known as Hypertext Transfer Protocol (HTTP or “protocol”). HTTP is a network protocol standard that defines how messages are formatted and transmitted and what actions web servers and browsers should take in response to various commands.

Whenever you enter a URL into your web browser, your computer sends a request to the server that hosts the website you’re trying to visit. That server sends back a response, usually the website’s HTML code. This communication between your computer and the server happens over port 80 for unsecured connections. An unsecured connection means that there is no SSL Certificate.

HTTPS is an extension of the Hypertext Transfer Protocol. The S is HTTPS stands for secure. When a website is encrypted with TLS (or SSL), it uses Hypertext Transfer Protocol Secure (HTTPS). 

Basically, it’s HTTP with encryption. It is used to secure communication over a computer network and is widely used on the Internet. HTTPS encrypts and decrypts user page requests and the pages returned by the web server.

This protects against man-in-the-middle attacks and the confidentiality of data sent between the browser and the website. HTTPS connections use port 443 by default.

HTTPS is more secure than HTTP because it uses encryption to protect information as it is being sent between clients and servers. When an organization enables HTTPS, any information you transmit, like passwords or credit card numbers, will be difficult for anyone to intercept.

HTTP does not use encryption, which means that any information you send can be intercepted by someone else on the network. This is why using a secure connection is essential when sending sensitive information.

Another difference between the protocols is that HTTPS uses port 443, while HTML uses port 80. Port 443 is the standard port for secured Hypertext Transfer Protocol (HTTPS). Port 80 is the default port for unsecured Hypertext Transfer Protocol.

To enable HTTPS on a website, it must have a valid SSL (secure sockets layer) certificate. This certificate is used to encrypt information as it is being sent between your computer and the server. An SSL certificate contains a public key and a private key. The public key encrypts information, while the private key decrypts it.

SSL Certificates are issued by Certificate Authorities (CAs). A CA is an organization that verifies the identity of a website and then gives a certificate to that site. When you visit a website, your browser checks to see if the site’s SSL Certificate is valid. You will see a green padlock in the address bar if it is. If it is not, you will see a warning message.

Web encryption is the process of encrypting information as it is being sent between a web server and a web browser. SSL/TLS Certificates use this process to protect sensitive information such as credit card numbers, passwords, and personal information.

SSL/TLS Certificates use a process called secure encryption to protect information as it is being sent over the Internet. Secure encryption is a form of data security that uses mathematical algorithms to encrypt and decrypt data.

Secure encryption protects credit card numbers, passwords, and personal information. When this information is encrypted, it is turned into a code that the intended recipient can only decrypt. This makes it difficult for anyone to intercept and read the information.