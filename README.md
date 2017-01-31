# git-lesson

1. Initialize your git repo

    * Run 'git init' in the directory that you want to track changes in
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

2. Create your first commit

    * Create a basic text file called "hello"

        * `touch hello`

    * Stage your changes

        * `git add hello` (you can also do `git add .` to add all items in the directory)

    * Commit your changes

        * `git commit`

        * This will bring up a prompt to enter a message summarizing your commit. The editor that comes up will depend on how your environment is set up.

3. Push your commit to the repo

    * Once you have all the changes committed if you're working with a remote origin then you need to push or changes to that origin
        * `git push`
        
        * If you're working locally only then there is no need to push changes to the remote

4. Pulling and cloning

    * If there has been changes made to the file then you will need to pull them from remote
        
        * `git pull` will bring down the changes and attempt to automatically merge them

    * If you're just starting work on a new project that has already had a repository made you can also clone it
    
        * `git clone <<repository.url.git>>` this will automatically pull the latest version of the application down from the repository and will additionally set the remote upstream

5. Branching and Merging

    * Branches are typically used to allow for simultaneous development and allow for individual features to be worked on and tested without having to affect anyone else working on the project

    * The branch "Master" is typcially reserved for the working releases of the application while other branches (names can be determined by the grou) are used for development and testing

    * When development is finished on a branch it is then "Merged" into the "Master" branch so that there is a single source of the latest working build of the application

    * `git checkout -b feature` (the "-b" specifies that the branch is to be created")

        * development occurs on the branch then the changes are staged and committed...

    * Once development is completed the user then switches back to master

        * `git checkout master`

    * Then the developer merges the master branch with the branch they created

        * `git merge feature`

    * Git will automatically attempt to merge the files if there are any conflicts it will prompt the user to fix them either manually or by using a merge tool
