# Fork process

[Source](https://docs.github.com/en/get-started/quickstart/fork-a-repo)

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Git-flow scenario to master</p></figcaption></figure>

* [ ] Fork the "upstream" repository in your github organisation

```
//TODO
Screenshot of Github
```
![](images/Capture%20d%E2%80%99%C3%A9cran%20du%202023-05-09%2011-09-06.png)


* [ ] Clone "teacher" repo in your local machine

```
[INPUT]
git clone git@github.com:LucaBassi/Labo-Master.git

[OUTPUT]
$ ls 
$ LABO-MASTER
```

* [ ] Init Git flow (with standard settings)

```
[INPUT]
git-flow init

[OUTPUT]
$ git branch 
* develop
  main

```

* [ ] Integrate updates from upstream (main) into your repository (develop)

```
[INPUT]
git checkout develop
git pull origin main

[OUTPUT]
 * branch            main       -> FETCH_HEAD
Updating 65402b5..35e8589
Fast-forward
 labo-01-git-flow/ReadMe.md | 2 ++
 1 file changed, 2 insertions(+)
 create mode 100644 labo-01-git-flow/ReadMe.md

```

* [ ] Create a branch feature called "terraformBasicScript"

```
[INPUT]
git checkout -b terraformBasicScript

[OUTPUT]
git branch
  develop
  main
* terraformBasicScript

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
