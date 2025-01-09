# GitHub step by step guide for ubuntu system

## Step 1
- Open ubuntu terminal
- Update systems with latest packages

```
sudo apt-get update
```

- Install git in Ubuntu (if not installed)
- It will ask for password we can use system password 
```
sudo apt-get install git-core
```

- Check the git version

```
git --version
```
## Step 2

- Now set the config file 
```
git config --global user.name "user_name"
git config --global user.email "user_email"
```

- Using this command we can see all config settings we have created for git

```
git config --list
```
## Step 3

- Create folder in system which contain all files of our project
```
mkdir firstGitRepo
```
- Now goto that folder location and create files inside that folder

```
cd firstGitRepo
touch index.html
```

- Open file from terminal using below command, make change on that file and save it 

```
gedit index.html
```
- We can view file content in terminal
```
cat index.html
```

## Step 4

- Now we have to initialize empty repository in that folder 

```
git init
```

- Now add all files 
```
git add .
```
- We can use below command anytime to check status of files
```
git status
```
- Now commit the changes to clean work tree
```
git commit -m 'commit_message'
```
- we can select the branch where we want to push the code
```
git branch -M main
```

- we can also switch the branch using below command 
```
git checkout branch_name
```

- Now we have to push code from local to github
```
git push origin branch_name
```

#### It will ask for username and password after giving username and password if it return error the follow this steps
- Open Github 
- Click on profile > settings
- Now in settings page sidebar we can see last options "Developer Settings"
- At Left sidebar we can see menu "Personal Access Token" click on that and select "Tokens(Classic)"
- Generate new Token and set the duration as per requirement
- copy and Save that toke
- Now follow the below syntax 
```
git remote set-url origin https://<token>@github.com/<username>/<repo>
```
- After that we can push code
```
git push origin branch_name
```
- To pull code from repo to local we use git pull
```
git pull origin branch_name
```
