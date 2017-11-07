---
layout: post
title: "How to Work with GitHub and Multiple Accounts"
date:  8/11/17 8:25 AM
tags: 
	-  ssh
	-  git
---
## Create a New SSH Key
```
ssh-keygen -t rsa -C 'pig@pig.com'
```
save file as id_rsa_pig to ~/.ssh/id_rsa_pig
## Attach the new key
copy id_rsa_pig.pub entire string into git hub ->SSH and GPG Keys->New SSH key
then in Terminal run : ssh-add ~/.ssh/id_rsa_pig

## create a config file
```
nano ~/.ssh/config
Host github-pig
  HostName github.com
  User git
  IdentityFile ~/.ssh/id_rsa_pig
  
```
## Try it out
```
mkdir test
cd test
git init
git config user.name "pig"
git config user.email pig@pig.com
```
Login to your company account, create a new repository, give it a name of "test," and then return to the Terminal and push your git repo to GitHub.

```
git add .
git commit -m 'first commit'
git remote add origin git@github-pig:pig/test.git
git push origin master

```
## Don't use git command line and Phpstorm git at same time.


