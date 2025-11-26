# Lab Summary: Capturing Metasploit HTTP Request

## Goal
Capture and analyze the HTTP request sent by the Metasploit module  
`auxiliary/scanner/http/coldfusion_locale_traversal` and identify the directory used in the path.

---

## Steps

### 1. Load the Metasploit module
use auxiliary/scanner/http/coldfusion_locale_traversal

### 2. Configure proxy to route traffic through Burp Suite
set Proxies http:127.0.0.1:8080

### 3. Run the module
run

### 4. Capture the request in Burp Suite  
Burp shows a GET request to:

/CFIDE/administrator/index.cfm

---

## Result
The directory used in the path `/XXXXX/administrator/..` is:

### **CFIDE**

---

## Conclusion
The module simply sends a normal HTTP request to the standard ColdFusion Administrator path.  
By intercepting the traffic in Burp Suite, you can clearly see what Metasploit is doing behind the scenes.
