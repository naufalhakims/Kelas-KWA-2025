# SQL injection vulnerability allowing login bypass

This lab contains a SQL injection vulnerability in the login function.

To solve the lab, perform a SQL injection attack that logs in to the application as the administrator user.

Here are the Solution :
1. Go to Login Page of the website 
2. Modify the username parameter, giving it the value: administrator'--
3. Type anything on the password

![alt text](<img/Screenshot 2025-09-10 114220.png>)

And if you login, you already in administrator account and solved the challenge

![alt text](<img/Screenshot 2025-09-10 114135.png>)