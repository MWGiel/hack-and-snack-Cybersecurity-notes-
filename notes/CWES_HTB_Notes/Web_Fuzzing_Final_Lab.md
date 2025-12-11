## Final lab raport
- the first thing I did was fuzzing the ip from the task and I got the response <ip>:PORT /admin/panel.php
- I got the information "invalid parameter, please ensure accessID is set correctly" so I fuzzed the accessID parameter and got a "getacces" response
- When using curl to see the page result using the accessID parameter, I was advised to use the vhost fuzzing_fun.htb
- then I fuzzed fuzzing_fun.htb for potential subdomains and got the response "hidden", I added this subdomain to /etc/hosts and got a prompt to continue fuzzing in the /godeep/ folder
- I fuzzed podler /godeep and after a few levels of fuzzing I got a path leading to the flag page
## I managed to complete this lab with a little help, but I also managed to complete the entire module, I'm very satisfied
