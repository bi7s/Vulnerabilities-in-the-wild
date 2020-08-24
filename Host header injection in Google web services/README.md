### Host header injection in Google web services

## List of vulnerable services :

- https://www.google.com
- https://account.google.com
- https://mail.google.com
- https://drive.google.com
- https://youtube.com

and other

Steps to reproduce:
  1. Go to any site from list (google.com, account.google.com, mail.google.com, youtube.com drive.google.com);
  2. Intercept GET request using burp suite or other tools;
  3. Replace path to "/maps/vt/icon/name=../../" **(possibly use shoter path "/.")**;
  4. Replace Host header to any name;
  5. Send modified request.
  6. You will redirect to "new" host. 

Screenshots :


## https://www.google.com


![](https://github.com/bi7s/Vulnerabilities-in-the-wild/blob/master/Host%20header%20injection%20in%20Google%20web%20services/HHI%20(www.google.com)%20inj.png)

## https://account.google.com


![](https://github.com/bi7s/Vulnerabilities-in-the-wild/blob/master/Host%20header%20injection%20in%20Google%20web%20services/HHI%20(account.google.com)%20inj%20.png)

## https://mail.google.com


![](https://github.com/bi7s/Vulnerabilities-in-the-wild/blob/master/Host%20header%20injection%20in%20Google%20web%20services/HHI%20(mail.google.com)%20inj%20.png)

## https://drive.google.com

![](https://github.com/bi7s/Vulnerabilities-in-the-wild/blob/master/Host%20header%20injection%20in%20Google%20web%20services/HHI%20(drive.google.com)%20inj.png)

## https://www.youtube.com


![](https://github.com/bi7s/Vulnerabilities-in-the-wild/blob/master/Host%20header%20injection%20in%20Google%20web%20services/HHI%20(www.youtube.com)%20inj.png)
