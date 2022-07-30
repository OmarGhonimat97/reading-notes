# Readings: Django Custom User

## Django Custom User Model

> Setup

To start, create a new Django project from the command line. We need to do several things:

- create and navigate into a dedicated directory called accounts for our code
- install Django
- make a new Django project called django_project
- make a new app accounts
- start the local web server

> AbstractUser vs AbstractBaseUser

There are two modern ways to create a custom user model in Django: ***AbstractUser*** and ***AbstractBaseUser***. 
In both cases we can subclass them to extend existing functionality however ***AbstractBaseUser*** requires much, much more work.

> Custom User Model

Creating our initial custom user model requires four steps:

- update django_project/settings.py
- create a new CustomUser model
- create new UserCreation and UserChangeForm
- update the admin

> Superuser

It's helpful to create a superuser that we can use to log in to the admin and test out log in/log out. On the command line type the following command and go through the prompts.

> Templates/Views/URLs

Our goal is a homepage with links to log in, log out, and sign up. Start by updating settings.py to use a project-level templates directory.

## DjangoX

DjangoX can be installed via Pip, Pipenv, or Docker.
To start, clone the repo to your local computer and change into the proper directory.

```commandline
$ git clone https://github.com/wsvincent/djangox.git
$ cd djangox
```

> Pip

```commandline
$ python -m venv .venv

# Windows
$ Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
$ .venv\Scripts\Activate.ps1

# macOS
$ source djangox/bin/activate

(.venv) $ pip install -r requirements.txt
(.venv) $ python manage.py migrate
(.venv) $ python manage.py createsuperuser
(.venv) $ python manage.py runserver
# Load the site at http://127.0.0.1:8000
```

