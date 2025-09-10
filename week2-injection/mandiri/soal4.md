# More SQL
Resource : https://play.picoctf.org/practice/challenge/358?page=1&search=sql 

This challenge is similar as SQLite, we use payload `'OR 1=1; -- //` to solved the challenge

First, open up your burpsuite to intercept it, and once you input the username and pasword exactly just like as the payload you like this

![alt text](<img/Screenshot 2025-09-10 215312.png>)

The flag appeared on response

![alt text](<img/Screenshot (32).png>)

And solved!