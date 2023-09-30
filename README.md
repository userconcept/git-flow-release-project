# git-flow-release-project

Git-flow project start, release and update cycle (Git-Flow, Release, Tags, SemVer, Conventional Commits).

## GitHub interface:

**Create repository: \<git-flow-release-project\>**

## Local:

`mkdir git-flow-release-project && cd git-flow-release-project`

**Add initial project files to created directory: README.md, package.json, .gitignore, etc**

`git init`

`git add .`

`git commit -m "feat: username create repository with project v0.1.0"`

`git branch -M main`

`git remote add origin git@github.com:username/git-flow-release-project.git`

`git tag -a v0.1.0 -m "Release v0.1.0"`

`git push -u origin main --tags`

## GitHub interface:

**Create a new release**

**Choose a tag: v0.1.0**

**Release title: v0.1.0**

**Describe this release:**

```Markdown
## Initial release v0.1.0

Initial release v0.1.0 of git-flow project

## Features

* [Create repository](https://github.com/userconcept/git-flow-release-project/commit/<commit_hash>): feat: userconcept create repository with project v0.1.0
```

**Publish release**

## Local:

**Create \<develop\> branch from \<main\> and push it with --set-upstream:**

`git checkout -b develop` (develop branch)

`git push -u origin develop`

**Create \<feature\> branch from \<develop\>:**

`git checkout develop`

`git checkout -b feature/username/add-contributing.md` (feature branch)

**Add some feature, for example - create CONTRIBUTING.md file**

`git add .`

`git commit -m "feat: username add contributing.md"`

`git push -u origin feature/username/add-contributing.md`

## GitHub interface:

**Compare & Pull Request**

**Pull Request from \<feature/username/add-contributing.md\> to \<develop\> branch**

**Leave a comment: Add CONTRIBUTING.md file**

**Create pull request**

**Merge pull request**

**Confirm merge**

## Local:

**Create \<release\> branch from \<develop\>:**

`git checkout develop`

`git pull`

`git checkout -b release/v0.2.0` (release branch)

**Bump SemVer to v0.2.0 in package.json, etc**

`git add .`

`git commit -m "feat: username bump SemVer to v0.2.0"`

`git push -u origin release/v0.2.0`

## GitHub interface:

**Compare & Pull Request**

**Pull Request from \<release/v0.2.0\> to \<main\> branch**

**Leave a comment: Release v0.2.0 of git-flow project**

**Create pull request**

**Merge pull request**

**Confirm merge**

## Local:

**Pull \<main\> branch with release code version, add tag and push it:**

`git checkout main`

`git pull`

`git log --pretty=oneline`

`git tag -a v0.2.0 -m "Release v0.2.0" <abbreviated commit hash>`

`git push origin v0.2.0`

**Merge release code version from \<release/v0.2.0\> to \<develop\> branch and push it:**

`git checkout develop`

`git pull`

`git merge --no-ff release/v0.2.0`

`git push`

## GitHub interface:

**Draft new release**

**Choose a tag: v0.2.0**

**Release title: v0.2.0**

**Describe this release:**

```Markdown
## Release v0.2.0

Release v0.2.0 of git-flow project

## Features

* [#1](https://github.com/userconcept/git-flow-release-project/pull/1): feat: userconcept add contributing.md
```

**Publish release**

## Local:

**Create \<hotfix\> branch from \<main\>:**

`git checkout main`

`git pull`

`git checkout -b hotfix/v0.2.1` (hotfix branch)

**Bump SemVer to v0.2.1 in package.json, etc**

`git add .`

`git commit -m "feat: username bump SemVer to v0.2.1"`

**Add some fixes, for example - add text to CONTRIBUTING.md file**

`git add .`

`git commit -m "fix: username add text to contributing.md"`

`git push -u origin hotfix/v0.2.1`

## GitHub interface:

**Compare & Pull Request**

**Pull Request from \<hotfix/v0.2.1\> to \<main\> branch**

**Leave a comment: Release hotfix v0.2.1 of git-flow project**

**Create pull request**

**Merge pull request**

**Confirm merge**

## Local:

**Pull \<main\> branch with release code version, add tag and push it:**

`git checkout main`

`git pull`

`git log --pretty=oneline`

`git tag -a v0.2.1 -m "Release hotfix v0.2.1" <abbreviated commit hash>`

`git push origin v0.2.1`

**Merge hotfix code version from \<hotfix/v0.2.1\> to \<develop\> branch and push it:**

`git checkout develop`

`git pull`

`git merge --no-ff hotfix/v0.2.1`

`git push`

## GitHub interface:

**Draft new release**

**Choose a tag: v0.2.1**

**Release title: v0.2.1**

**Describe this release:**

```Markdown
## Release v0.2.1

Release hotfix v0.2.1 of git-flow project

## Fixes

* [#3](https://github.com/userconcept/git-flow-release-project/pull/3): fix: userconcept add text to contributing.md
```

**Publish release**

## Project page

[https://github.com/userconcept/git-flow-release-project](https://github.com/userconcept/git-flow-release-project)

## My website

[https://userconcept.ru](https://userconcept.ru)
