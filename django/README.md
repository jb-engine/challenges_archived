# Introduction:

This is a challenge project from Manatal back end team to evaluate how good you are with building APIs with Django.

## We look for:

- Readability: You can write clear code that any devs could read and understand in one go (Think comments, convention, etc.)
- Simplicity: You can write gimmick-free and straightforward code with no ambiguities
- Defensiveness: You can cover edge cases and treat user inputs with care

## Ground Rules

- We prefer well-thought-out solutions over the quick-and-dirty kind. So take your time, if you need it.
- We accept only completed test covering all the requirements (and recommendations).
- Submission is done via email (send the link to your repo).

## Guidelines

- Send us the project and your comments as a git repository to [yassine.belmamoun@manatal.com](mailto:yassine.belmamoun@manatal.com).
- Keep track of the time you spend on each part of this project and add a reference to it in your `README.md`.


# Django Test

You will build a simple API using Django Rest Framework backend application allowing management of schools.


## Step 1

The first step focuses on Django setup and models.

1. Create a Django app, with:
     - Postgres as a database
     - Pipenv as a Python dependency manager.
     - Environment file (for sensitive information, etc.)

2. Add models to create the following structure:
     - Students have a first name, a last name, and a student identification string (20 characters max for each)
     - Schools have a name (20 char max) and a maximum number of student (any positive integer)
     - Each student object must belong to a school object


## Step 2

This second step focuses on Django Rest Framework (DRF).

Feel free to cover edge cases. (Add a reference to it in your README.md)
We encourage you to use `ModelViewSet` and `ModelSerializer` classes to automatically handle the different API HTTP methods.

1. Add __Django REST framework__ library to your project by using Pipenv

2. Enable and use the DRF browsable API for testing things manually.

3. Design your API according to specifications below (make sure to test and customize your solution) by creating urls, views, serializers, tests for all your models so that:
     - Endpoint `students/` will return all students (GET) and allow student creation (POST)
     - Endpoint `/schools/` will return all schools (GET) and allow school creation (POST)
     - Endpoint `/schools/:id` and `/students/:id` will return the object by :id (GET) and allow editing (PUT/PATCH) or deleting (DELETE)
     - Student creation will generate a unique identification string (like random hexadecimal or uuid4 or anything of your choice)
     - Trying to add a student in a full school (maximum number of student reached) will return a DRF error message

#### References:
- ModelViewSet: https://www.django-rest-framework.org/api-guide/viewsets/#modelviewset
- ModelSerializer: https://www.django-rest-framework.org/api-guide/serializers/#modelserializer


## Step 3

This third step focuses on __Django Nested Routers__.

1. Add Django Nested Routers library to your project by using Pipenv

2. Design your API according to specifications below:
     - Endpoint /schools/:id/students will return students who belong to school :id (GET)
     - Endpoint /schools/:id/students will allow student creation in the school :id (POST)
     - Your nested endpoint will allow GET/PUT/PATCH/DELETE methods on /schools/:id/students/:id
     - Your nested endpoint will respect the same two last rules of Step 2 too

#### References:
- drf-nested-routers: https://github.com/alanjds/drf-nested-routers


## Bonus

- You can host your solution in Heroku (or other).
- You can add fields of your choice to students and schools such as location, nationality, age, etc. You can use Python Faker library to generate random data (names, etc) to populate fields.
- You can add search filters to your endpoints such as /students/?search=jeremy and you can add ordering filters as well, for example by age, by nationality, etc.
- You can add pagination or anything else that you wanna show us, feel free to add interesting stuff to this project!


