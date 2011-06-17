==========
cheatsheet

------------
Global setup

	#. Download and install Git
	#. git config --global user.name "Your Name"
	#. git config --global user.email your_email@foo.com
        
------------------
Set Up a New Repo

	#. mkdir test
	#. cd test
	#. git init
	#. touch README
	#. git add README
	#. git commit -m 'first commit'
	#. git remote add origin git@github.com:$username/test.git
	#. git push -u origin master
      
------------------
Existing Git Repo

	#. cd existing_git_repo
	#. git remote add origin git@github.com:$username/test.git
	#. git push -u origin master

----------------
Clone (Checkout)

	#. git clone git@github.com:$username/repo.git
      
---------------------------
Importing a Subversion Repo

  https://github.com/$username/test/imports/new
