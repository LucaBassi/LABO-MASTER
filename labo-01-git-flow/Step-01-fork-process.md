# Fork process

[Source](https://docs.github.com/en/get-started/quickstart/fork-a-repo)

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Git-flow scenario to master</p></figcaption></figure>

* [x] Fork the "upstream" repository in your github organisation

![image-20230510201926483](C:\Users\Auggus\Documents\CPNV\GitHub Repos\Labo-Master\labo-01-git-flow\assets\image-20230510201926483.png)

* [x] Clone your own repo in your local machine

```
[INPUT]
git clone https://github.com/CPNV-DGS-MON1/Labo-Master.git

[OUTPUT]
Cloning into 'Labo-Master'...
remote: Enumerating objects: 24, done.
remote: Counting objects: 100% (24/24), done.
remote: Compressing objects: 100% (22/22), done.
remote: Total 24 (delta 3), reused 18 (delta 1), pack-reused 0
Receiving objects: 100% (24/24), 6.31 KiB | 1.26 MiB/s, done.
Resolving deltas: 100% (3/3), done.

```

![image-20230510202231934](C:\Users\Auggus\Documents\CPNV\GitHub Repos\Labo-Master\labo-01-git-flow\assets\image-20230510202231934.png)

* [x] Init Git flow (with standard settings)

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
Hooks and filters directory? [C:/Users/Auggus/Documents/CPNV/GitHub Repos/Labo-Master/.git/hooks]
```

![image-20230510202357159](C:\Users\Auggus\Documents\CPNV\GitHub Repos\Labo-Master\labo-01-git-flow\assets\image-20230510202357159.png)

* [ ] Integrate updates from upstream (main) into your repository (develop)

```
[INPUT]
git remote add upstream https://github.com/CPNV-MON1/Labo-Master.git

[OUTPUT]
origin  https://github.com/CPNV-DGS-MON1/Labo-Master.git (fetch)
origin  https://github.com/CPNV-DGS-MON1/Labo-Master.git (push)
upstream        https://github.com/CPNV-MON1/Labo-Master.git (fetch)
upstream        https://github.com/CPNV-MON1/Labo-Master.git (push)
```

![image-20230510202743642](C:\Users\Auggus\Documents\CPNV\GitHub Repos\Labo-Master\labo-01-git-flow\assets\image-20230510202743642.png)

![image-20230510202718447](C:\Users\Auggus\Documents\CPNV\GitHub Repos\Labo-Master\labo-01-git-flow\assets\image-20230510202718447.png)

* [ ] Create a branch feature called "terraformBasicScript"

```
[INPUT]
//TODO

[OUTPUT]
//TODO
```

* [ ] Add this code and commit it (feat:add basic terraform script")

```
terraform {
  required_providers {
    aws = {
      source  = "hashicorp/aws"
      version = "~> 4.16"
    }
  }

  required_version = ">= 1.2.0"
}

provider "aws" {
  region  = "us-west-2"
}

resource "aws_instance" "app_server" {
  ami           = "ami-830c94e3"
  instance_type = "t2.micro"

  tags = {
    Name = "ExampleAppServerInstance"
  }
}
```

```
[INPUT]
//TODO

[OUTPUT]
//TODO
```

* [ ] Finish the feature

```
[INPUT]
//TODO

[OUTPUT]
//TODO
```

* Push this modification on your repository

```
[INPUT]
//TODO

[OUTPUT]
//TODO
```

* What happens to the feature/branch ?

```
//TODO
Add your answer with command line used to validate your analysis.
```

* Open a pull request comparing your develop branch to your main
* Assign the pull request to your partner

```
//TODO
Screenshot pull request on github
```

* Notify him using a issue "Could you please review my pull request ?"

```
//TODO
Screenshot issue on github
```
