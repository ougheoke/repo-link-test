# repo-link-test


# Add a GitHub Repository to your Local Machine 
## Step 1: Create a GitHub Repository
### Navigate to the Repositories Tab
  - Log into your GitHub account
  - On your profile, navigate to the Repositories tab
  - Click on the **New** button
  
  ![new_repo](https://user-images.githubusercontent.com/111533969/217383587-1f24cf7f-08b2-4210-ae81-874415d31461.png)

### Repository Details
  - On this page, type a name for your repository (you can use the suggestion or create your own)
  - You can choose to make it public or private.
  - Adding a `README` file is optional, but highly recommended.
  
  ![repo-test](https://user-images.githubusercontent.com/111533969/218136077-fae1730a-705a-4550-9425-7478727bc6ef.png)

  - Your default branch will be set to `main`
  - Click on **Create repository** to make your repository.
  
  **You're all set to clone your repo to your machine!**
  
 ## Step 2: Clone your repository to your local machine
Cloning via terminal:
- On your GitHub Repo, click the green code button, then copy the .git URL to your clipboard.
![](https://user-images.githubusercontent.com/97190412/217404862-42231c01-029b-4d0b-a8c4-2cccb1cf5d41.png)
  - It should look like this: `https://github.com/username/repo-name.git`

 
- Open your preferred code editor (ex. Visual Studio Code)
  - Then, open a gitbash terminal
 
- Move to the parent directory where you would like to clone your new GitHub repository. **Desktop is a good place to start.**
  - use `cd` to change directory
  - Run `cd Desktop`

- Clone your GitHub repository to your local machine
  - Run `git clone https://github.com/username/repo-name.git`
  - Now, you will find a folder on your desktop named `repo-name`

- Move into this folder:
  - Run `cd repo-name`
- To make changed to the files in this folder/local repo
  - Run `code .` to open the folder

 **Now you can make changes to the files!**
 
## Step 3: Make changes? Lets get that repository updated!:sweat_smile: 
- First, you will need to cd in the correct repository. 
  - For our example you would put `cd OneDrive/desktop/Code/repo-link-test` in your gitbash terminal.
  - It should look like this:
![AAA](https://user-images.githubusercontent.com/111534176/217842187-82e01e80-2acd-432e-9056-f795bdbdcdff.PNG)
- After you are in the right repository, you will begin by checking your status by entering `git status` in your gitbash terminal.
  - The following prompt should follow:
```diff
$ git status
On branch main
Your branch is up to date with 'origin/main'.
Untracked files:
  (use "git add <file>..." to include in what will be committed)
- debug.log
- index.html
nothing added to commit but untracked files present (use "git add" to track)
```
- After you see which files have been changed or updated, we will need to add them to the list that will be pushed back to the repository using `git add *` in your gitbash terminal.
  - An alternative way would be adding each file individual, `git add index.html debug.log` in your gitbash terminal.
- It is a good idea to check status again, `git status` in your gitbash terminal.
  - This will confirm the the changes/updates have been added correctly.
```diff
$ git status
On branch main
Your branch is up to date with 'origin/main'.
Untracked files:
  (use "git add <file>..." to include in what will be committed)
+ new file: debug.log
+ new file: index.html
nothing added to commit but untracked files present (use "git add" to track)
```  
- The next step is commiting the files that you just added, `git commit` in your gitbash terminal.
  - If you would like to add a message about this update you can do `git commit -m 'message here'` in your gitbash terminal.
  - It will show the following:
```
$ git commit -m 'This is a test push'
[main 9ab22ef] This is a test push
 2 files changed, 1 insertion(+)
 create mode 100644 debug.log
 create mode 100644 index.html
 ```
- The final step is pushing all of your new and committed code back to the repository, `git push` in your gitbash terminal.
  - It should show the following:
```
$ git push
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 16 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (4/4), 349 bytes | 349.00 KiB/s, done.
Total 4 (delta 0), reused 0 (delta 0), pack-reused 0
To https://github.com/ougheoke/repo-link-test.git
   2ec005d..9ab22ef  main -> main
```
- Finally, back to the old trusty, `git status` to make sure everything pushed correctly.
  - If you get this message, you are good to go!
```
$ git status
On branch main
Your branch is up to date with 'origin/main'.

nothing to commit, working tree clean
```
