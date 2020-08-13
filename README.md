# To create this project

1. After creating the Dockerfile, run on terminal: `docker build .`
2. After creatng the docker-compose.yml, run on terminal: `docker-compose build`
3. To create the Django Proyect, run: `docker-compose run app sh -c "django-admin.py startproject app ."`
4. Create a Core App `docker-compose run app sh -c "python manage.py startapp core"` and delete `views.py` and `tests.py`
5. Create a `tests` folder inside core and create `__init__.py` file inside it.
6. Run Migrations for the core app `docker-compose run app sh -c "python manage.py makemigrations core"`
7. Create `core/management/commands/wait_for_db.py` file (with directories and `__init__.py` files)
8. Create a superuser `docker-compose run app sh -c "python manage.py createsuperuser"`
9. Start the app with `docker-compose up`
10. Create a new app for users `docker-compose run --rm app sh -c "python manage.py startapp user"`
11. Inside user app directory, remove: migrations, admin, model and tests because those are covered on the core app.
12. Create tests folder inside user app directory.
13. Create `serializers.py` file inside `user` directory.
14. Create recipe app `docker-compose run --rm app sh -c "python manage.py startapp recipe"`
15. Clean up recipe directory by deleting migrations directory and admin, models, tests files and create tests directory.
16. Add recipe app to the app settings INSTALLED APPS.