# Website Enumeration & Information Gathering

## High Level Goals

By the end of this lesons, you will be familiar with the following

- Drib
- Google Dorks
- Nikto
- Nmap
- Ping, Host, Nslookup
- Website Enumeration - Theory
- Whatweb

## Dirb

### Waht is DIRP

DIRB is a Web Content Scanner. It looks for existing (and/or hidden) Web Objects. It basically works by launching a dictionary based attack against a web server and analyzing the response.

DIRB comes with a set of preconfigured attack wordlists for easy usage but you can use your custom wordlists. Also DIRB sometimes can be used as a classic CGI scanner, but remember is a content scanner not a vulnerability scanner.

DIRB main purpose is to help in professional web application auditing. Specially in security related testing. It covers some holes not covered by classic web vulnerability scanners. DIRB looks for specific web objects that other generic CGI scanners can’t look for. It doesn’t search vulnerabilities nor does it look for web contents that can be vulnerables.

### How can we use it

- Opean your tirmenal and write `dirb`

![dirb-1](./img/Dirb-1.png)

* Note: make sure you are opeaning your OWASP server

- Write this command `dirb http://192.168.1.85` to generate a dictionary from our server

![dirb-2](./img/Dirb-2.png)

- Now we can go in our brawser and use any directory from the `dirb` such as lets use `http://192.168.1.58/phpmyadmin/`

![dirb-3](./img/Dirb-3.png)

 and we will see this 

![dirb-4](./img/Dirb-4.png)

## Google Dorks

### What is Google Dorks


A Google dork query, sometimes just referred to as a dork, is a search string that uses advanced search operators to find information that is not readily available on a website.

Google dorking, also known as Google hacking, can return information that is difficult to locate through simple search queries. That description includes information that is not intended for public viewing but that has not been adequately protected. 

As a passive attack method, Google dorking can return usernames and passwords, email lists, sensitive documents, personally identifiable financial information (PIFI) and website vulnerabilities. That information can be used for any number of illegal activities, including cyberterrorism, industrial espionage, identity theft and cyberstalking.

A search parameter is a limitation applied to a search. Here are a few examples of advanced search parameters:

- site: returns files located on a particular website or domain.

- filetype: followed (without a space) by a file extension returns files of the specified type, such as DOC, PDF, XLS and INI. Multiple file types can be searched for simultaneously by separating extensions with “|”.

- inurl: followed by a particular string returns results with that sequence of characters in the URL.

- intext: followed by the searcher’s chosen word or phrase returns files with the string anywhere in the text.

### How can we use it

1. Make sure you are opening OWASPBWA and Kali Linux

2. Go to firefox browser 

- Then go in google and write in search `site:tesla.com filetype:pdf` you will get all PDF result from tesla website

![google1](./img/Google-1.png)

- Now we must find some big things like eamils we can visit any website lets visit University website like [http://etf.bg.ac.rs](http://etf.bg.ac.rs) write in google search this command `"@etf.bg.ac.rs" -site:etf.bg.ac.rs`

![google2](./img/Google-2.png)

- Let us search for slash admin directory form Google search write `intitle:admin OR inurl:admin site:etf.bg.ac.rs`

![google3](./img/Google-3.png)

We got a links that we can opean it that awesome now opean any of these links

![google4](./img/Google-4.png)

We got a `Secure Connection Faild` press in `Enable TLS 1.0 and 1.1` and we will go in the admin page with multiple input and one admin email

![google5](./img/Google-5.png)

3. We can get a multiple commands to serach in google database go to [https://www.exploit-db.com/google-hacking-database](link)
