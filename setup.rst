Make sure python is installed
==========================
	which python
You will get the location of where python is installed (i.e /usr/bin/python) if not
--------------------------
	sudo apt-get install python
	sudo apt-get install python-dev

Make sure pip is installed
==========================
	pip
you will get a usage statement if it is. if not
--------------------------
	sudo apt-get install python-pip

Install virtualenv
==========================
	sudo pip install virtualenv
This will install the virtualenv python package to your /usr/local/bin

Install virtualenvwrapper
==========================
	sudo pip install virtualenv
This will install the virtualenvwrapper python package to your /usr/local/bin

If you don't already have an Envs/ dir on you home~
--------------------------
	export WORKON_HOME=~/Envs
	mkdir -p $WORKON_HOME

You will want to add the following to your ~/.bashrc
--------------------------
	export WORKON_HOME=~/Envs
	source /usr/local/bin/virtualenvwrapper.sh

for a list of virtualenvwrapper commands: http://virtualenvwrapper.readthedocs.org/en/latest/command_ref.html

If you will be using PostgreSQL You need to install postgresql-server-dev-X.Y for building a server-side extension or libpq-dev for building a client-side application
==========================
	apt-get install postgresql-server-dev-9.1
	apt-get install libpq-dev
	apt-get install postgresql-client
	apt-get install postgresql-contrib

If you will be using Postgis you will need to install postgis and set a template on Postgres for it:
==========================
	apt-get install postgresql-9.1-postgis

You will then need to create a spatial database template
--------------------------
	https://docs.djangoproject.com/en/1.4/ref/contrib/gis/install/#spatialdb-template

you will also need the psycopg2 python module that django makes heavy use of
==========================
	apt-get install python-psycopg2
OR
	pip install psycopg2

cd in to project directory (cd ~/projects/mysite/) and create a virtual environment for our project
==========================
	mkvirtualenv my_env

Activate the environment
==========================
	workon my_env

you should see "(my_env)" at the start of the shell promp to indicate the env you are using. 
Anything installed from this point will be installed in this env and not globally, (so no need for sudo)

Install django in the env
==========================
	pip install django

To see a list of packages that have been installed on the virtual env
==========================
	lssitepackages

Start a new django project
==========================
	django-admin.py startproject mysite

Run the python server
==========================
	python manage.py runserver
By defualt this will create the server on localhost port 8000 (http://127.0.0.1:8000/) you can specify which port to run the server on by running:
--------------------------
	python manage.py runserver 127.0.0.1:8001

Read follow the djnago tutorials
==========================
https://docs.djangoproject.com/en/1.4/intro/tutorial01/







