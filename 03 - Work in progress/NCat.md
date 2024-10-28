# Ncat
Tags: [[Tools]], [[Kali]]

The Ncat tool is used to capture an incomming TCP or UDP request.  An example capture would be:

```
┌──(kali㉿kali)-[~]
└─$ nc -l -p 443 -v
listening on [any] 443 ...
192.168.2.148: inverse host lookup failed: Unknown host
connect to [192.168.2.166] from (UNKNOWN) [192.168.2.148] 54601
GET / HTTP/1.1
Host: 192.168.2.166:443
Connection: keep-alive
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/130.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8
Sec-GPC: 1
Accept-Language: en-US,en
Accept-Encoding: gzip, deflate
Cookie: csrftoken=6oWojjbzdqOGpVbxJWAJHo8nMFJU1PrX; sessionid=prwbh9y0n3ltom1rxu1wzlxutiany53q
```

[Ncat](https://nmap.org/ncat/)