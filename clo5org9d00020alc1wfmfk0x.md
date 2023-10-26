---
title: "What are Proxy Servers?"
datePublished: Wed Oct 25 2023 11:42:24 GMT+0000 (Coordinated Universal Time)
cuid: clo5org9d00020alc1wfmfk0x
slug: what-are-proxy-servers
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698234105534/cb9cde6c-631e-49a5-9aa9-01131678c2ec.png
tags: internet-technologies

---

A proxy server acts as a gateway between you and the internet. It’s an intermediary server separating end users from the websites they browse. Proxy servers provide varying levels of functionality, security, and privacy depending on your use case, needs, or company policy.

If you’re using a proxy server, internet traffic flows through the proxy server on its way to the address you requested. The request then comes back through that same proxy server (there are exceptions to this rule), and then the proxy server forwards the data received from the website to you.

If that’s all it does, why bother with a proxy server? Why not just go straight from to the website and back?

Modern proxy servers do much more than forward web requests, all in the name of data security and network performance. Proxy servers act as a firewall and web filter, provide shared network connections, and cache data to speed up common requests. A good proxy server keeps users and the internal network protected from the bad stuff that lives out on the wild internet. Lastly, proxy servers can provide a high level of privacy.

### What does a Proxy Server Do?

Every computer on the internet needs to have a unique Internet Protocol (IP) Address. Think of this IP address as your computer’s street address. Just as the post office knows to deliver your mail to your street address, the internet knows how to send the correct data to the correct computer by the IP address.

A proxy server is basically a computer on the internet with its own IP address that your computer knows. When you send a web request, your request goes to the proxy server first. The proxy server then makes your web request on your behalf, collects the response from the web server, and forwards you the web page data so you can see the page in your browser.

When the proxy server forwards your web requests, it can make changes to the data you send and still get you the information that you expect to see. A proxy server can change your IP address, so the web server doesn’t know exactly where you are in the world. It can encrypt your data, so your data is unreadable in transit. And lastly, a proxy server can block access to certain web pages, based on IP address.

### Why use Proxy Servers?

There are several reasons organizations and individuals use a proxy server.

* **To control internet usage of employees and children:** Organizations and parents set up proxy servers to control and monitor how their employees or kids use the internet. Most organizations don’t want you looking at specific websites on company time, and they can configure the proxy server to deny access to specific sites, instead of redirecting you with a nice note asking you to refrain from looking at said sites on the company network. They can also monitor and log all web requests, so even though they might not block the site, they know how much time you spend cyberloafing.
    

* **Bandwidth savings and improved speeds:** Organizations can also get better overall network performance with a good proxy server. Proxy servers can cache (save a copy of the website locally) popular websites – so when you ask for binarybits.hashnode.dev, the proxy server will check to see if it has the most recent copy of the site, and then send you the saved copy. What this means is that when hundreds of people hit binarybits.hashnode.dev at the same time from the same proxy server, the proxy server only sends one request to binarybits.hashnode.dev. This saves bandwidth for the company and improves the network performance.
    
* **Privacy benefits:** Individuals and organizations alike use proxy servers to browse the internet more privately. Some proxy servers will change the IP address and other identifying information the web request contains. This means the destination server doesn’t know who actually made the original request, which helps keeps your personal information and browsing habits more private.
    

* **Improved security:** Proxy servers provide security benefits on top of the privacy benefits. You can configure your proxy server to encrypt your web requests to keep prying eyes from reading your transactions. You can also prevent known malware sites from any access through the proxy server. Additionally, organizations can couple their proxy server with a Virtual Private Network (VPN), so remote users always access the internet through the company proxy. A VPN is a direct connection to the company network that companies provide to external or remote users. By using a VPN, the company can control and verify that their users have access to the resources (email, internal data) they need, while also providing a secure connection for the user to protect the company data.
    

* **Get access to blocked resources:** Proxy servers allow users to circumvent content restrictions imposed by companies or governments. Is the local sportsball team’s game blacked out online? Log into a proxy server on the other side of the country and watch from there. The proxy server makes it look like you are in California, but you actually live in North Carolina. Several governments around the world closely monitor and restrict access to the internet, and proxy servers offer their citizens access to an uncensored internet.
    

Now let us look at risks associated with Proxy Servers.

### Why not use Proxy Servers?

You do need to be cautious when you choose a proxy server: a few common risks can negate any of the potential benefits:

* **Free proxy server risks** 
    
    * You know the old saying “You get what you pay for?” Well, using one of the many free proxy server services can be quite risky, even the services using ad-based revenue models.
        
    * Free usually means they aren’t investing heavily in backend hardware or encryption. You’ll likely see performance issues and potential data security issues. If you ever find a completely “free” proxy server, tread very carefully. Some of those are just looking to steal your credit card numbers.
        

* **Browsing history log**
    
    * The proxy server has your original IP address and web request information possibly unencrypted saved locally. Make sure to check if your proxy server logs and saves that data – and what kind of retention or law enforcement cooperation policies they follow.
        
    * If you expect to use a proxy server for privacy, but the vendor is just logging and selling your data you might not be receiving the expected value for the service.
        

* **No encryption**
    
    * If you use a proxy server without encryption, you might as well not use a proxy server. No encryption means you are sending your requests as plain text. Anyone who is listening will be able to pull usernames passwords and account information really easily. Make sure whatever proxy server you use provides full encryption capability.