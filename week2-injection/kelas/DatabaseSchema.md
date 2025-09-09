# Database Schema

The "Database Schema" challenge tests skills in extracting the database schema through SQL injection, which can reveal sensitive structural details of the backend database.

First thing first, we need to intercept and find the `res/product/search/q=payload?` and send to the repeater. Inject a UNION payload like this

```bash
string')) UNION SELECT 1, 2, 3, 4, 5, 6, 7, 8, sql FROM sqlite_schema--
```

encode it into url

![alt text](<img/Screenshot (30).png>)

after decode you can put it on payload and it will return a Structured Database in SQL

![alt text](<img/Screenshot (29).png>)

Solved!

![alt text](<img/Screenshot (31).png>)