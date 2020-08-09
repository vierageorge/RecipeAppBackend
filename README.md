# To create this project

1. After creating the Dockerfile, run on terminal: `docker build .`
2. After creatng the docker-compose.yml, run on terminal: `docker-compose build`
3. To create the Django Proyect, run: `docker-compose run app sh -c "django-admin.py startproject app ."`
4. Create a Core App `docker-compose run app sh -c "python manage.py startapp core"` and delete `views.py` and `tests.py`
5. Create a `tests` folder inside core and create `__init__.py` file inside it.