# Nmap — Quick Glossary

## Terms
- **Nmap** — network scanning tool (host discovery, port scan, service/OS detection).  
- **Host** — target device (IP or hostname).  
- **Port** — network entry point for a service.  
- **Port states**:  
  - **open** — service available, port responds  
  - **closed** — port closed, host responds  
  - **filtered** — blocked or unknown by firewall  

## Common Scans
- **TCP SYN scan (-sS)** — stealthy "half-open" scan.  
- **TCP Connect scan (-sT)** — full TCP connection scan.  
- **UDP scan (-sU)** — checks UDP ports.  
- **Ping scan (-sn)** — detects live hosts only.  
- **Version detection (-sV)** — finds service versions.  
- **OS detection (-O)** — guesses operating system.  
- **Aggressive scan (-A)** — combines version, OS, traceroute, scripts.  

## Useful Flags
- `-p` — specify ports (`-p 22,80` or `-p-` for all)  
- `-Pn` — skip host discovery  
- `-oN/-oX/-oG` — save results in text/XML/grepable  
- `--script <script>` — run NSE scripts (e.g., `vuln`)  
- `--traceroute` — show route to target  

## Quick Examples
```bash
# Version scan on a host
nmap -sV 192.168.1.1

# Scan all TCP ports
nmap -p- -T4 192.168.1.0/24

# Ping scan for live hosts
nmap -sn 192.168.1.0/24

# Scan with vulnerability scripts
nmap -sV --script vuln 10.10.10.10

ONLY SCAN NETWORKS YOU OWN OR YOU HAVE PERMISSION TO TEST





