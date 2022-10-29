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


## Branch
- #### `Check all branch List`
    ```bash
    git branch
    ```
- #### `Create New Branch`
    ```bash
    git branch <Your-Branch-Name>
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
