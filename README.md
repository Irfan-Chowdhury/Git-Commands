<div align='center'>

# Git-Commands
</div>

## A. General

- #### `Create Git`
    ```bash
    git init
    ```

- #### `Add All Files`
    ```bash
    git add .
    ```

- #### `Commit`
    ```bash
    git commit -m "Your Message"
    ```

- #### `Add & Commit together`
    ``` bash
    git commit -am "Your Message"
    or,
    git commit -a -m "Your Message"
    ```

- #### `Push`
    ```bash
    git push -u origin main
    or,
    git push
    ```

- #### `Clone`
    ```bash
    git clone [url-link.git]
    ```

- #### `Fetch`
    ```bash
    git fetch
    ```

- #### `Pull`
    ```bash
    git pull
    ```

- #### `Check file status`
    ```bash
    git status
    ```

- #### `Check all log`
    ```bash
    git log
    ```

- #### `Merge file`
    ```bash
    git merge <branch-name>
    ```
    <i>This command merges the specified branch’s history into the current branch.</i>
    
- #### `Undo merge before commit & push`
    ```bash
    git merge --abort
    ```
 
- #### `Steps to remove directory from Repository`
    ```bash
    git rm -r --cached YourFolderName
    git commit -m "Removed YourFolderName from repository"
    git push origin main
    ```

    
- #### `Check remote origin`
    ```bash
    git remote -v
    ```

- #### `Change remote origin`
    ```bash
    git remote set-url origin https://github.com/......
    ```

- #### `Add remote url`
    ```bash
    git remote add origin [url-link]
    ```

- #### `To push with new branch`
    ```bash
    git push --set-upstream origin <New-Branch>
    ```

- #### `To Check Remote Origin`
    ```bash
    git remote -v 
    ```

- #### `To change remote origin`
    ```bash
    git remote set-url origin https://github.com/......
    ```
	
- #### `If gitignore not working, then run this command`
    ```bash
    git rm -r --cached directory/sub-directory
    ```
    then use `git add .` , `git commit -m message` & `git push` 
	   
<br>

## B. Branch

- #### `Check all branch List`
    ```bash
    git branch
    ```
- #### `Create New Branch`
    ```bash
    git branch <Your-Branch-Name>
    ```
- #### `Push the new branch in github`
    ```bash
    git push --set-upstream origin <Your-New-Branch-Name>
    ```
- #### `Switch Branch`
    ```bash
    git checkout <Branch-Name>
    ```
- #### `Delete branch locally`
    ```bash
    git branch -d <Branch-Name>
    or,
    git branch -D <Branch-Name>
    ```
    <i>The -d option will delete the branch only if it has already been pushed and merged with the remote branch</i> 
    <br><br>
    <i>
    -D instead if you want to force the branch to be deleted, even if it hasn't been pushed or merged yet.
    </i>


- #### `Delete branch remotely`
    ```bash
    git push origin --delete <Branch-Name>
    ```
    
### Merging branch via command line:
If you do not want to use the merge button or an automatic merge cannot be performed, you can perform a manual merge on the command line. However, the following steps are not applicable if the base branch is protected.
- Step 1: Clone the repository or update your local repository with the latest changes.
```bash
git pull origin develop
```

- Step 2: Switch to the base branch of the pull request.
```bash
git checkout develop
```

- Step 3: Merge the head branch into the base branch.
```bash
git merge tenant-authorization
```

- Step 4: Push the changes.
```bash
git push -u origin develop
```

### Fetch new branch from remote to local machine:
If a team member has created a new branch on the GitHub server and you want to fetch and work with that branch locally, you can follow these steps:

- Step 1: Fetch Branches from the Remote
```bash
git fetch origin
```

- Step 2: List Remote Branches
```bash
git branch -r
```

- Step 3: Check Out the New Branch
```bash
git checkout -b new-branch-name origin/new-branch-name
```
This command will create a new local branch named branch-name that tracks the remote branch of the same name. It also checks out the new branch so you can start working on it.


- Step 4: Push Changes to the Remote (Optional)
```bash
git push origin new-branch-name
```
<br>

## C. Publish your private assignments in your github public repository

- #### `Check Current URL`
    ```bash
    git remote -v
    ```

<i>Then create a new repository. After get new repository link update something in your locale machine which is in private mode. Copy the new url and jus change <b>set-url</b> instead of <b>add</b></i> 

```bash
git remote set-url origin https://github.com/Irfan-Chowdhury/your_new_repository.git
```

```bash
git push
```

<br>

## D. Undo last commit from local and remote 

- #### `Locally`
```bash
git reset --soft HEAD~1
```

- #### `Remotely`
```bash
git push origin +HEAD
```

<br>

## E. Tag
- #### `For Releasing New Version`
```bash
git tag -a v0.1.2 -m "Release v0.1.2"
git push --follow-tags
```

<br>

## F.  Control your specific files/directory to visible/hide in GitHub
- #### `For remove/hide`
```bash
git rm -r --cached app/Http/Controllers
```

- #### `For add/visible`
```bash
git add -f app/Http/Controllers/Landlord
```
- #### `After doing these, please run these commands given below` 
```bash
git commit -m "Control my controller files"
git push origin main
```
<br>

## G. Pushing Issues
If you face authenticate issue during try to push from terminal, first check which remote url exists in your repository. 
- check remote url
```bash
git remote -v
```
- if url start with `https://github.com/` then replace with `git@github.com`. For example, suppose your url is `https://github.com/Irfan-Chowdhury/Git-Commands.git`. Now set with `git@github.com:Irfan-Chowdhury/Git-Commands.git`.
```bash
git remote set-url origin git@github.com:Irfan-Chowdhury/Git-Commands.git
```
Now you can push easily from your terminal.
