# Introduction To Burpsuite

## High Level Goals

By the end of this lesson, you will be familiar with the following:

- Burp Suite
- Burp Suite Intercept
- Burp Suite Intruder
- Burp Suite Repeater

## what is Burp Suite

**Burp Suite** is an integrated platform for performing security testing of web applications. Its various tools work seamlessly together to support the entire testing process, from initial mapping and analysis of an application’s attack surface, through to finding and exploiting security vulnerabilities.

In its simplest form, **Burp Suite** can be classified as an Interception Proxy. While browsing their target application, a penetration tester can configure their internet browser to route traffic through the **Burp Suite** proxy server.

## Burepsuite Configuration
To configuration your Burepsuite follow these steps:

1. let's start to configure **proxy** for  our Firefox 
- First open terminal and start our burepsuite, we can do that by typing this command

		burpsuite

**If** you get these issue 

![burp1](/img/burp1.png)

click in `OK`, then do these steps

![burp2](/img/burp2.png)

![burp3](/img/burp3.png)

![burp4](/img/burp4.png)

![burp5](/img/burp5.png)

![burp6](/img/burp6.png)

![burp7](/img/burp7.png)

- know start our Firefox 

![burp8](/img/burp8.png)

![burp9](/img/burp9.png)

make sure to select `Manual proxy configuration` and write these sitting
in **HTTP Proxy:** `127.0.0.1` **PORT:** `8080` and click in **Also use this proxy for FTP and HTTPS**

![burp10](/img/burp10.png)

Now when we visit any website called http we can get information in our burp but when we visit websites called https like facebook we will get issue secure, because the burp certificate it's not in our browser we need to add it  by following this steps
A. Go to `http://burp`

![burp11](/img/burp11.png)

now download the certificate and go again in Firefox setting go to **Privacy & Security** scroll down tell we get option called **Certificates** click in `view certificate` and import the file we downloaded it and select it `cacert.der` then you will see the popup  

![burp12](/img/burp12.png)

Now if you check again, you can visit the websites with https, you can visit Facebook

---

## Burp Suite Intercept

The Intercept tab is used to display and modify HTTP and WebSocket messages that pass between your browser and web servers. The ability to monitor, intercept and modify all messages is a core part of Burp's user-driven workflow. In Burp Proxy's options, you can configure interception rules to determine exactly what HTTP requests and responses are stalled for interception (for example, in-scope items, items with specific file extensions, requests with parameters, etc.). You can also configure which WebSocket messages  are intercepted.

### Controls

When an intercepted message is being displayed, details of the destination server are shown at the top of the panel. For HTTP requests, you can manually edit the target server to which the request will be sent, by clicking on the server caption or the button next to it.

