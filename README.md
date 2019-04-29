# Git-Session 

A Free Open Source DVCS ”distributed version control system ” 

# How it Works!

- #### Snapshots, Not Differences
  - Compares SHA1 sum of modified files.
  - Saves the new file as a Whole "easier to retrive lost data"
  - Each Snapshot contains references to the files "to save space uses ref. only"
- #### Stores new versions of files only
- #### Each snapshot contains each file
- #### Everything is local “distributed”
    - Each Computer has all the history of the project
    - Makes it faster and easeir to contribute 
    - Safer beacuase the data are not onlt on one repo
- #### Git has Integrity
    - Everything in Git is CHECKSUMMED "fast ,reliable"
    - Uses SHA-1 hash "a 40 hexadecimal char string"
    - Easy to recognize corrupted files.
- #### Git Generally Only Adds Data "Everything is almost reversible"



## Files’ Three States
- Modified
- Staged
- Committed

## Installtion
```sh
$ sudo apt update
$ sudo apt intsall git
```

## First Time Configurations 
```sh
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
git config --global core.editor nano
git config --global merge.tool meld 
```

## Git Help
git has a really good command manual for each command
```sh
$ git help <command>
$ man git <command>
$ git <command> -h #summarized
```
## Important Terms
- Repository
- Index “Staging area”
- working tree “Project tree”
- Commit
- Branch
- Tag
- Master
- Head
# Git Basics
- #### Git Repository
```sh
$ git init # Intialize a Embty/new repository
$ git clone <URL># to Clone/Copy exsiting repository
```
 `<URL>`: can be git, shh, http, https, file , etc 
- ## Recording Changes to the Repository ![N|Solid](./pasted%20image%200.png)
    - #### Checking status of your files
        ```sh
        $ git status`
        $ git status -s # Summarized
        ```
        - `??`    “ untraked ”
        - A     “ staged ”
        - M     “ Modified staged “ 
        - `M`    “ Modified untracked “
        Example: 
        ```sh
        $ git status
        $ echo 'I' > README #creates a new file
        $ git status
        ```
    - #### Staging Modified Files
        Stage your files after adding not before
        ``` sh
        $ git add <files|WildCards> 
        ```
        Example:
        ```sh
        $ git add README
        $ git status
        $ echo “USE” >> README
        $ git status
        $ git add README
        $ git status
        ```
    - #### Ignoring Files
        A file listing patterns to match them with files in your repositories.
        File name “.gitignore”
        - .gitignore [`common templates`](https://github.com/github/gitignore)
        - See `man gitignore` for more information
    - #### Viewing staged and unstaged
        ``` sh
        $ git status
        $ git diff
        $ git diff --staged
        ```

    
