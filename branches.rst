Using Branches.
---------------

+ Commands.

  - git branch [branche-name]

    It creates a new branch of the project tree,

  - git checkout [branch-name]

    It switches to another branch.

  - HEAD

    Pointer to the current branch being worked on, it  can use git status to view which branch HEAD is
    pionting to.

  - man git-branch

    Local docs for the git branch command.

  - man git-checkout

    Local docs for the git checkout command.

+ Branch, What does it mean?

  We can enter git status to check in what branche we are.

  $ git status
  On branch master
  Your branch is ahead of 'origin/master' by 1 commit.
    (use "git push" to publish your local commits)

  Untracked files:
    (use "git add <file>..." to include in what will be committed)

          tags.rst

  nothing added to commit but untracked files present (use "git add" to track)

  As we can see, we are in master branch. When we make a commit to our master branch, git makes a snap
  shot of our current git database so the next time we make a commit to our branch, git will create
  another snap shot. This means, If we want to go back to a previous condition of our repository then git
  has the information to restore to prior state.

  When our application is not ready to be used (broken stage), we can have a branch or several branches.
  For demo purposes, we will call it "development" and we can merge it to master branch when it is
  complete.

  $ git branch development

  Note: We are not on that branch yet as we see in the following command.

  $ git status
  On branch master
  nothing to commit, working directory clean
  To change to development branch.

  The following command is a precise way of seieng the previous command.

  --oneline flag shows oneline at a time.

  --decorate flag will print out any reference for us.

  $ git log --oneline --decorate
  c49e146 (HEAD -> master, development) Tagging in git...   --> HEAD is pointing to master.
  4a9eeb2 (tag: v0.1, origin/master) Typo...
  f87fc03 Updating Spacing...
  dc48d78 Checking spelling...
  4ec3553 Checking spelling...
  fcc38f7 Updating typos...
  9e53e5d git check-ignore - line...
  a55390f Updating committing and ignoring files...
  2c9b406 Updating and ignoring vim backups...
  06f5852 Git, notes...

  To switch to development branch, we enter the following command.

  $ git checkout development
<<<<<<< HEAD
  Switched to branch 'development'

  $ git status
  On branch development      ---> as we can see, we are in development branch.
  Untracked files:
    (use "git add <file>..." to include in what will be committed)

          branches.rst
          tags.rst

  nothing added to commit but untracked files present (use "git add" to track)

  The message displayed informs us that we need to add the files, as consequence; we need to commit.

+ Conclusion.
  The previous examples show a broad understanding about git branch, as a result; they can assist us to
  expand our horizon.
=======
>>>>>>> development
