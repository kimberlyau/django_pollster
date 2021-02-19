# Once python is installed
> pip install pipenv
* creates virtual environment to install packages
* also creates Pipfile which shows what packages that are 
* installed; will use SQLite included

> pipenv shell 
> django-admin startproject pollster

## Note
* Project (overall application); multiple apps within project
* Pollster application with polls app and pages app (static pages)

## Files
* manage.py:   the command line tool we'll be using
* settings.py: information about database and other settings
* url.py:      routing; each app will have its own
* wsgi.py:     serving the app; will not need to touch


> python manage.py runserver 8081 // port number

# Our first app
> python manage.py startapp polls 
* admin.py: admin area
* apps.py: will have polls configs
* models.py: questions models and choices model
* views.py: render template

## Adding the models
1. models.py
2. Add PollsConfig to settings.py
3. Create migration to make database table
    > python manage.py makemigrations polls
    * Creates 0001_initial.py that will tell tables what to do
    > python manage.py migrate

