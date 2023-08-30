<div align='center'>

# Git-Commands
</div>

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
	   

## Branch

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

## Publish your private assignments in your github public repository

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

## Undo last commit from local and remote 

- #### `Locally`
```bash
git reset --soft HEAD~1
```

- #### `Remotely`
```bash
git push origin +HEAD
```

## Tag
- #### `For Releasing New Version`
```bash
git tag -a v0.1.2 -m "Release v0.1.2"
git push --follow-tags
```

## Control your specific files/directory to visible/hide in GitHub
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


