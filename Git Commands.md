1. **git init** → Initializes a new Git repository in the current directory.
2. **git add .** → Stages all changes (new, modified, or deleted files) for the next commit.
3. **git branch -m main** → Renames the current branch to "main."
4. **git remote add origin \[https://github.com/user/user-repo.git]** → Links the local repository to a remote repository at the specified URL.
5. **git remote -v** → Displays the remote repositories linked to the local repo with their fetch and push URLs.
6. **git push -u origin main** → Pushes the main branch to the remote "origin" and sets it as the default upstream branch for future pushes.
#### git branching

- **git branch \[name]** → Creates a new branch with the specified name.
- **git branch** → Lists all branches in the repository, highlighting the current branch.
- **git checkout \[branch_name]** → Switches to the specified branch.
- **git branch -d \[branch_name]** → Deletes the specified branch (if fully merged).
- **git checkout -b \[branch_name]** → Creates a new branch with the specified name and switches to it.

## Steps for Open Source Collaboration
### 1. Fork the Repository
- Go to the GitHub repository.
- Fork the repository.
- Create your forked repository.
- Copy the main branch only.
- Hit the **Create Fork** button.
- Done~

### 2. Clone the Forked Repo
- Go to the repository you forked.
- Copy the **git_link**.
- Clone the repository to your local folder using `git clone <git_link>`.

### 3. Create a New Branch
- `git branch` → _See all branches in your current repo._
- `git branch [branch_name]` → _Create a new branch in your repo._
- `git checkout [branch_name]` → _Switch to another branch._
- `git checkout -b [branch_name]` → _Create a new branch and switch to it._
- `git branch -d [branch_name]` → _Delete a branch._

### 4. Make a Pull Request
- Make changes in your branch.
- Stage and commit changes:

```bash
git add .  
git commit -m "Your changes description"
```  

- Push your branch to your forked repo:    
```bash
git push origin [branch_name]
```
  
- Go to the original repository on GitHub.
- Click **Compare & Pull Request**.
- Write a brief description of your changes and submit the pull request.
- Done! 🎉

-----------

## Random Commands

1. **git log** → Displays the commit history with details like author, date, and commit message.
2. **git log --oneline** → Shows the commit history in a condensed, single-line format per commit.
3. **git reset \[commit_id] --hard** → Resets the repository to the specified commit, discarding all changes after it.
4. **git push -f** → Force-pushes changes to the remote repository, overwriting the existing history.
5. **git revert \[commit_id]** → Creates a new commit that undoes the changes introduced by the specified commit.

