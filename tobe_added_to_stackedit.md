
## The GitHub flow:

The GitHub flow is branch-based workflow built around core Git commands used by teams around the globe—including ours.

**The GitHub flow has six steps, each with distinct benefits when implemented**:
 1. Create a branch: Topic branches created from the canonical deployment branch (usually master) allow teams to contribute to many parallel efforts. Short-lived topic branches, in particular, keep teams focused and results in quick ships.
 2. Add commits: Snapshots of development efforts within a branch create safe, revertible points in the project’s history.
 3. Open a pull request: Pull requests publicize a project’s ongoing efforts and set the tone for a transparent development process.
 4. Discuss and review code: Teams participate in code reviews by commenting, testing, and reviewing open pull requests. Code review is at the core of an open and participatory culture.
 5. Merge: Upon clicking merge, GitHub automatically performs the equivalent of a local ‘git merge’ operation. GitHub also keeps the entire branch development history on the merged pull request.
 6. Deploy: Teams can choose the best release cycles or incorporate continuous integration tools and operate with the assurance that code on the deployment branch has gone through a robust workflow.

### GitHub and the command line:

##### Example: Contribute to an existing repository

- download a repository on GitHub.com to our machine

`git clone https://github.com/me/
repo.git`

- change into the `repo` directory

`cd repo`

- create a new branch to store any new changes

`git branch my-branch`

- switch to that branch (line of development)

`git checkout my-branch`

- make changes, for example, edit `file1.md` and `file2.md` using the text editor

- stage the changed files

`git add file1.md file2.md`

- take a snapshot of the staging area (anything that's been added)

`git commit -m "my snapshot"`

- push changes to github

`git push --set-upstream origin my-
branch`
<hr>

##### Example: Start a new repository and publish it to GitHub

First, you will need to create a new repository on GitHub.

- create a new directory, and initialize it with git-specific functions

  `git init my-repo`

- change into the `my-repo` directory

  `cd my-repo`

- create the first file in the project

  `touch README.md`

- git isn't aware of the file, stage it

  `git add README.md`

- take a snapshot of the staging area

  `git commit -m "add README to initial commit"`

- provide the path for the repository you created on github

  `git remote add origin https://github.com/YOUR-USERNAME/YOUR-
  REPOSITORY.git`

- push changes to github

  `git push --set-upstream origin master`
---

Example: contribute to an existing branch on GitHub

> assumption: a project called `repo` already exists on the machine, and a new branch has been pushed to GitHub.com since the last time changes were made locally

- change into the `repo` directory

  `cd repo`

- update all remote tracking branches, and the currently checked out branch

  `git pull`

- change into the existing branch called `feature-a`

  `git checkout feature-a`

- make changes, for example, edit `file1.md` using the text editor.

- stage the changed file

  `git add file1.md`

- take a snapshot of the staging area

  `git commit -m "edit file1"`

- push changes to github

  `git push`

### Models for collaborative development

There are two primary ways people collaborate on GitHub:
- Shared repository
- Fork and pull

With a shared repository, individuals and teams are explicitly designated as contributors with read, write, or administrator access.

For an open source project, or for projects to which anyone can contribute, managing individual permissions can be challenging, but a fork and pull model allows anyone who can view the project to contribute.<strong> A fork is a copy of a project under an developer’s personal account</strong>. Every developer has full control of their fork and is free to implement a fix or new feature. Work completed in forks is either kept separate, or is surfaced back to the original project via a pull request. There, maintainers can review the suggested changes before they’re merged. See the Forking Projects Guide for more information.
