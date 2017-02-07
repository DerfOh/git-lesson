# git-lesson
# git
## A quick rundown

---

## Vocabulary
* Pull
* Staging (adding)
* Commit
* Push
* Working Directory
* Repository (remote & local)
* Branch
* Merge


---

## The workflow
![](http://i.imgur.com/lfWAbTS.png)
---

## Initialize your git repo

* Run `git init` in the directory that you want to track changes in
* You can also do `git clone <<repository.url.git>>` if you already have a remote origin set up
* The following is also provided by GitHub as a framework for setting up a remote origin for your repository

    ```bash
    echo "# git-lesson" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git remote add origin git@github.com:DerfOh/git-lesson.git
    git push -u origin master
    ```

---

## Create your first commit

* Stage your changes

    * `git add .`

* Commit your changes

    * `git commit`

* Write your commit message

---

## Push your commit to the repository
* `git push`
    * Once you have all the changes committed if you're working with a remote origin then you need to push or changes to that origin
    
    * If you're working locally only then there is no need to push

---

## Pulling and cloning

* `git clone <<repository.url.git>>` 
    *  If you already have an existing repository to start with

* `git pull` 

    * Pull from the remote repository after you have cloned it to your local directory

---

## Branching

* `git checkout -b feature` (the "-b" specifies that the branch is to be created")

    * development occurs on the branch then the changes are staged and committed...


---

## Merging
* Once development is completed the user then switches back to master

    * `git checkout master`

* Then the developer merges the master branch with the branch they created

    * `git merge feature`

* Git will automatically attempt to merge the files if there are any conflicts it will prompt the user to fix them
