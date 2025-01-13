# Assignment 4

## Goals

* Build on containerization of [Simple Microservice Example](https://github.com/CSUChico-CSCI644/simple-microservice-example) from assignment 3.
* Deploy [Simple Microservice Example](https://github.com/CSUChico-CSCI644/simple-microservice-example) as a Kubernetes deployment.
  * You should not publish any containers to container registries, everything should be built locally. Use of existing published official containers is allowed.
* Build a run script to spin up everything on a fresh cluster.


## Submission

You should submit **all** files needed to build and deploy. You should also submit a run script that will start your minikube cluster, build, and deploy all from the single script.

### Submitting

If you don't have a CSCI644 Git repo, go to Canvas to see the instructions for generating a Git Repo for this class.

You will submit many of the the assignments for this class to separate branches on your CSCI644 repo. Make sure you make an initial **main** branch first as this will make things easier.

Now submit your all necessary files including your kubernetes *yaml* deployment file(s) to the **assignment4** branch:

```bash
git checkout -b assignment4  #create branch and switch to it
git add -A  #add all
git commit -m "Assignment 4 Submission"  #Commit changes to branch
git push origin assignment4  #Push code up to assignment4 branch on remote
```

Make sure your branch is exactly named `assignment4` matching the case, spacing, etc as my grading script will only pull your submission if it matches exactly.

If you plan on making multiple updates to the code on this branch, you can include the `--set-upstream` option when you push the code (i.e. `git push --set-upstream origin assignment4`) -- this adds an upstream (tracking) reference so that, any time you push or pull from this branch in the future, you can simply use `git push` or `git pull`, without specifying the remote and branch.

If you would like to merge your `assignment4` branch with your `main` branch, you can run the following commands:
```bash
git checkout main  #switch to the main branch
git merge assignment4  #join the development history from the assignment1 branch with the current (main) branch
git push origin main  #push the assignment4 history up to the main branch on the remote
```
