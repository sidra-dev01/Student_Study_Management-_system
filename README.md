STUDENT STUDY MANAGEMENT SYSTEM


Database Management System Project


Submitted By:

Sidra khalid


Course:

Database Management System (DBMS)


Project Type:

Database Project


Technology Use:

 phpMyAdmin


Project Components:

ERD • Database Tables • SQL Queries









1. Introduction
The Student Study Management System is a simple database project designed to manage basic information about students, teachers, and subjects. It helps us understand how tables, relationships, keys, and SQL queries work in a database.
2. Purpose of the Project
The purpose of this project is to create a simple database for managing students, teachers, and subjects. The project will also help us understand ERD, primary keys, foreign keys, relationships, and cardinality.
3. Main Components
Our database will initially contain three main entities:
Student 
Teacher 
Subject 
4. Entities and Attributes
Our database contains three main entities: Student, Teacher, and Subject. Each entity has different attributes that store the required information.
1 Student Entity
The Student entity stores the basic information of students.
Attributes:
Student ID
Student Name
Age
Semester
2 Teacher Entity
The Teacher entity stores the basic information of teachers.
Attributes:
Teacher ID
Teacher Name
Specialization 
3 Subject Entity
The Subject entity stores information about the subjects taught in the system.
Attributes:
Subject ID
Subject Name
Credit Hours
4. Objectives of the Project
The main objectives of this project are:
To store basic information about students, teachers, and subjects.
To understand the basic structure of a database.
To learn how different tables are connected with each other.
To understand primary keys, foreign keys, and relationships.
To practice basic SQL queries.
To create and manage a simple database using phpMyAdmin.
5. Scope of the Project
This project will manage basic information related to students, teachers, and subjects. It will show how data can be stored in different tables and how these tables can be connected through relationships. The project will also provide basic SQL operations for managing the stored data.
6. Tools and Technologies
The following tools and technologies will be used in this project:
MySQL — for storing and managing the database.
phpMyAdmin — for creating and managing database tables.
SQL — for performing database operations.
ERD Tool — for designing the Entity Relationship Diagram.
GitHub — for storing and presenting the completed project.



ERD Design
1 Entities
The Student Study Management System contains three main entities. These entities represent the main objects of the system.
1. Student
The Teacher entity stores basic information about teachers.
2. Teacher
The Teacher entity stores basic information about teachers.
3. Subject
The Subject entity stores information about the subjects taught in the system.
2 Attributes
Student Attributes
Student ID — A unique identification number for each student.
Student Name — The name of the student.
Age — The age of the student.
Semester — The current semester of the student.
Teacher Attributes
Teacher ID — A unique identification number for each teacher.
Teacher Name — The name of the teacher.
Specialization — The area in which the teacher specializes.
Subject Attributes
Subject ID — A unique identification number for each subject.
Subject Name — The name of the subject.
Credit Hours — The number of credit hours of the subject.

3.1 Primary Keys
A Primary Key (PK) is a unique field used to identify each record in a table. A primary key cannot contain duplicate values.
In our project:
Student ID → Primary Key of Student table 
Teacher ID → Primary Key of Teacher table
Subject ID → Primary Key of Subject table
3.2 Foreign Keys
A Foreign Key (FK) is a field that connects one table with another table. It usually refers to the Primary Key of another table.
In our project, we will decide the required Foreign Keys after defining the relationships between Student, Teacher, and Subject.












4 — SQL Queries
4.1 SELECT Query
SELECT * FROM student;

Explanation:
This query displays all records from the Student table.
4.2 JOIN Query
SELECT 
    student.student_name,
    subject.subject_name,
    teacher.teacher_name
FROM student
JOIN subject
ON student.subject_id = subject.subject_id
JOIN teacher
ON subject.teacher_id = teacher.teacher_id;
Explanation:
This query connects the Student, Subject, and Teacher tables and displays related information.
4.3 WHERE Query
SELECT 
    student.student_name,
    subject.subject_name,
    teacher.teacher_name
FROM student
JOIN subject
ON student.subject_id = subject.subject_id
JOIN teacher
ON subject.teacher_id = teacher.teacher_id
WHERE subject.subject_name = 'Database Systems';
Explanation:
This query displays only the students who are studying Database Systems.
4.4 ORDER BY Query
SELECT *
FROM student
ORDER BY student_name ASC;
Explanation:
This query arranges the student names in alphabetical order from A to Z.
4.5 UPDATE Query
UPDATE student
SET age = 22
WHERE student_name = 'Ahmed';
Explanation:
This query updates Ahmed's age to 22.
4.6 COUNT Query
SELECT COUNT(*) AS total_students
FROM student;
Explanation:
This query counts the total number of students in the Student table.
4.7 GROUP BY Query
SELECT subject_id, COUNT(*) AS total_students
FROM student
GROUP BY subject_id;
Explanation:
This query groups students according to their subject and counts the students in each subject.
4.8 DISTINCT Query
SELECT DISTINCT subject_id
FROM student;
Explanation:
This query displays only unique subject IDs and removes duplicate values.
5.Conclusion
The Student Study Management System successfully demonstrates the basic concepts of database design and management. The project stores information about students, teachers, and subjects in a structured database.
The project includes an ERD, database tables, primary keys, foreign keys, relationships, and SQL queries. MySQL and phpMyAdmin are used to create and manage the database.
Overall, this project helped in understanding how a relational database is designed and how SQL is used to store and retrieve information.
































