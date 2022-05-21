# Contributing to a 3rd party repo for beginners

## Table of Contents

* [Pre-requisites](#pre-requisites)
* [What will you learn](#what-will-you-learn)
* [A good workflow to start with](#a-good-workflow-to-start-with)
  - [Initialize things](#initialize-things)
  - [Add your changes](#add-your-changes)
    - [Initialize a feature branch](#initialize-a-feature-branch)
    - [Feature development cycle](#feature-development-cycle)
  - [Cleaning up](#cleaning-up)
* [Workflow visualized](#workflow-visualized)

## Pre-requisites

You know and use basic git commands like 
`init`, `clone`, `add`, `commit`, 
`branch`, `checkout`, `merge`, `pull`, `push`.

You probably know and use git commands like
`fetch`, `pull --rebase`, `rebase`, `cherry-pick`.

You want to contribute to a repo you do not have write access to.

You do not know how to or do not feel confident working
with repos you do not have write access to.

You do not follow any firm workflow working with your own
repos or repos you do not have write access.

## What will you learn

* How to keep your fork in sync with a source repo
* How to minimize risks of conflicts
* How to keep your repo history tree as clean as possible
* How to contribute properly via pull requests

## A good workflow to start with

Some definitions:
 - **upstream** is a repo you want to contribute to
 - **origin** or **fork** is your own fork of an upstream
 - **local** is a local clone of origin
 - **master** is a default branch (`master` for older repos or `main` for more recent repos)

### Initialize things

 1. Fork an upstream: on GitHub navigate to the upstream and click **Fork** button.
 1. `git clone <origin-url>.git <project-directory>`
    on your machine to clone your fork
 1. `cd <project-directory>`
 1. `git remote add <upstream-url>.git` to enable upstream-related actions

### Add your changes

It is important to have your fork in sync with upstream,
employ branches and follow certain workflow
to minimize conflicts risks and keep the project's git history tree as clean as possible.

#### Initialize a feature branch

 1. sync local and origin with upstream
    `git checkout master && git pull upstream master && git push origin master`
 1. create a feature branch with a meaningful name
    `git checkout -b <feature-branch-name>`
    
> There are many branch naming conventions. Few to mention are:
> * start with author initials so other collaborators know who
>   initialized the branch and also find branches per author, e.g. `or-feature-portview`
> * use slashes to denominate scopes, e.g. `feature/api/rest`, `bugfix/sleep`
> * use ticket/issue/epic/story id, e.g. `feat/epic123/story128/search-people`

Useful alias:

`git config --global alias.sync-master '!git checkout master && git pull upstream master && git push origin master'`

Usage: `git sync-master`
 
#### Feature development cycle

 1. do whatever you want on a dedicated feature branch
 1. commit often: `git add . && git commit -m "Add REST api PATCH method"`
 1. squash eventually grouping commits as appropriate:
    `git rebase -i <REF>`
    ([Making use of git rebase](https://gist.github.com/OleksiyRudenko/232e1ebe6ed0780fc69d7391723cc75b))
 1. sync eventually local, origin, and feature branch with upstream
    * `git checkout master && git pull upstream master && git push origin master`
    * `git checkout - && git merge master`
    * resolve conflicts using your IDE or command line
    * when done `git add . && git commit -m "Resolved merge conflict by incorporating both suggestions"`
    * see also 
      [Resolving a merge conflict using the command line](https://help.github.com/articles/resolving-a-merge-conflict-using-the-command-line/)
 1. go to `#1`
 1. eventually push to origin: `git push origin <feature-branch-name>`

Useful alias:

`git config --global alias.sync-branch '!git sync-master && git checkout - && git merge master'`

Usage: `git sync-branch` (it also does `sync-master` as a part of the flow)

**Commit message**

There are numbers of commit message structure conventions.
To mention a few:
 * start with commit scope, e.g. one of `feat|fix|docs|style|refactor|test|chore`
 * add feature/fix scope, e.g. `(api)`
 * use imperative mood in the subject line, e.g. one of `Add|Change|Fix|Refactor|Remove|Bump version|Release version`
 
If you resolve an issue (in upstream or fork) it is useful
to have a note on issue resolution.

Your commit message may look like the following
```
fix(foo api): Fix ABC component render conditions

Resolves: #12
See also: #34, #78
```

Further reading:
 * [Conventional Commits 1.0.0-beta.2](https://www.conventionalcommits.org/en/v1.0.0-beta.2/)
 * [How to Write a Git Commit Message](https://chris.beams.io/posts/git-commit/)
 * [5 Useful Tips For A Better Commit Message](https://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message)
 * [Semantic release](https://github.com/semantic-release/semantic-release)
 * [even more...](https://www.google.com/search?q=writing+a+good+commit+message)

**DON'Ts**

Do not squash or rebase what is already on remotes!

Do not overwrite hsitory on remotes!

**NB**

The above doesn't cover the case when you work on the same branch
with someone else,
when you will prefer `git pull --rebase` over `git pull`.

### Contribute via pull request

Contributing is not necessarily required.
You may develop your fork for your own purposes
(adhering to upstream license conditions).

Otherwise stick to the following contribution workflow:

 1. `git push origin <feature-branch-name>` to push your feature branch to the origin.
 1. Navigate to the cloud git hub (e.g. GitHub)
 1. Use cloud UI to create the PR
 1. Pass through code review process until your
    changes are merged or declined
    
Once your feature branch gets merged you will find your commits
in upon next sync with upstream. So, you don't need merging those
to your `master` locally.

However, you will need to merge into `master` if you do not
contribute to the upstream or your PR is declined and you want
to keep those for yourself.

### Cleaning up

Once your PR approved and merged you can get rid of your feature branch:
 - `git branch -D feature-branch` locally
 - `git push --delete origin feature-branch` on your remote

## A better workflow

<details><summary>Work In Progress under the cut</summary>

1. Keep things in sync
1. When base branch (`master`) gets updated, rebase feature branch onto it
   - NB! If a feature branch is on remote already then after rebase
     `push --force` is required to get the remote updated; USE WITH CAUTION
   - an alternative solution: branch off from master (new branch) and
     cherry-pick from old branch or rebase from the old branch onto new branch;
     remove old branch both locally and on remote
1. When ready to update `master`
   - cherry-pick or rebase onto master and squash (using e.g. PR)
   - remove feature branch
   
</details>


## Workflow visualized

[Basic git contribution workflow visualized](https://docs.google.com/presentation/d/13dati5gvA5f_hQFgxJPhPicjF5CRKu1e75RSsahmEaU)
