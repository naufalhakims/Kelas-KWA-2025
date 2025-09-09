# User Credentials

This challenge was about exploiting an SQL Injection vulnerability to extract sensitive user credentials from the application's database.

The step by step in User Credentials simply same step like DatabaseSchema but with different payload like this `string')) UNION SELECT id,email,password,4,5,6,7,8,9 FROM users--`

![alt text](<img/Screenshot (28).png>)

after encoded it into url the paste it into the repeater and we will get user credentials responses

![alt text](<img/Screenshot (27).png>)

Solved!

![alt text](<img/Screenshot 2025-09-10 031612.png>)