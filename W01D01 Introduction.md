
# Introduction Penetration-Testing

  

## High Level Goals

By the end of this Stage, you will be familiar with the following:

- Virtual Lap
- Enumeration & Information
- Burp Suite
- HTML Injection
- Command Injection + Execution
- Broken Authentication
- Brute force Attacks
- Access Control
- XSS
- SQL Injection
- XPath, XXE
- Logging + Monitoring
- Bug Hunting
  
## Virtual Lap

**What is Virtual Lap**

A virtual Lab is a simulated lab environment typically implemented as a software program which allows the users to perform their experiments.

 **What we will learn**

We will learn how to download and use this following:

1. Virtual Box.
2. Kali Linux.
3. OWASPBWA.
4. TryHackMe Platform.

## Enumeration & Information

 **What is Enumeration & Information**

Enumeration is defined as the process of extracting user names, machine names, network resources, shares and services from a system.

In this phase, the attacker creates an active connection to the system and performs directed queries to gain more information about the target. The gathered information is used to identify the vulnerabilities or weak points in system security and tries to exploit in the System gaining phase.

 **What is the website we will use to Enumeration & Information**

- Google Dorking.
- WhatWeb.
- Dirb.
- Nmap.
- Nikto.

## Burpsuite

**What is Burpsuite used for**

Burp or Burp Suite is a set of tools used for penetration testing of web applications. ... BurpSuite aims to be an all-in-one set of tools, and its capabilities can be enhanced by installing add-ons that are called BApps. It is the most popular tool among professional web app security researchers and bug bounty hunters.

## HTML Injection

 **What is HTML Injection**

HTML injection is a type of injection vulnerability that occurs when a user is able to control an input point and is able to inject arbitrary HTML code into a vulnerable web page. This vulnerability can have many consequences, like disclosure of a user’s session cookies that could be used to impersonate the victim, or, more generally, it can allow the attacker to modify the page content seen by the victims.

## Command Injection

 **What is Command Injection**

Command injection is an attack in which the goal is execution of arbitrary commands on the host operating system via a vulnerable application. we will talk about it later.

## Broken Authentication

 **What is Broken Authentication**

Authentication is “broken” when attackers are able to compromise passwords, keys or session tokens, user account information, and other details to assume user identities. Due to poor design and implementation of identity and access controls, the prevalence of broken authentication is widespread.

**Brute Force Attack**

A brute force attack uses trial-and-error to guess login info, encryption keys, or find a hidden web page. Hackers work through all possible combinations hoping to guess correctly.

These attacks are done by ‘brute force’ meaning they use excessive forceful attempts to try and ‘force’ their way into your private account(s).

This is an old attack method, but it's still effective and popular with hackers. Because depending on the length and complexity of the password, cracking it can take anywhere from a few seconds to many years.

## Broken Access Control

 **What is Broken Access Control**

Broken access control vulnerabilities exist when a user can in fact access some resource or perform some action that they are not supposed to be able to access.

## Cross Site Scripting - XSS

 **What is Cross Site Scripting - XSS**

Cross-site scripting (XSS) is a type of security vulnerability typically found in web applications.
XSS attacks enable attackers to inject client-side scripts into web pages viewed by other users.
A cross-site scripting vulnerability may be used by attackers to bypass access controls such as the same-origin policy.

Cross-site scripting carried out on websites accounted for roughly 84% of all security vulnerabilities documented by Symantec up until 2007. XSS effects vary in range from petty nuisance to significant security risk, depending on the sensitivity of the data handled by the vulnerable site and the nature of any security mitigation implemented by the site's owner network.

## SQL Injection

**What is SQL Injection**

A SQL is a type of attack by which cybercriminals exploit software vulnerabilities in web applications for the purpose of stealing, deleting, or modifying data, or gaining administrative control over the systems running the affected applications.

## XXE

 **What is XXE**

XML external entity injection (also known as XXE) is a web security vulnerability that allows an attacker to interfere with an application's processing of XML data. It often allows an attacker to view files on the application server file system, and to interact with any back-end or external systems that the application itself can access.

In some situations, an attacker can escalate an XXE attack to compromise the underlying server or other back-end infrastructure, by leveraging the XXE vulnerability to perform server-side request forgery (SSRF) attacks.

## Logging + Monitoring

**What is Logging + Monitoring**

Logging and monitoring are both valuable components to maintaining optimal application performance. Using a combination of logging tools and real-time monitoring systems helps improve observability and reduces the time spent sifting through log files to determine the root cause of performance problems.

**What’s the Difference? Logging vs Monitoring**

Logging is used as both a verb and a noun, referring either to the practice of logging errors and changes or to the application logs that are collected. The purpose of logging is to create an ongoing record of application events. Log files can be used to review any event within a system, including failures and state transformations. Consequently, log messages can provide valuable information to help pinpoint the cause of performance problems. Log data can help DevOps teams troubleshoot issues by identifying which changes resulted in error reporting, but is only as valuable as the information it contains.

Monitoring is an umbrella term that can include many facets of system evaluation, but in this context, we're referring to application performance monitoring (APM). APM is the process of instrumenting an application to collect, aggregate and analyze metrics to better evaluate the use of the system by gauging availability, response time, memory usage, bandwidth, and CPU time consumption.

## Bug Hunting

**What is Bug Hunting**

A bug bounty program allows hackers to receive compensation for reporting bugs, also known as vulnerabilities and possible exploits, in organizations’ hardware, firmware, and software. Most commonly, though, they allow organizations to use external resources to find and disclose vulnerabilities that exist within their sensitive applications.

The goal of this initiative is to prevent black-hat or grey-hat hackers from exploiting an organization for bugs found in applications that contain confidential information to the company or its customers. Over the years, bug bounty programs have grown exponentially to include large companies and government organizations.