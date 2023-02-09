# repo-link-test

# Header
## step 1: omonegho 
  create repo on github
  - Log into your GitHub account
  * On your profile, navigate to the Repositories tab
  + Click on the New button
  
  ![new_repo](https://user-images.githubusercontent.com/111533969/217383587-1f24cf7f-08b2-4210-ae81-874415d31461.png)

  
 ## step2: lauren 
 link the repo to your local pc
 
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
