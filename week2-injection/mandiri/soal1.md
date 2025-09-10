# SQL injection vulnerability in WHERE clause allowing retrieval of hidden data
Resource : https://portswigger.net/web-security/sql-injection/lab-retrieve-hidden-data

This lab contains a SQL injection vulnerability in the product category filter. When the user selects a category. To solve the lab, perform a SQL injection attack that causes the application to display one or more unreleased products. Here are the solution :

1. Use Burp Suite to intercept and modify the request that sets the product category filter.
2. Modify the category parameter, giving it the value '+OR+1=1--
3. Submit the request, and verify that the response now contains one or more unreleased products.

If you already do the following step above you will get a congratulations from the lab like this

![alt text](<img/Screenshot 2025-09-10 110156.png>)