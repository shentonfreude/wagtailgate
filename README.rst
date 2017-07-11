========
 README
========

Trying out Wagtail CMS, following the tutorial at
http://docs.wagtail.io/en/v1.11.1/getting_started/tutorial.html

Install, Run
============

Install the virtualenv then packages::

  virtualenv -ppython3 .venv3
  source .venv3/bin/activate
  pip install wagtail
  cd mysite/
  pip install -r requirements.txt

Create the database and superuser, standard Django stuff::

  python manage.py migrate
  python manage.py createsuperuser

Development
===========

As you add models, you'll need to migrate the database schema then
restart the server; I do this::

  ./manage.py makemigrations && ./manage.py migrate && ./manage.py runserver

