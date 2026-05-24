# Assignment 3

## Goals

* Containerize [Simple Microservice Example](https://github.com/CSUChico-CSCI644/simple-microservice-example)
    * Should have multiple new Dockerfiles to containerize each component of the microservice:
        - API Gateway
        - Frontend Application
        - Backend QuoteService
        - MongoDB
        - NGINX
        - Should be able to use the default redis container image
* Create *docker-compose.yml* file to spin up the microservice

## Deployment Requirements

The application code already includes health checks, readiness checks, runtime
configuration, seed data, and end-to-end contract tests. Your work is to
containerize and connect the services correctly.

Your Docker Compose deployment must:

* Start the frontend, NGINX, API Gateway, QuoteService, MongoDB, and Redis.
* Make the application reachable from the host at `http://localhost:8080`.
* Configure service hostnames, ports, usernames, and passwords through Compose
  environment variables instead of editing application source files.
* Use a repeatable MongoDB seed/init approach that does not duplicate seed data.
* Include health checks for services that have `/healthz` or `/readyz` endpoints.
* Preserve Redis-backed quote count behavior across API calls while the stack is
  running.

The deployment is considered working when this passes from the repo root:

```bash
make test-e2e BASE_URL=http://localhost:8080
```

Include a `verification.md` file with the command you ran and the final contract
test output.

## Video Recording

In addition to submitting your code to the course repo, submit a short screen
recording to Canvas. Do not commit the video file to Git.

In the recording, walk through your submission and explain what each major part
does. Show your Dockerfiles, `docker-compose.yml`, service environment
variables, health checks, volumes, networking choices, and the contract test
result.

The goal is not video production quality. The goal is to show that you
understand the work you submitted and can explain the choices in your own words.

## Submission

If you don't have a CSCI644 Git repo, go to Canvas to see the instructions for generating a Git Repo for this class.

You will submit many of the the assignments for this class to separate branches on your CSCI644 repo. Make sure you make an initial **main** branch first as this will make things easier.

Now submit your Dockerfiles, microservice files, and docker-compose.yml to the **assignment3** branch:

```bash
git checkout -b assignment3  #create branch and switch to it
git add -A  #add all
git commit -m "Assignment 3 Submission"  #Commit changes to branch
git push origin assignment3  #Push code up to assignment3 branch on remote
```

Make sure your branch is exactly named `assignment3` matching the case, spacing, etc as my grading script will only pull your submission if it matches exactly.

If you plan on making multiple updates to the code on this branch, you can include the `--set-upstream` option when you push the code (i.e. `git push --set-upstream origin assignment3`) -- this adds an upstream (tracking) reference so that, any time you push or pull from this branch in the future, you can simply use `git push` or `git pull`, without specifying the remote and branch.

If you would like to merge your `assignment3` branch with your `main` branch, you can run the following commands:
```bash
git checkout main  #switch to the main branch
git merge assignment3  #join the development history from the assignment1 branch with the current (main) branch
git push origin main  #push the assignment3 history up to the main branch on the remote
```
