# Prerequisites

## Setting up/updating the git environment and git flow

[Get the installer](https://git-scm.com/downloads)

{% hint style="info" %}
Git-flow library:\
For Windows, is natively integrated.\
For Mac, [here is the procedure](https://git-scm.com/download/mac).\
Pour Linux, [here is the procedure.](https://howtoinstall.co/en/git-flow)
{% endhint %}

```
[INPUT]
git flow init

[OUTPUT]
Which branch should be used for bringing forth production releases?
   - main
Branch name for production releases: [main] 
Branch name for "next release" development: [develop] 

How to name your supporting branch prefixes?
Feature branches? [feature/] 
Bugfix branches? [bugfix/] 
Release branches? [release/] 
Hotfix branches? [hotfix/] 
Support branches? [support/] 
Version tag prefix? [] 
Hooks and filters directory? [/home/louc/Documents/Git/MON1/Labo-Master/.git/hooks] 

```

* [x] Confirm the installed version

```
[INPUT]
git flow version

[OUTPUT]
1.12.3 (AVH Edition)
```

* [ ] What do you think about this release?

```
Changelog

    Explicitly get the default values from the system and global config.

```

## What's git-flow, branches feature.

[Source](https://nvie.com/posts/a-successful-git-branching-model/)

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption><p>Source : A successful git branching model</p></figcaption></figure>

* [x] Which branches are persistent and what do they contain?

```
- Master, contain the production application
- Develop, contain the delepooing form of application

```

* [x] Why do we have to merge hotfix in both master and develop branches, but not into all active feature branches?

```
The modifications added in others branches are not include in changes at the moment of the hotfix opperation.
They will be merged in a second time, when features branches will be merged.   
```

## Initialize git flow on an existing project

* [x] What happens when you run the "git flow init" command on an existing local repository?

```
Creation of two branches "Master and Develop", ask for namming other futures branches and switch in branch develop.
```

* [x] When do we need to make this git command?

```
Aflet clonning a repo or at the innitialisation of it.
```

## Practice the basic git commands

[Source](https://www.atlassian.com/git/glossary)

* [x] What does this git command "git add -all" achieve (.gitignore impacts)?

```
File usually ignored by the file .gitignore will be not ignored and add in the next commit 
```

* [x] What does this git command "git status" achieve?

```
Display the status of the current repo, show witch files are already added or not for the next commit. 
Show files deleted or added.  
```

* [x] What does this git command "git remote add upstream \<url>" achieve?

```
Add a target who can be fetch or push with current folder
```
