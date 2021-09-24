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

## Burp Intercept

The Intercept tab is used to display and modify HTTP and WebSocket messages that pass between your browser and web servers. The ability to monitor, intercept and modify all messages is a core part of Burp's user-driven workflow. In Burp Proxy's options, you can configure interception rules to determine exactly what HTTP requests and responses are stalled for interception (for example, in-scope items, items with specific file extensions, requests with parameters, etc.). You can also configure which WebSocket messages  are intercepted.

### Controls

When an intercepted message is being displayed, details of the destination server are shown at the top of the panel. For HTTP requests, you can manually edit the target server to which the request will be sent, by clicking on the server caption or the button next to it.

- **Forward**  - When you have reviewed and (if required) edited the message, click "Forward" to send the message on to the server or browser.

- **Drop**  - Use this to abandon the message so that it is not forwarded.

- **Interception is on/off**  - This button is used to toggle all interception on and off. If the button is showing "Intercept is on", then messages will be intercepted or automatically forwarded according to the configured options for interception of HTTP and WebSocket messages. If the button is showing "Intercept is off" then all messages will be automatically forwarded.

- **Action**  - This shows a menu of available actions that can be performed on the currently displayed message. These are the same options that appear on the context menu of the intercepted message display.

- **Comment field**  - This lets you add a comment to interesting items, to easily identify them later. Comments added in the intercept panel will appear in the relevant item in the Proxy history. Further, if you add a comment to an HTTP request, the comment will appear again if the corresponding response is also intercepted.

- **Highlight**  - This lets you apply a colored highlight to interesting items. As with comments, highlights will appear in the Proxy history and on intercepted responses.

-----
## Burp Intruder

Burp Intruder is a tool for automating customized attacks against web applications. It is extremely powerful and configurable, and can be used to perform a huge range of tasks, from simple brute-force guessing of web directories through to active exploitation of complex blind SQL injection vulnerabilities.

### How Intruder works

Burp Intruder works by taking an HTTP request (called the "base request"), modifying the request in various systematic ways, issuing each modified version of the request, and analyzing the application's responses to identify interesting features.

For each attack, you must specify one or more sets of payloads and the positions in the base request where the payloads are to be placed. Numerous methods of generating payloads are available (including simple lists of strings, numbers, dates, brute force, a bit flipping, and many others). Payloads can be placed into payload positions using different algorithms, Various tools are available to help analyze the results and identify interesting items for further investigation.

### Saving an attack

Intruder attacks are not saved to a project file by default. If you are using a project file, you can save attacks by doing any of the following:

-   From the Intruder attack window, click on the "Save" tab. Here, you can save to a project file, or save the results table, server responses or configuration of the attack.

-   From the Intruder attack window, click on the "Options" tab. Under "Save Options", select the checkbox to save the attack to a project file. This can be done before or during an attack.

-   From the Dashboard, scroll to the attack in the task list and click on the save icon. This can be done before or during an attack.

-   In Intruder, select the "Options" tab. Under "Save Options", select the checkbox to save the attack to a project file.
-   When an attack has finished, Burp will give you the option of saving the attack to a project file if you close the attack window.

Once an attack is saved to a project file, the state of the attack is constantly saved from that point on. Saved attacks can be closed, and re-opened later from the task list of the Dashboard.

Intruder does not save attacks to project files by default, as saving many attacks can result in large project files. We recommend that you only save attacks to project files once you have found something interesting. Note that this opt-in saving is unique to Intruder: other tasks (such as scans) have a smaller effect on project file size and are saved to project files by default.

**Note:**  Intruder attacks can no longer be saved to state files. Legacy state files can still be loaded, however. To load a legacy state file, Select the top level Intruder tab and click on "Open saved attack".

**Note:**  Missing information in a row on the attack results page may mean that you shut down Burp Suite while an attack was in progress, and one of the requests was not sent.
