## Information Disclosure – Public Access to Frontend Configuration Files

During a security review of a public web application, public access to frontend project configuration files was identified. These files should not be exposed in a production environment.

---

### Vulnerability Details

- **Type:** Information Disclosure / Security Misconfiguration  
- **Risk Level:** Low  

---

### Exposed Resources (HTTP 200)

The following frontend-related configuration files were accessible publicly:

- `package.json`
- `package-lock.json`

---

### Security Impact

The exposed files allow an attacker to:

- Identify exact versions of frontend dependencies  
- Perform full technology fingerprinting of the application  
- Facilitate version-based vulnerability research (CVE targeting)

From the lock file, it was possible to determine specific third-party libraries and their versions, for example:

- `air-datepicker` (3.x)
- `flatpickr` (4.x)
- `litepicker` (2.x)

---

### What Was **Not** Found

No sensitive data was identified in the exposed resources:

- No API keys  
- No credentials  
- No environment variables  
- No `.git` repository access  

---

### Additional Verification

The following common sensitive paths were verified and found to be properly restricted or non-existent:

- `.env` → 403 Forbidden  
- `.git` → 404 Not Found  
- `node_modules`, `vendor`, `admin`, `api`, `_debugbar` → 404 Not Found  

---

### Impact Assessment

This issue does **not** allow direct compromise, code execution, or privilege escalation.

However, it increases the application’s attack surface and lowers the effort required for future exploitation if vulnerabilities are discovered in the disclosed components.

---

### Recommendations

- Restrict public access to development and configuration files in production  
- Review web server and deployment configuration for unintended file exposure  
- Ensure only compiled/static assets intended for public delivery are accessible  

---

### Notes

- Testing was non-intrusive and performed in good faith  
- No data was modified or exfiltrated  
- No automated exploitation or scanning was conducted  