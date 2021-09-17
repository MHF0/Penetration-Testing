
# **Website Enumeration & Information Gathering**

## 5. Ping, Host, Nslookup, Whois and Whatweb

**In this lesson, we want to know how can we got an IP address from any website as we know the websites we visiting it, it's showing us a domain name like `www.example.com` we want to know what is the IP address that this website using it.**

### Ping
The ping command is useful for determining the status of the network and various foreign hosts, tracking and isolating hardware and software problems, and testing, measuring, and managing networks. We can used it by typing `ping (our IP target)`

    ping 192.168.1.85

As we see the output

	PING 192.168.1.85 (192.168.1.85) 56(84) bytes of data.
	64 bytes from 192.168.1.85: icmp_seq=1 ttl=64 time=1.00 ms
	64 bytes from 192.168.1.85: icmp_seq=2 ttl=64 time=0.438 ms
	64 bytes from 192.168.1.85: icmp_seq=3 ttl=64 time=0.478 ms

It is mean the server with the IP `192.168.1.85` is running now, we can scan as domain name not only IP address.  Let's scan `google.com`

	$ ping google.com                                                    130x
	PING google.com(mrs09s09-in-x0e.1e100.net (2a00:1450:4006:807::200e)) 56 data bytes
	64 bytes from mrs08s05-in-x0e.1e100.net (2a00:1450:4006:807::200e): icmp_seq=1 ttl=115 time=133 ms
	64 bytes from mrs08s05-in-x0e.1e100.net (2a00:1450:4006:807::200e): icmp_seq=2 ttl=115 time=55.7 ms
	64 bytes from mrs08s05-in-x0e.1e100.net (2a00:1450:4006:807::200e): icmp_seq=3 ttl=115 time=55.3 ms
	64 bytes from mrs08s05-in-x0e.1e100.net (2a00:1450:4006:807::200e): icmp_seq=4 ttl=115 time=55.5 ms
	64 bytes from mrs08s05-in-x0e.1e100.net (2a00:1450:4006:807::200e): icmp_seq=5 ttl=115 time=53.1 ms
	64 bytes from mrs08s05-in-x0e.1e100.net (2a00:1450:4006:807::200e): icmp_seq=6 ttl=115 time=55.4 ms
	64 bytes from mrs08s05-in-x0e.1e100.net (2a00:1450:4006:807::200e): icmp_seq=7 ttl=115 time=54.9 ms

We can know what is the IP address that google using it, it is `mrs09s09-in-x0e.1e100.net` but the `ping` commands it doesn't necessary always telling the troth, some website might block  thing probs, and we might know to be able to ping them  however they could still be online, so don't worry if the ping does not work perfectly.

### Host
Host command is used for DNS (Domain Name System) lookup operations. In simple words, this command is used to find the IP address of a particular domain name or if you want to find out the domain name of a particular IP address, the host command becomes handy. You can also find more specific details of a domain by specifying the corresponding option along with the domain name.

Syntax:

	host [-aCdlriTWV] [-c class] [-N ndots] [-t type] [-W time]
	     [-R number] [-m flag] hostname [server]
	     
Host IP_Address: This will display the domain details of the specified IP Address, let's scan  `tesla.com` by using this command `host tesla.com`

	$ host tesla.com   
	tesla.com has address 199.66.11.62
	tesla.com mail is handled by 10 tesla-com.mail.protection.outlook.com.

### Nslookup
The **nslookup** command queries internet domain name servers in two modes. Interactive mode allows you to query name servers for information about various hosts and domains, or to print a list of the hosts in a domain. In noninteractive mode, the names and requested information are printed for a specified host or domain.

It's like host, we can run this command `nslookup tesla.com`

	$ nslookup tesla.com
	Server:         192.168.1.1
	Address:        192.168.1.1#53

	Non-authoritative answer:
	Name:   tesla.com
	Address: 199.66.11.62

### Whois

Whois searches for an object in a WHOIS database. WHOIS is a query  and response protocol that is widely used for querying databases that store the registered users of an Internet resource, such as a domain name or an P  address block, but is also used for a wider range of other information. Let's scan `tesla.com`

	whois tesla.com

then we're getting some phones numbers, getting name servers and some postal code, we get information about  admins organization, city, phone number and some others information.

### Whatweb
WhatWeb identifies websites. Its goal is to answer the question, “What is that Website?”. WhatWeb recognizes web technologies including content management systems (CMS), blogging platforms, statistic/analytics packages, JavaScript libraries, web servers, and embedded devices. WhatWeb has over 1700 plugins, each to recognize something different. WhatWeb also identifies version numbers, email addresses, account IDs, web framework modules, SQL errors, and more, let's scan our target OWASP

	$ whatweb 192.168.1.85
	http://192.168.1.85 [200 OK] Apache[2.2.14][mod_mono/2.4.3,mod_perl/2.0.4,mod_python/3.3.1,mod_ssl/2.2.14,proxy_html/3.0.1], Country[RESERVED][ZZ]
	Email[admin@metacorp.com,admin@owaspbwa.org,bob@ateliergraphique.com,cycloneuser-3@cyclonetransfers.com,jack@metacorp.com,test@thebodgeitstore.com],
	HTML5, HTTPServer[Ubuntu Linux][Apache/2.2.14 (Ubuntu) mod_mono/2.4.3 		PHP/5.3.2-1ubuntu4.30 with Suhosin-Patch proxy_html/3.0.1 mod_python/3.3.1 Python/2.6.5 mod_ssl/2.2.14 OpenSSL/0.9.8k Phusion_Passenger/4.0.38 mod_perl/2.0.4 Perl/v5.10.1], IP[192.168.1.85], JQuery[1.3.2],
	OpenSSL[0.9.8k], PHP[5.3.2-1ubuntu4.30][Suhosin-Patch], Passenger[4.0.38], Perl[5.10.1], Python[2.6.5], Script[text/javascript],
	Title[owaspbwa OWASP Broken Web Applications]
