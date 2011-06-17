cheatsheet
----------

Global setup:

 Download and install Git
  git config --global user.name "Your Name"
  git config --global user.email your_email@foo.com
        

Next steps:

  mkdir test
  cd test
  git init
  touch README
  git add README
  git commit -m 'first commit'
  git remote add origin git@github.com:$username/test.git
  git push -u origin master
      

Existing Git Repo?

  cd existing_git_repo
  git remote add origin git@github.com:$username/test.git
  git push -u origin master
      

Importing a Subversion Repo?

  https://github.com/$username/test/imports/new
