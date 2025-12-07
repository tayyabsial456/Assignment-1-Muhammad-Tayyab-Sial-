# Assignment 1: Student Record Manager

## Objective
To build a basic Student Record Manager using a class structure to store, analyze, and retrieve student data. This assignment requires integrating concepts of variables, control flow, functions, loops, strings, and fundamental data structures (Lists, Dictionaries, Tuples, Sets), culminating in the use of Object-Oriented Programming (OOP).

## Part 1: The Student Class (OOP and Data Structures)
Create a Python class named Student.

    1. Class Attributes (Variables):

        - The Student class must have an initializer (__init__) that accepts the following arguments:
            - name (String)
            - student_id (String or Integer)
            - courses_and_grades (Dictionary, e.g., {'Math': 85, 'Science': 92, 'History': 78})

    2. Methods (Functions):
        - **get_average_grade(self)**:
            - Calculates and returns the average grade from the courses_and_grades dictionary.
        - **add_course_and_grade(self, course_name, grade)**:
            - Adds a new course and its corresponding grade to the student's courses_and_grades dictionary.
        - **get_honors_courses(self, threshold=90)**:
            - Uses a loop and conditional execution to find all courses where the grade is equal to or above the threshold (defaulting to 90).
            - Returns these high-performing course names as a List.
        - **get_unique_grades(self)**:
            - Returns a Set of all the unique grades the student has received.

## Part 2: The Manager Logic (Sequence Functions and Control Flow)
Outside of the Student class, implement the following steps:

    1. Initialize Data (Lists and Tuples):
        - Create a List named all_students to store instances (objects) of the Student class.
        - Create at least three Student objects with diverse data. For one student, ensure their initial courses are stored as a Tuple of (course, grade) pairs (e.g., [('Art', 95), ('PE', 88)]) and have your class initializer convert this into the required dictionary format upon creation.
    
    2. Apply Logic (Loops and Conditionals):
        - Use a Loop to iterate through the all_students list.
        - Inside the loop, use a Conditional Statement to check if a student's get_average_grade() is above 80.
        - If the average is above 80, print a formatted statement using String formatting (e.g., f-strings) saying: "[Student Name] has an excellent average of [Average Grade] and the following honor courses: [List of Honor Courses]".
        - If the average is 80 or below, call the add_course_and_grade method for that student, giving them a new course "Study Skills" with a grade of 100, and then print a statement confirming the addition.[muhammad_tayyab_sial_assignment_1.py](https://github.com/user-attachments/files/24019360/muhammad_tayyab_sial_assignment_1.py)
[muhammad_tayyab_sial_assignment_1.py](https://github.com/user-attachments/files/24019358/muhammad_tayyab_sial_assignment_1.py)
