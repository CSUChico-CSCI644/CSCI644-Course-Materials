# Assignment 5

## Goals

* Build a web CI/CD deployment pipeline for the [Simple Microservice Example](https://github.com/CSUChico-CSCI644/simple-microservice-example)
* Should have stages for the following:
    * linting (can be faked)
    * testing (can be faked)
    * building
    * deployment
* Make a simple HTML change to show your name **after** initially committing your linting and testing pipeline so the change can be traced in the CI/CD pipeline results.

## Pipeline Requirements

Your CI/CD pipeline must:

* Include separate linting, testing, building, and deployment stages.
* Run a linting job before the build stage. This may be a simple placeholder or
  syntax check.
* Run a testing job before the build stage. This may be a simple placeholder or
  basic test command.
* Build a container image for the web application.
* Only publish or retag the image as `latest` during the deployment stage if the
  linting, testing, and building stages pass.

You do not need to deploy to Kubernetes, GCP, or a public website for this
assignment. For this assignment, the deployment stage may be publishing the
successfully built container image as the `latest` image.

## Required HTML Change

After your initial CI/CD pipeline is committed and running, make a second commit
that changes the frontend HTML to display your name.

For grading, make this exact change in `FrontendApplication/src/index.html`:

```html
<p id="student-name">Deployed by: First Last</p>
```

Replace `First Last` with your real name. Place this line inside the existing
hero section under the subtitle so it is visible on the page.

## Video Recording

In addition to submitting your code to the course repo, submit a short screen
recording to Canvas. Do not commit the video file to Git.

In the recording, walk through your submission and explain what each major part
does. Show your `.gitlab-ci.yml`, explain the linting, testing, building, and
deployment stages, show where the `latest` image is published or retagged, and
show the required HTML name change.

The goal is not video production quality. The goal is to show that you
understand the work you submitted and can explain the choices in your own words.

## Submission

If you don't have a CSCI644 Git repo, go to Canvas to see the instructions for generating a Git Repo for this class.

You will submit many of the the assignments for this class to separate branches on your CSCI644 repo. Make sure you make an initial **main** branch first as this will make things easier.

Now submit your all necessary files including *.gitlab-ci.yml* and any deployment files needed by your pipeline to the **assignment5** branch:

```bash
git checkout -b assignment5  #create branch and switch to it
git add -A  #add all
git commit -m "Assignment 5 Submission"  #Commit changes to branch
git push origin assignment5  #Push code up to assignment5 branch on remote
```

Make sure your branch is exactly named `assignment5` matching the case, spacing, etc as my grading script will only pull your submission if it matches exactly.

If you plan on making multiple updates to the code on this branch, you can include the `--set-upstream` option when you push the code (i.e. `git push --set-upstream origin assignment5`) -- this adds an upstream (tracking) reference so that, any time you push or pull from this branch in the future, you can simply use `git push` or `git pull`, without specifying the remote and branch.

If you would like to merge your `assignment5` branch with your `main` branch, you can run the following commands:
```bash
git checkout main  #switch to the main branch
git merge assignment5  #join the development history from the assignment1 branch with the current (main) branch
git push origin main  #push the assignment5 history up to the main branch on the remote
```
