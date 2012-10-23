Prints the CREATE TABLE SQL statements for the given app name
	python manage.py sql [APP_NAME]

====================
Outputs the CREATE INDEX statements for this given app name
	python manage.py sqlindexes [APP_NAME]

=====================
Combination of the sql, sqlindex and sqlcustom commands for the given app name
	python manage.py sqlall [APP_NAME]

=====================
Prints the DROP TABLE SQL statements for the given app name
	python manage.py sqlclear [APP_NAME]

=====================
Checks for any errors in the construction of your models. Validates all models installed.
	python manage.py validate

=====================
Sync the db by running the sql from sqlall for all aps in INSTALLED_APPS.
	python manage.py syncdb


http shortcuts:
https://docs.djangoproject.com/en/dev/topics/http/shortcuts/
