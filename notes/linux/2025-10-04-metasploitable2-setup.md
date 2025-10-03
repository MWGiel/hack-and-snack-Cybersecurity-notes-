# Metasploitable2 — quick lab note
**Date:** 2025-10-04  
**Environment:** VirtualBox VM (Metasploitable2) + Kali (attacker)

> **Legal / ethical note:** All testing performed in an isolated lab environment on machines I own/control. Do not run these tools against systems you do not have explicit permission to test.

## What I did
- Installed **Metasploitable2** as a virtual machine in **VirtualBox**.  
- From my **Kali** machine I accessed the VM's web interface via its IP address in a browser to see available services.  
- Scanned the Metasploitable2 VM with **Nmap** to enumerate open ports and services.  

## Example commands
- Basic service discovery on the target (replace `<IP>` with VM IP):
```bash
# quick service/version scan
nmap -sV <IP>

# full port scan + service detection + OS guess (no aggressive NSE by default)
nmap -p- -sV -O -T4 <IP>

    Check specifically for SSH (port 22):

nmap -p 22 -sV <IP>

SSH (short)

    SSH (Secure Shell) is a standard encrypted protocol for remote login and command execution.

    Default port: 22.

    It provides confidentiality and integrity for remote sessions.

Password brute-force (example: Hydra)

    I examined the SSH service and tested a password-guessing approach in the lab using Hydra (only on authorized lab VM).

    Example Hydra command (replace placeholders):

sudo hydra -l msfadmin -P /path/to/wordlist.txt -t 16 ssh://<IP>

    Explanation:

        -l msfadmin → single username to test (msfadmin is common on Metasploitable2).

        -P /path/to/wordlist.txt → path to the password wordlist.

        -t 16 → number of parallel tasks/threads.

        ssh://<IP> → target service and IP.
