# Red-Team / Offensive Lab — Summary
**Date:** 2025-10-05  
**Environment:** VirtualBox (Kali + Metasploitable2)

> **Legal / ethical disclaimer:**  
> All tests were performed in an isolated lab environment on machines I fully own or control.  
> Never use the described techniques against systems without explicit authorization — doing so is illegal and unethical.

---

## Environment setup
- **Host:** VirtualBox  
- **Attacker VM:** Kali Linux  
- **Target VM:** Metasploitable2  

---

## Tools and activities (overview)
- **w3brute** — performed authorized brute-force tests against web login forms.  
- **Ncrack** — successfully cracked a password on the Metasploitable2 VM.  
- **SQL / SQL Injection** — reminder: SQL is the standard language for database queries. SQL Injection involves injecting malicious input into a vulnerable query to gain unauthorized access.  
- **XSS (Cross-Site Scripting)** — injected a small payload into a web page that redirected users to YouTube; also demonstrated cookie and credential capture within the lab.  
- **slowhttptest** — simulated a DoS (Denial-of-Service) attack to overload the virtual machine with slow requests.  
- **Nmap** — scanned the target VM for open ports, services, and OS information.  
- **Payload injection** — delivered a test payload and obtained remote access to the lab machine, allowing access to local files (under controlled conditions).  
- **msfvenom** — used for generating payloads during exploit testing.  
- **Encrypted file brute-force** — cracked an encrypted local file via a wordlist attack.  
- **GitHub repo cloning** — cloned a test repository from GitHub to the "victim" VM to demonstrate network connectivity.  
- **Payload masking (obfuscation)** — experimented with concealing a payload within an archive and disguising its appearance (lab-only demonstration).

---

## Observations
- Weak passwords on the Metasploitable2 VM were successfully cracked — emphasizes the need for strong, unique passphrases.  
- XSS vulnerabilities allowed demonstration of credential and cookie interception in a sandboxed environment.  
- DoS simulation effectively overloaded the VM, confirming that slow request handling can exhaust resources.  
- Remote access payloads provided control over the VM, confirming proper connectivity and permissions inside the lab.

---

**Note:** All activities were conducted purely for educational and research purposes within a controlled lab environment.
