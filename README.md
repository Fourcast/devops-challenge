# Devops Technical Challenge
Repository containing the technical challenge for potential devops candidate

### Goal

Your goal is to illustrate how you would deploy and scale two applications (App A and App B) to incoming requests.

### Assignment

Your task is to accomplish the following:

- Deploy the sample python applications to a cluster of nodes using a container orchestration framework
- Application A should be publicly accessible over HTTPS
- Application B should not be accessible via the public internet

Please show how you would auto-scale the number of nodes and containers as the number of requests increases

### Deliverables

- A design architecture of the different resources used and how they communicate between each other
- A Dockerfile for each application
- IaC code for all the resources you deploy (you are encouraged to use Terraform).
- Document how you will use continuous integration to build the different artifacts for the different  environment (dev, acc, prod)
- Document how you will use continuous delivery to ship to the different environments (dev, acc, prod)
- A google cloud project with all the resources deployed

Notes
- Please do not fork or submit a PR to this repo
- Please document your thought-processes and use well-written git commit messages to show your progress
- Feel free to change the python application and its requirements in any way you see fit
- We are purposefully not being overly prescriptive in this assignment, as we want you to think creatively about the solution
- This assignment should take less than 8 hours to complete but again this depends on your familiarity with Google Cloud
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