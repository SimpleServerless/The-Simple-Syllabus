# The Simple Syllabus
 
### Lesson 1: A simple routing framework
If you're embedding a fat web server in your serverless function just to do routing, you're doing it wrong. With about 100 lines of code you
do something like this.
```
@router.rest("GET", "/students")
def list_students(args: dict) -> dict:
    ...
    return student_list
```

Repo: [simple-routing](https://github.com/SimpleServerless/simple-routing)

---

### Lesson 2: Iterating on and testing your lambda locally
If to you debugging means adding print statements and deploying your code to the cloud to see what happens, you're doing
it wrong. Lambdas are pretty simple. It's a function that takes two dictionaries for input. Learn how to use the 
`run_local.py` script to iterate and debug in your shell or IDE. No containers or extra tools required.

Repo: [simple-routing](https://github.com/SimpleServerless/simple-routing)

---

### Lesson 3: A dynamic routing framework
Building on **Lesson 1** we use CDK to add a few lines of code to scan our lambda for `@router` decorators
and dynamically deploy the REST routes on API Gateway or graphql resolvers on AppSync. Now all you need to do to
turn a function in a lambda into an API endpoint is type `@router.rest("GET", "/students")` above it.

Repo: [dynamic-routing](https://github.com/SimpleServerless/dynamic-routing)

---

### Lesson 4: Run a relational database for $1
A turnkey RDS deployment so you can run a secure relational database for your side projects and keep your 
prototyping costs down.

Repo: [simple-database](https://github.com/SimpleServerless/simple-database)

---

### Lesson 5: Run a bastion host for $1
A turnkey bastion host deployment so you can tunnel to the relational database from **Lesson 4** and query it from your laptop.

Repo: [simple-bastion](https://github.com/SimpleServerless/simple-bastion)

---

### Lesson 6: Database connections
There are lots of ways to do this and some ways can get expensive. Here's something that works for a moderate scale, doesn't
cost any extra, and keeps your lambda clean. Just add `@tansaction` above your function and a connection is injected.

Repo: [simple-db-connection](https://github.com/SimpleServerless/simple-db-connection)

---

### Blogs, videos and more lessons are on the way

