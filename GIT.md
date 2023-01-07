# Installation on Windows 

![GIT](https://user-images.githubusercontent.com/111989928/209775863-c6760874-790b-4d20-8e13-6edc466a7ae6.png)



1. Download Link - https://git-scm.com/download/win (Step by step video - **[Video](https://www.simplilearn.com/tutorials/git-tutorial/git-installation-on-windows)**)



## Commands for setup

Check Version
```sh
git --version
```
Create folder
```sh
mkdir Test
```
Enter folder
```sh
cd Test
```
Git initialization
```sh
git init
```
Check status (Refresh)
```sh
git status
```
Create text file
```sh
touch file.txt
```
Check status (Refresh)
```sh
git status
```
Add file for commit stage
```sh
git add file.txt
```
If files more than 2 or more
```sh
git add .
```
Commit files anbd update details / reason for changes in files
```sh
git commit -m "new"
```
Link with GitHub
```sh
git config --global user.email raam043@icloud.com
```
```sh
git config --global user.username Raam0433
```
```sh
git commit -m "new"
```


## Create Repository on `GitHub`
Change the branch from Master to Main
```sh
git branch -M main
```
Linking with Repository
```sh
git remote add origin https://github.com/Raam0433/Test.git
```
Push the files/code
```sh
git push -u origin main
```

![GIT](https://user-images.githubusercontent.com/111989928/210564648-0a5fee31-b950-4093-b00b-b9bdd19d1297.png)


![GIT2](https://user-images.githubusercontent.com/111989928/210564749-bccf1e5a-c682-4eb8-b39d-84e1c9a678c0.png)


