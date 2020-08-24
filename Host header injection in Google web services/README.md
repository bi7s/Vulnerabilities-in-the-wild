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
  3. Replace path to "/maps/vt/icon/name=../../";
  4. Replace Host header to any name;
  5. Send modified request.
  6. You will redirect to "new" host. 

Screenshots :
- https://www.google.com


- https://account.google.com


- https://mail.google.com


- https://drive.google.com


- https://youtube.com
