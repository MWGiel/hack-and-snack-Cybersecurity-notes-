## Today i started a Web Penetration Tester Path on HTB and learned about HTTP and HTPPS
If we type http:// instead of https:// to visit a website that enforces HTTPS, the browser attempts to resolve the domain and redirects the user to the webserver hosting the target website.
A request is sent to port 80 first, which is the unencrypted HTTP protocol.
The server detects this and redirects the client to secure HTTPS port 443 instead. This is done via the 301 Moved Permanently response code, which we will discuss in an upcoming section.

Next, the client (web browser) sends a "client hello" packet, giving information about itself. After this, the server replies with "server hello", followed by a key exchange to exchange SSL certificates. 
The client verifies the key/certificate and sends one of its own. After this, an encrypted handshake is initiated to confirm whether the encryption and transfer are working correctly.
> Mwegiel@htb[/htb]$ curl https://inlanefreight.com curl: (60) SSL certificate problem: Invalid certificate chain More details here: https://curl.haxx.se/docs/sslcerts.html

## Completed first lab but it was very easy, i have must must curl <ip> -v and got an answer :)
