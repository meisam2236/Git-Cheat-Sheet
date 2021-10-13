- [Configuration](#configuration)
  - [username for all projects](#username-for-all-projects)
  - [email for all projects](#email-for-all-projects)
  - [username for the project](#username-for-the-project)
  - [email for the project](#email-for-the-project)
- [Starting project](#starting-project)
  - [Create a project in local machine](#create-a-project-in-local-machine)
  - [Create an entry in git](#create-an-entry-in-git)
  - [Clone a project from server to local machine](#clone-a-project-from-server-to-local-machine)
- [Common Commands](#common-commands)
  - [Show changes compare to last commit](#show-changes-compare-to-last-commit)
  - [Add file to staging area(ready to commit)](#add-file-to-staging-areaready-to-commit)
  - [Add all files to staging area](#add-all-files-to-staging-area)
  - [Show changes compare to last stage](#show-changes-compare-to-last-stage)
  - [Show changes of the stage files compare to last commit](#show-changes-of-the-stage-files-compare-to-last-commit)
  - [Show changes compare to last commit](#show-changes-compare-to-last-commit-1)
  - [Commit](#commit)
  - [Remove file from repository](#remove-file-from-repository)
  - [Save unfinished changes compare to last commit without commiting](#save-unfinished-changes-compare-to-last-commit-without-commiting)
  - [Recover stash](#recover-stash)
  - [Drop stash](#drop-stash)
- [Working with Branches](#working-with-branches)
  - [Show repository branches](#show-repository-branches)
  - [Show repository branches with remote branches](#show-repository-branches-with-remote-branches)
  - [Create new branch](#create-new-branch)
  - [Move to branch](#move-to-branch)
  - [Create a branch and move to it](#create-a-branch-and-move-to-it)
  - [Merge branch to current branch](#merge-branch-to-current-branch)
  - [Rebase branch to current branch](#rebase-branch-to-current-branch)
  - [Remove branch](#remove-branch)
- [Connection to Server Project](#connection-to-server-project)
  - [Get and show changes of the remote server project without applying to local](#get-and-show-changes-of-the-remote-server-project-without-applying-to-local)
  - [Get and merge changes of the remote server project](#get-and-merge-changes-of-the-remote-server-project)
  - [Send changes to remote server](#send-changes-to-remote-server)
  - [Send new tags to remote server](#send-new-tags-to-remote-server)
  - [Send new branch to remote server](#send-new-branch-to-remote-server)
- [Checking Past Commits](#checking-past-commits)
  - [Show all commits](#show-all-commits)
  - [Show last commits(with number)](#show-last-commitswith-number)
  - [Show last commits in graph](#show-last-commits-in-graph)
  - [Show user commits](#show-user-commits)
  - [Show commits of the file](#show-commits-of-the-file)
- [Tag Commits](#tag-commits)
  - [Show all repository tags](#show-all-repository-tags)
  - [Add tag to last commit](#add-tag-to-last-commit)
  - [Remove tag](#remove-tag)
- [Repair Errors](#repair-errors)
  - [Removing file commits and restoring to last commit](#removing-file-commits-and-restoring-to-last-commit)
  - [Restore changes of the staging area](#restore-changes-of-the-staging-area)
  - [Back to certain commit and removing commits between](#back-to-certain-commit-and-removing-commits-between)
  - [Back to certain commit and removing commits between without minding changes in files](#back-to-certain-commit-and-removing-commits-between-without-minding-changes-in-files)
  - [Create a commit with reverse of the changes](#create-a-commit-with-reverse-of-the-changes)
  - [Add changes to last commit](#add-changes-to-last-commit)
  - [Remove changes after last commit in local project](#remove-changes-after-last-commit-in-local-project)
- [Other Commands](#other-commands)
  - [Create custom shortcut for useful command](#create-custom-shortcut-for-useful-command)
  - [Start search operation for commit with bug](#start-search-operation-for-commit-with-bug)
  - [Specify commit without bug](#specify-commit-without-bug)
  - [Specify commit with bug](#specify-commit-with-bug)
  - [Apply certain commit to branch in a new commit](#apply-certain-commit-to-branch-in-a-new-commit)
# Configuration
## username for all projects
```shell
git config --global user.name <username>
```
## email for all projects
```shell
git config --global user.email <email>
```
## username for the project
```shell
git config --local user.name <username>
```
## email for the project
```shell
git config --local user.email <email>
```
# Starting project
## Create a project in local machine
```shell
git init <project name>
```
## Create an entry in git
```shell
git remote add <name> <url>
```
## Clone a project from server to local machine
```shell
git clone <url>
```
# Common Commands
## Show changes compare to last commit
```shell
git status
```
## Add file to staging area(ready to commit)
```shell
git add <file name>
```
## Add all files to staging area
```shell
git add
```
## Show changes compare to last stage
```shell
git diff <file name>
```
## Show changes of the stage files compare to last commit
```shell
git diff --staged <file name>
```
## Show changes compare to last commit
```shell
git diff HEAD
```
## Commit
```shell
git commit
```
## Remove file from repository
```shell
git rm <file name>
```
## Save unfinished changes compare to last commit without commiting
```shell
git stash
```
## Recover stash
```shell
git stash apply
```
## Drop stash
```shell
git stash drop
```
# Working with Branches
## Show repository branches
```shell
git branch
```
## Show repository branches with remote branches
```shell
git branch -a
```
## Create new branch
```shell
git checkout <branch name>
```
## Move to branch
```shell
git checkout <branch name>
```
## Create a branch and move to it
```shell
git checkout -b <branch name>
```
## Merge branch to current branch
```shell
git merge <branch name>
```
## Rebase branch to current branch
```shell
git rebase <branch name>
```
## Remove branch
```shell
git branch -d <branch name>
```
# Connection to Server Project
## Get and show changes of the remote server project without applying to local
```shell
git fetch
```
## Get and merge changes of the remote server project
```shell
git pull
```
## Send changes to remote server
```shell
git push
```
## Send new tags to remote server
```shell
git push --tags
```
## Send new branch to remote server
```shell
git push -u <remote name> <branch name>
```
# Checking Past Commits
## Show all commits
```shell
git log
```
## Show last commits(with number)
```shell
git log -n <c>
```
## Show last commits in graph
```shell
git log --online--graph--decorate
```
## Show user commits
```shell
git log --author= <X>
```
## Show commits of the file
```shell
git log -- <file name>
```
# Tag Commits
## Show all repository tags
```shell
git tag
```
## Add tag to last commit
```shell
git tag <name>
```
## Remove tag
```shell
git tag -d <name>
```
# Repair Errors
## Removing file commits and restoring to last commit
```shell
git restore <file name>
```
## Restore changes of the staging area
```shell
git restore --staged <file name>
```
## Back to certain commit and removing commits between
```shell
git reset <commit>
```
## Back to certain commit and removing commits between without minding changes in files
```shell
git reset --hard <commit>
```
## Create a commit with reverse of the changes
```shell
git revert <commit>
```
## Add changes to last commit
```shell
git commit --amend
```
## Remove changes after last commit in local project
```shell
git clean
```
# Other Commands
## Create custom shortcut for useful command
```shell
git config --globalalias <alias> <command>
```
## Start search operation for commit with bug
```shell
git bisect start
```
## Specify commit without bug
```shell
git bisect good <commit>
```
## Specify commit with bug
```shell
git bisect bad <commit>
```
## Apply certain commit to branch in a new commit
```shell
git cherry-pick <commit>
```
