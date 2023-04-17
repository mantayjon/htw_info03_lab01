#### EURE NAMEN, Tobias Bayer, Jonas Mantay

[our repository](https://github.com/mantayjon/info03_lab01)

# Labreport 01

### Part 2: Set up a central github repo and try out:	

We set up a github repository by clicking 'new repository' on the github website.
Our next step is to read the recommended instructions on the website. To create a new repository on the command line , it tells us to:

1. `echo "# test" >> README.md`
    - writes '# test' into a file. If the file does not exist, it is created first.
2. `git init`
    - git init initialises a git repository. A hidden .git folder is created, which contains information about the repository.
3. `git add README.md`
    - git add file.extension adds a file to the staging area, ready to be commited. We could have written git add . to add all files in the current working     - directory to the commit.
4. `git commit -m "first commit"`
    - git commit -m message creates a commit with a message, e.g "add very important thing"
5. `git branch -M main`
    - git branch -M main is short for git branch -move --force main. This means that a new branch will be created as main no matter what.
6. `git remote add origin https://github.com/abductedRhino/test.git`
    - this adds a repository to pull from and push to. The name is origin.
7. `git push -u origin main`
    - this creates an upstream tracking branch and pushes it.
    
With the suggested steps, we are able to create and push a github repository. We write a list called 'Einkaufsliste' into our `README.md` and collaboratively push items to it. Again, we choose to use the Terminal: 
```bash
mkdir info3
cd info3
git clone https://github.com/mantayjon/info03_lab01.git
cd info03_lab01
```
1. make a new directory named 'info3'
2. change directory to 'info3'
3. copy the git repository from https://github.com/mantayjon/info03_lab01.git
4. change directory to 'info03_lab01'
To push an item to the List in `README.md`, we open the file with any text-editor and append a new list-item in markdown syntax, e.g. `- Salz` and hit save. We then return to our Terminal:
```bash
git add .
git commit -m "add item to list"
git push
```
1. add every new or changed file in current working directory to git staging area. In this case, just `README.md`
2. create a commit with message 'add item to list'
3. push, update the remote commit with the commit we just created.
With the above, we are able to change files collaboratively, but we will create conflicts if someone tries to push a commit to the remote without `git pull`ing before. This is not a great workflow, but there are solutions:
- work on different branches
- work in different files

This report was created in a similar way as the `git init` above. Except we `git clone`, `echo "text" >> file`, `git add file`, `git commit -m "message"`, `git push`.
![screenshot](https://github.com/mantayjon/info03_lab01/blob/main/pics/screenshot_from_2023-04-16_19-42-12.png)
This copies the remote repo, makes a file with a line of text, adds it to the staging area, creates a commit with a message and updates the remote with the local commit.

* sharing files and changes
* different workflows (see git slides)
* resolving merge conflicts
* rebasing, merging, fast-forwarding

