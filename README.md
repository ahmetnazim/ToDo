# Create To Do Lists

Listing some planned actions application source code


Steps

# 1 Setting up project

	Initialize the git

		git config --global user.email "your@email.com"
		git config --global user.name "Your Name"
		git init 

	create README.md file
		md stands for markdown and the latest industry standart to write documentation in git project

	create .gitignore
		# Created by https://www.gitignore.io/api/python,vagrant
		# Edit at https://www.gitignore.io/?templates=python,vagrant
	
	create the LICENCE file
		https://choosealicense.com/licenses/mit/

	Add new files to git repo
		git add .
			Adds or removes all green files to project

		git commit -am "Initial commit"
			-a is all -m message
			Describe the changes to project since the last commit

	Pushing to github
        git branch -M main
        git push -u origin main

# 2 Create Python Virtual Environment

    python -m venv env

    Activate the virtual environment
		source env/bin/activate

    For deactivate
		deactivate
# 3 Install required Python packages

	Create requirements.txt in the project folder

	List the pakages and specific versions
		If you do not write the version it installs th elatest version and it might be crash your project.
		You can check the latest versions from https://pypi.org/
	
	Install requirements in the activated environment from vagrant folder in development server 
		pip install -r requirements.txt
			-r stands for requirements

# 4 Create new django project and app

	In the activated environment from vagrant folder in development server 

	Project:
		django-admin.py startproject todo_project .

	API:
		python manage.py startapp todo_api
			django can manage more api for your project

# 5 Enable your app in the django settings file

	in todo_project > setting.py 

		in INSTALLED_APPS = [

			add

				'todo_api',

# 6 Test and commit your changes

	Django has its own development server. To activate it

		python manage.py runserver 0.0.0.0:8000
			0.0.0.0 means make available all network adapters on development server
			8000 port comes from our vagrant settings

	Open the browser 127.0.0.1:8000
		127.0.0.1 is the localhost

		you can stop the server with Cntrl + C

	 
 
