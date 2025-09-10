# SQL injection UNION attack, determining the number of columns returned by the query - Portswigger

Resources : https://portswigger.net/web-security/sql-injection/union-attacks/lab-determine-number-of-columns

The objective of the challenge is to determining the number of columns returned by the query.

1. First step you always can use your burpsuite and select a random catagory and turn your intercept on. 
2. After that, find a GET category request on the proxy
3. Send to the repeater
4. Inject payload like this one `'+UNION+SELECT+NULL,NULL--`
5. You'll get a error
6. Relax just send it again and voila

![alt text](<img/Screenshot 2025-09-10 223149.png>)