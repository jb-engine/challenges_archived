Create a backend application allowing management of classrooms and students

Keep track of the time you spend on each part of this project and send it with your submission to [alexandre@jb-engine.com](mailto:alexandre@jb-engine.com).


# Step 1

The first step focuses on Django setup and models.

- Create a Django app, with Postgres as a database, and Pipenv as a Python dependency manager

- Add models to create the following structure:

  - Students have a first name and last name, and a student id (20 characters max for each)
  - Classrooms have a name (20 char max) and a maximum number of student (any positive integer)
  - Each student object must belong to a classroom object


# Step 2

This second step focuses on Django Rest Framework (DRF).

- Add Django REST framework library to your project by using Pipenv

- Create urls, views, serializers for all your models such as:

  - endpoint /students/ will return all students (GET) and allow student creation (POST)
  - endpoint /classrooms/ will return all classrooms(GET) and allow classroom creation (POST)
  - endpoint /classrooms/:id and /students/:id will return the object by :id (GET) and allow editing (PUT/PATCH) or deleting (DELETE)
  - student creation generate random student id (you can choose the method of your choice)
  - trying to adding a student in a full classroom (maximum number of student reached) will return a DRF error message


# Step 3

This third step focuses on Django Nested Routers.

- Add Django Nested Routers library to your project by using Pipenv
- Configure your urls, views, and serializers such as:
  - endpoint /classrooms/:id/students will return students who belong to classroom :id (GET)
  - endpoint /classrooms/:id/ will allow student creation in the classroom :id (POST)
  - make sure your nested endpoint respects the same two rules as Step 2 and allow PUT/PATCH/DELETE methods too

# Guidelines

- Send us the project and your comments as a git patch or repository, or a hosted live demo
