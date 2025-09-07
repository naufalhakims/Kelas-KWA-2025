# Login Admin

The Admin Login challenge is tutorial question number 1, which contains instructions to log in as an admin using SQL injection. Here we are shown a payload to perform SQL injection. It contains a string such as`OR true --`. This command will break the query and we will login to the admin account. We dont have to think about the password since we can use SQLi.

![alt text](img/image-1.png)

Now let's see if its works

![alt text](img/image.png)

As you can see we already logged in with admin@juice-sh.op and here we go we solved it.

![alt text](img/image-2.png)