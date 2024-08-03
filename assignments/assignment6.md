# Assignment 6

## Goals

* Build a CI/CD deployment pipeline for the [Simple AI Example]()
* Should have the following stages:
    * training
    * testing/validation
    * deployment
        * only if validates higher than existing model
* Commit the pipeline with the initial model, then improve the model and trigger the pipeline again. Finally, trigger the pipeline, with a model that is worse to demo that the deployment only happens if model is improved.


## Submission

If you don't have a CSCI644 Git repo, go to Canvas to see the instructions for generating a Git Repo for this class.

You will submit many of the the assignments for this class to separate branches on your CSCI644 repo. Make sure you make an initial **main** branch first as this will make things easier.

Now submit your all necessary files including *.gitlab-ci.yml* file to the **assignment6** branch. Should also include a file called **web.md** in the root path of your repo with the URL where your hosted deployment after the CI/CD completes is located:

```bash
git checkout -b assignment6  #create branch and switch to it
git add -A  #add all
git commit -m "Assignment 6 Submission"  #Commit changes to branch
git push origin assignment6  #Push code up to assignment6 branch on remote
```

Make sure your branch is exactly named `assignment6` matching the case, spacing, etc as my grading script will only pull your submission if it matches exactly.

If you plan on making multiple updates to the code on this branch, you can include the `--set-upstream` option when you push the code (i.e. `git push --set-upstream origin assignment6`) -- this adds an upstream (tracking) reference so that, any time you push or pull from this branch in the future, you can simply use `git push` or `git pull`, without specifying the remote and branch.

If you would like to merge your `assignment6` branch with your `main` branch, you can run the following commands:
```bash
git checkout main  #switch to the main branch
git merge assignment6  #join the development history from the assignment1 branch with the current (main) branch
git push origin main  #push the assignment6 history up to the main branch on the remote
```