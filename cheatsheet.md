cheatsheet

code4lib Git workshop 08/04/2016

global setup

  ```
  $ git config --global user.name "Your Name"
  $ git config --global user.email your_email@foo.com
  ```
        
set up a new repo

  ```
  $ mkdir test
  $ cd test
  $ git init
  $ touch README
  $ git add README
  $ git commit -m 'first commit'
  $ git remote add origin git@github.com:$username/test.git
  $ git push -u origin master
  ```
      
updating an existing git repo

  ```
  $ cd existing_git_repo
  $ git remote add origin git@github.com:$username/test.git
  $ git push -u origin master
  ```

clone/checkout

  ```
  $ git clone git@github.com:$username/repo.git
  ```

importing a subversion repo

* https://github.com/$username/test/imports/new

working in a feature branch

  ```
  $ git checkout -b feature_name
  // do stuff
  $ git commit -m 'first commit'
  // do more stuff
  $ git commit -m 'second commit'
  // fix one last typo
  $ git commit -m 'fixing one last thing'
  $ git rebase -i master
  ```

* you'll see a list of the commits:

  ```
  pick fba4829 first commit
  pick 9e04b6a second commit
  pick 16ee6e0 fixing one last thing
  ```

* to squash those down to a single commit, edit that to:

  ```
  pick fba4829 first commit
  squash 9e04b6a second commit
  squash 16ee6e0 fixing one last thing
  ```

* close your editor, and you'll be presented with a new file listing all of
the commit messages from the commits, which you can edit down to a nice
summary.  close that file, and your commits will now be combined into a
single commit, ready to open a PR.

pulling changes from a fork (e.g., reviewing a PR):

  ```
  git checkout -b my_local_branch master
  git pull https://github.com/$user/$repo.git $remote_branch_name
  ```

undoing the last commit (before it's pushed to github):

  ```
  git reset --soft HEAD~1
  ```
