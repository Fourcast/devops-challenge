# Devops Technical Challenge
Repository containing the technical challenge for potential devops candidate


# Important Notes
- Please do not submit a PR to this repo
- Please document your thought-processes and use well-written git commit messages to show your progress
- Feel free to change the python application and its requirements in any way you see fit
- We are purposefully not being overly prescriptive in this assignment, as we want you to think creatively about the solution
- This assignment should take less than 6 hours to complete but you can let us know if you need more time to complete it.
- If you get stuck or need more information, please reach out for clarity
- Have fun!

### Getting Started in Local Development

Running the apps locally:
```
pip install -r requirements.txt
sqlite3 database.db < schema.sql
python app_a.py
python app_b.py
```

Making a request
```
curl -X POST -H 'Authorization: mytoken' http://127.0.0.1:5000/jobs
```

Simulating a lot of requests
```
ab -m POST -H "Authorization: mytoken" -n 500 -c 4 http://127.0.0.1:5000/jobs
```
