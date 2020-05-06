---
layout: post
title:  "How Webpage loads!"
author: "Adi Bhamidipati"
---

# THIS IS A WIP commit

## What happens after you enter url into browser?

Browser will check if you entered just text without any protocol it goes to search engine and get the search results.
If you have provided a valid URL, the next steps would be figuring out the IP addess of the corresponding resource.

If it entered text have HTTP or HTTPS in the url, the browser will look for dns in the below order till it finds it
1) Browser DNS cache
2) Operating system host file  for DNS entry.
3) DNS query request to ISP and get the IP address.

After the host name is resolved, then it will reach out router cache to get host name resolved. 

If we have port number associated, browser will send a request to the corresponding server amd resource for html
Then the browser will render the html on the screen

Assuming we have IP address, browser will initiate the tcp request to the resource. Browser will now send the http request to 
the resource. If the Response code is 200 it is OK, which means it returned the resource requested by the browser

Typically browser display html content and do get requests to get additional assets and will cache the static data to avoid multiple requests and calls

# Related Technical Jargon

* What is URL?
> Uniform Resource Locater

* What is DNS?
> Domain Name systemii

* What is TCP?
> Transmission control Protocol
> The communication is intitiated with below steps using tcp protocol:
> SYNC -> ACK/SYNC
> SYNC

* What is HTTP?
> Hyper Text Transport Protocol

* What is DCHP?
> Dynamic Host Configuration Protocol, this is used to dynamically configure devices on ip network so the devies have access to network services like DNS, NTP, and any communication protocol based on UDP or TCP.

* What is Ping?
> Utility to verify quick access to resource and return the elapsed time to reach the resouce

* What is traceroute?
> Utility to track the network path from source to desitnation resource and record time for each step
