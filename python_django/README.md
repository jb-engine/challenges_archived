Create a backend application allowing management of classrooms and students

Keep track of the time you spend on each part of this project and send it with your submission to [alexandre@jb-engine.com](mailto:alexandre@jb-engine.com).


# Step 1

The first step focuses on Django setup and models.

- Create a Django app and a Postgres database
- Add models to create the following structure:
- Students have a first name and last name, and a student id (20 characters max for each)
- Classrooms have a name (20 char max) and a maximum number of student (any positive integer)
- Each student object must belong to a classroom object


# Step 2

This second step focuses on Django Rest Framework.
- Add Django REST framework library to your project
- Create urls, views, serializers for all your models such as:
- endpoint /students/ will return all students (GET) and allow student creation (POST)
- endpoint /classrooms/ will return all classrooms(GET) and allow classroom creation (POST)


# Step 3

This third step focuses on Nested Routers.
- Add Django Nested Routers library to your project
- Configure your urls, views, and serializers such as:
- endpoint /classrooms/:id/students will return students who belong to classroom :id (GET)
- endpoint /classrooms/:id/ will allow student creation in the classroom :id (POST)


# Guidelines

- Send us the project and your comments as a git patch or repository, or a hosted live demo
