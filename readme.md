<!--
Creator:
Location: SF
-->

![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png)

# Data Associations with Mongoose

### Why is this important?
<!-- framing the "why" in big-picture/real world examples -->
*This workshop is important because:*

- Git is a powerful tool for collaborating on code.

- GitHub is a popular online service for managing git repositories.

- Using git repositories for collaboration will be important throughout a web developer's career.

### What are the objectives?
<!-- specific/measurable goal for students to achieve -->
*After this workshop, developers will be able to:*


- Create their own git branches and explain a pattern for using branches to develop a full application.
- Make a new repository and add another developer as a collaborator.
- Resolve a merge conflict.

### Where should we be now?
<!-- call out the skills that are prerequisites -->
*Before this workshop, developers should already be able to:*

* Use git to stage and commit changes locally.
* Explain what the following terms mean for GitHub: pull, push, fork, clone, pull request.

## Branches

In Git, branches are a part of your everyday development process. When you want to add a new feature or fix a bug — no matter how big or how small — you spawn a new branch to encapsulate your changes. This makes sure that unstable code is never committed to the main code base, and it gives you the chance to clean up your feature’s history before merging it into the main branch.

Branches are incredibly lightweight "movable pointers" that help us as developers make experimental changes! A branch in git is just a label or pointer to a particular commit in a repository, along with all of it's history (parent commits).

What makes a branch special in git, is that we're always on a specific branch, and when we commit, the current branch HEAD moves forward to the new commit. Another way to say that is the HEAD always stays at the tip of the branch.

Terminology: HEAD is simply a reference to the current or most recent commit!


![Git Branch Diagram](https://www.atlassian.com/git/images/tutorials/collaborating/using-branches/01.svg)






Q. Why is branching an important part of git?
---

> A. Branches are useful for many reasons, but some of the most common ones:

> 1. To allow experimentation. By switching to a new branch, we can experiment,
and if the experiment fails, we can delete it and easily switch back to master
(or another branch of our choice). If it succeeds, we can merge those changes
into master.
2. To allow work to proceed on multiple features (or by multiple people) without
interfering. When a feature is complete, it can be merged back into master.
3. To allow easy bug fixes on a stable version while features are being developed.

## `git fetch`, `git merge`, and `git pull`

Fetching, merging, and pulling are related commands that you will frequently use to update your local repository to include your collaborator's work.

[`git fetch`](https://git-scm.com/docs/git-fetch) gets all of the updates from the remote repositories without changing the location of the local HEAD.

[`git merge`](https://git-scm.com/docs/git-merge) joins two different places in your development tree. This is frequently used to bring together your changes with the changes you just fetched. If you were on branch `add-auth` and you had just `git fetch`'d updates from the remote, you could then `git merge origin/add-auth`. This would join your changes and the changes that had been made to this branch on origin. You also commonly use merge to pull changes from one branch into another so that your current branch doesn't become out of date while you work.

[`git pull`](https://git-scm.com/docs/git-pull) is the combination of fetching and merging to the newly fetched version of the current branch.

![image](https://cloud.githubusercontent.com/assets/6520345/15020568/663aa804-11d7-11e6-83f6-774e43bc2ea6.png)

## Collaboration Workflows

There are two main scenarios for collaborating on coding projects:

1. You **fork** another developer's project and make pull requests from *your remote fork* to the *project's remote*.
2. Another developer makes you a **collaborator** on a project they own, giving you the ability to make pull requests directly from the project's *remote feature branches* to the project's *remote master*. (Note that as a collaborator on a project, you also have the ability to push directly to the master branch, which you should NEVER do.)

For this project, you should be collaborators!

![github-collab-diagram](https://cloud.githubusercontent.com/assets/7833470/12072895/69abd404-b0b1-11e5-8d8c-4ff54c13b0a0.png)

## Practice: Create and resolve a merge conflict

1. Pair up. Have one partner create a brand new repository on GitHub and [add your partner as a collaborator](https://help.github.com/articles/adding-collaborators-to-a-personal-repository/).
2. The person who created the GitHub repository should create a new project directory locally, generate one  `index.html` file, create a `readme.md` with some content, and push the new app to the remote repository.
3. The collaborator should then clone this repository.
4. Each person is about to change the README completely, and add 2 elements to `index.html`.  FIRST! Each person should start a new feature branch.  (Name them different things, like `better-readme` and `best-readme`.) You can check that you have all of the branches with `git branch`-that will print all of the branch names.
5. Now, have the original repo creator commit and push the work to GitHub on *their* branch. (E.g., `git push origin better-readme`.)  Open a pull request from the new branch to the master branch.
6. The collaborator should commit their changes and push the work to GitHub on *their* branch. (E.g., `git push origin best-readme`.) Open a pull request from the new branch to the master branch.
7. Choose a pull request to accept first. It shouldn't have any merge conflicts with the master branch, so you can just merge it in on GitHub.
8. The second pull request should be a little more interesting. We hope that we have created at least one merge conflict. [Resolve the merge conflict locally](https://github.com/SF-WDI-LABS/shared_modules/blob/master/how-to/github-collaboration-workflow.md#resolving-merge-conflicts-locally) on one of your computers and push the fixed version to GitHub.  
9. Feel free to delete this practice repository from your local machine and from GitHub. This workflow was intentionally sloppy and I'm hoping that you learned a little bit of what *not* to do.


## Resources

* **[WDI In-depth Guide for Teams Using GitHub](https://github.com/SF-WDI-LABS/shared_modules/blob/master/how-to/github-collaboration-workflow.md)**
* <a href="https://help.github.com/articles/adding-collaborators-to-a-personal-repository" >Adding collaborators to a personal repository</a>
* <a href="http://nvie.com/posts/a-successful-git-branching-model" >A successful Git branching model from industry</a>
* <a href="https://help.github.com/articles/using-pull-requests" >Using pull requests</a>

## Tutorials

* **We recommend you try Levels 1-3 of this [git branching tutorial](http://pcottle.github.io/learnGitBranching/).** Stop at 4: "Rebase Introduction". Take your time:
  * Read all the dialogs. They are part of the tutorial.
  * Think about what you want to achieve.
  * Think about the results you expect before you press enter.
  * Whenever you see/type `git commit`, you can assume some changes have been made and staged.
* <a href="https://www.codeschool.com/courses/try-git" >Try Git - Code School</a>
* <a href="https://github.com/Gazler/githug" >githug</a>
