Homework #7
Introduction
In this homework assignment, we will continue working with the homework from the previous module. In this assignment, we will use the PostgreSQL database. In the command line, run a Docker container:

bash
Copy code
docker run --name some-postgres -p 5432:5432 -e POSTGRES_PASSWORD=mysecretpassword -d postgres
Instead of some-postgres, choose a container name, and instead of mysecretpassword, come up with a password to connect to the database.

If you agree with your mentor and technically cannot use PostgreSQL, you may replace it with SQLite.

Steps to complete the homework:
Step One
Implement your SQLAlchemy models for tables:

Students table;
Groups table;
Lecturers table;
Subjects table with an indication of the lecturer teaching the subject;
A table where each student has grades from subjects with an indication of when the grade was received;
Step Two
Use Alembic to create migrations in the database.

Step Three
Write a script seed.py and fill the resulting database with random data (~30-50 students, 3 groups, 5-8 subjects, 3-5 lecturers, up to 20 grades for each student in all subjects). Use the Faker package for filling. During the filling, use the SQLAlchemy session mechanism.

Step Four
Make the following selections from the database:

Find 5 students with the highest average grade from all subjects.
Find the student with the highest average grade from a specific subject.
Find the average score in groups for a specific subject.
Find the average score in a group (across the entire grades table).
Find the subjects taught by a specific lecturer.
Find the list of students in a specific group.
Find the grades of students in a specific group from a given subject.
Find the average grade given by a specific lecturer from his subjects.
Find the list of subjects passed by a given student.
Find the list of courses taught by a specific lecturer to a specific student.
For queries, create a separate file my_select.py, which will contain 10 functions from select_1 to select_10. The functions should return the same result as in the previous homework assignment. While creating queries, use the SQLAlchemy session mechanism.
