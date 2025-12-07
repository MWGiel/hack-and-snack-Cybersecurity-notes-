## Skills Assessment Final Lab
- Q1  What is the IANA ID of the registrar of the inlanefreight.com domain?
> I did the enumeration using whois and found the information in the information
---
- Q2 What http server software is powering the inlanefreight.htb site on the target system? Respond with the name of the software, not the version, e.g., Apache.
> Using nmap, I enumerated the target and obtained information about the services that this system hosts
---
- Q3  What is the API key in the hidden admin directory that you have discovered on the target system?
> first I fuzzed the domains and found web1337 and then .dev, when I go to this page in the frontend there is a key
---
- Q4 After crawling the inlanefreight.htb domain on the target system, what is the email address you have found? Respond with the full email, e.g., mail@inlanefreight.htb.
- Q5 What is the API key the inlanefreight.htb developers will be changing too? 
> I used reconspider and scrapy to scan the page and found the answer to question 4 and 5 in the results
