# Fork process

[Source](https://docs.github.com/en/get-started/quickstart/fork-a-repo)

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>Git-flow scenario to master</p></figcaption></figure>

* [x] Fork the "upstream" repository in your github organisation

  [TO DO]

  Depuis la page du repository, cliquer sur Fork 

![image-20230510203158639](C:\Users\Janbl\AppData\Roaming\Typora\typora-user-images\image-20230510203158639.png)

* [x] Clone your own repo in your local machine

```
[INPUT]
git clone https://github.com/JanBlatterCPNV/MON1-Labo-Master

```

[OUTPUT]

![image-20230510203003173](C:\Users\Janbl\AppData\Roaming\Typora\typora-user-images\image-20230510203003173.png)

* [x] Init Git flow (with standard settings)

```
[INPUT]
git flow init
```

[OUTPUT]

![image-20230510202730745](C:\Users\Janbl\AppData\Roaming\Typora\typora-user-images\image-20230510202730745.png)

- [ ] Integrate updates from upstream (main) into your repository (develop)

```
[INPUT]
git switch main //se mettre dans la branche "main"
git merge develop // update la branche develop depuis la branche main
```

[OUTPUT]
//TODO

![image-20230510210042737](C:\Users\Janbl\AppData\Roaming\Typora\typora-user-images\image-20230510210042737.png)

* [ ] Create a branch feature called "terraformBasicScript"

```
[INPUT]
git flow feature start "terraformBasicScript"
```

[OUTPUT]
//TODO

![image-20230510213746080](C:\Users\Janbl\AppData\Roaming\Typora\typora-user-images\image-20230510213746080.png)

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
git add . 
git commit -m "add basic terraform script"
```

//TODO

![image-20230510214621437](C:\Users\Janbl\AppData\Roaming\Typora\typora-user-images\image-20230510214621437.png)

* [x] Finish the feature

```
[INPUT]
git flow feature finish terraformBasicScript

```

[OUTPUT]
//TODO

![image-20230510214845979](C:\Users\Janbl\AppData\Roaming\Typora\typora-user-images\image-20230510214845979.png)

* Push this modification on your repository

```
[INPUT]
git push --set-upstream origin develop // push la modification depuis la branche "develop" dans le repository
```

[OUTPUT]
//TODO![image-20230510215231561](C:\Users\Janbl\AppData\Roaming\Typora\typora-user-images\image-20230510215231561.png)

* What happens to the feature/branch ?

```
//TODO
Le feature a disparu suite à sa fermeture 
 
$ git flow feature finish terraformBasicScript
Switched to branch 'develop'
Updating 3192b2b..d6b4c15
Fast-forward
 labo-01-git-flow/terraformScript.py | 23 +++++++++++++++++++++++
 1 file changed, 23 insertions(+)
 create mode 100644 labo-01-git-flow/terraformScript.py
Deleted branch feature/terraformBasicScript (was d6b4c15).

Summary of actions:
- The feature branch 'feature/terraformBasicScript' was merged into 'develop'
- Feature branch 'feature/terraformBasicScript' has been locally deleted
- You are now on branch 'develop'

```

* Open a pull request comparing your develop branch to your main
* Assign the pull request to your partner

```
//TODO
Screenshot pull request on github
```

![image-20230510220430838](C:\Users\Janbl\AppData\Roaming\Typora\typora-user-images\image-20230510220430838.png)

* Notify him using a issue "Could you please review my pull request ?"

```
//TODO
Screenshot issue on github
```

![image-20230510221441098](C:\Users\Janbl\AppData\Roaming\Typora\typora-user-images\image-20230510221441098.png)
