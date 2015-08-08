#COMP3311-Assignment4

##Assignment description##
* You are required to build a simple information system for the University according to the database schema given below, so that the professors can retrieve useful information from the system. You need to complete a program using the C++ language and the ODBC interface. A skeleton of the C++ program is provided to you in the package.
* You need to build the tables and insert the records to the Oracle server before you can run the information system. So, you have to log in to Oracle using the SQLPlus client, and run the following three script files, drop_tables.sql, create_tables.sql, insert_records.sql. These three script files are also included in the package.
* After running the script files, make sure you issue the “commit;” command at the SQLplus prompt so that the data are physically written to the Oracle DBMS. You can then start your C++ program. You will be logged in to the Oracle server using your own Oracle account (i.e. comp3311stuxxx, xxx is from 001-089). This part has been done for you in the skeleton C++ program provided.

**The system should allow a professor to log in with his password and perform queries regarding**
- - - -
* Teaching information:
   (a) display the course_ID, course_name, offering_no, classroom, and no_of_stds of all the courses he/she is teaching in the current semester (assume the current semester is ‘Spring2014’),
   (b) display the course_ID, course_name, offering_no, classroom, and no_of_stds of the course he/she is “leading” in the current semester (assume the current semester is ‘Spring2014’).
   (c) group the prerequisites (course_IDs) by the course_IDs of the main courses and display the prerequisites (course_ID) in a list. See the screen shot in the assignment output section for the expected output. Hint: you will find the aggregate function LISTAGG() function useful. You can refer to http://www.oracle-developer.net/display.php?id=515 for the exact syntax of LISTAGG().

* Supervision information:
   (a) display all the student_ID, last_name, first_name, phone of all the students he/she supervises.
   (b) group the students (student_ID, last_name, first_name) according to the supervisors’ staff_IDs, and display the student information in a list in ascending order of the student_IDs, see the screen shot for the exact output.
Hint: you may find the LISTAGG() function and the concatenation operator “||” useful.
￼
* Administrative information:
   (a) change the login password for himself/herself,
   (b) add a phone number for himself/herself (assume professors do no share phone numbers),
   (c) displays the student_ID, last_name, first_name, and phone number for each TA of the course offerings he/she teaches in the current semester (assume the current semester is ‘Spring2014’),
   (d) display the lists of all the preferred offerings (course_ID, offering_no) for all the TAs, group the result by the TAs’ student_IDs. Hint: you will find the aggregate function LISTAGG() function useful.
