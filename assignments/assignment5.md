# Assignment 5

## Goals

* Build a web CI/CD deployment pipeline for the [Simple Microservice Example](https://github.com/CSUChico-CSCI644/simple-microservice-example)
* Should have stages for the following:
    * linting (can be faked)
    * testing (can be faked)
    * building
    * deployment
* Make a simple change to HTML to have your name **after** initially committing your linting and testing so that can be traced/seen from CI/CD pipeline results.


## Submission

If you don't have a CSCI644 Git repo, go to Canvas to see the instructions for generating a Git Repo for this class.

You will submit many of the the assignments for this class to separate branches on your CSCI644 repo. Make sure you make an initial **main** branch first as this will make things easier.

Now submit your all necessary files including *.gitlab-ci.yml* file to the **assignment5** branch. Should also include a file called **web.md** in the root path of your repo with the URL where your hosted deployment after the CI/CD completes is located:

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
