# Assignment 2

## Goals

* Use Ansible 
* Deploy [Simple Microservice Example](https://github.com/CSUChico-CSCI644/simple-microservice-example) to GCP via Ansible and Ansible gcloud support
* Submit Ansible Playbook(s) to accomplish this.

## Submission

If you don't have a CSCI644 Git repo, go to Canvas to see the instructions for generating a Git Repo for this class.

You will submit all the assignments for this class to separate branches on your CSCI644 repo. Make sure you make an initial **main** branch first as this will make things easier.

Now submit your code to the **assignment2** branch:

```bash
git checkout -b assignment2  #create branch and switch to it
git add -A  #add all
git commit -m "Assignment 2 Submission"  #Commit changes to branch
git push origin assignment2  #Push code up to assignment1 branch on remote
```

Make sure your branch is exactly named `assignment2` matching the case, spacing, etc as my grading script will only pull your submission if it matches exactly.

If you plan on making multiple updates to the code on this branch, you can include the `--set-upstream` option when you push the code (i.e. `git push --set-upstream origin assignment2`) -- this adds an upstream (tracking) reference so that, any time you push or pull from this branch in the future, you can simply use `git push` or `git pull`, without specifying the remote and branch.

If you would like to merge your `assignment2` branch with your `main` branch, you can run the following commands:
```bash
git checkout main  #switch to the main branch
git merge assignment2  #join the development history from the assignment1 branch with the current (main) branch
git push origin main  #push the assignment1 history up to the main branch on the remote
```