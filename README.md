# PLSQL- 2.1
1.	Produce an unduplicated list of all product IDs for all products that have been sold. Sort the list.
2.	Show the basket ID, product ID, product name, and description for all items ordered. (Do it two ways—one with an ANSI join and one with a traditional join.)
3.	Modify the queries in Step 2 to include the customer's last name.
4.	Display all orders (basket ID, shopper ID, and date ordered) placed in February 2012. The date should be displayed in this format: February 12, 2012.
5.	Display the total quantity sold by product ID.
6.	Modify the query in Step 5 to show only products that have sold less than a quantity of 3.
7.	List all active coffee products (product ID, name, and price) for all coffee items priced above the overall average of coffee items.
8.  Create a table namd CONTACTS that include the following columns
9.	Add two rows of data to the table, using data values you create. Make sure the default option on the LAST—DATE column is used in the second row added. Also, issue a command to save the data in the table permanently.
10.	Issue a command to change the e-mail value for the first row added to the table. Show a query on the table to confirm that the change was completed. Then issue a command to undo the change.


LAB1
---A Review of   “SQL” command line properties and SQL*Plus Print Commands

Problem:  
You are a new employee at the XYZ Corp. and you have been hired as a Database Programmer to replace an experienced Database programmer ( user known as  ‘ORDERS’ as the owner on the system)  that has moved on to bigger and more challenging assignments.
This is your first day on the job and you will not get to meet with the person you are replacing for a few days and will not get much time with that person as their assignment will keep them on the road for the majority of the time. Therefore, your problem is to gain as much information about their old assignments before you meet with them so as to maximize the benefit of your Q & A time when you do meet.

Your first question is:
1)What Database Objects( tables) am I responsible for, how can I find them,  
and 2) read through it before your meeting?--

A)	Locate tables for this class.
 Use Select              Table_name from all_tables

Your first step is to print the information by querying all the tables to find the names of the FIELDS.  Be sure to include table names and for the owner information.   
B)	Describe tables you will be using
with   “Describe: command.
You have been handed  select commands that will assist in
1)	Defining the names of the tables (objects) owned by ‘ORDERS’  
2)	All of the Columns

3)	Table Constraints for the tables (objects) owned by ‘ORDERS’.
4)	Constraint Type

Use the information gained from the describe command and add the needed data to gain this information.   --  You may well want to include the following Column commands to clean up the Constraint results that produce wrapped rows of data.

	 SQL> Column Table_name heading ‘Table|Name’ Format A___
	 SQL> Column Column_Name Heading ‘Column|Name’ Formatm A___
	 SQL> Column Constraint_Name Heading ‘Constraint|Name’ Format A___
	 SQL> Column Constraint_Type Heading ‘Constraint|Type’ Format A___

Your final step will then be to perform   SELECT * and   DESCRIBE commands for each of these tables owned by ‘ORDERS’.


LAB2
1.
	Create an Anonymous block. Declare a Sequence Number named list#, a
constant named C_XYZ that is Number(10), an Binary Integer named V_Counter1, a variable named V_Row_number based on the column Row in the Theater Table (you will have to create the table and the row), and a character string named String A that is up to 50 characters long. Print out and hand in the code and show that it compiled without errors. Hint:(You will have to include a Begin with a Null Process and an end to get this to compile).

2.
Create an Anonymous block that Creates and Inserts data into the Student, Course
and Student/Course composite tables using the Create and Insert commands. You will find the table description attached. Print out and hand in the code, the proof that it successfully compiled and show the tables created and populated by the code using the Select and Describe commands.

3.
Create an Anonymous block that counts the number of courses a student is signed up for in the Course/Student composite table. Use the tables you created in #2 above. Print out and hand in the code, the proof that it successfully compiled and show the test results. No error processing should be required. Hint:(Use the select Into command for each student inside a loop to determine this information).

4.
Create an Anonymous block that counts the number of students enrolled in the Student table. Use DBMS Output Putline to send out a message  stating the number of students found. Print out and hand in the code, the proof that it successfully compiled and show test results. No error processing required.

5.
Create an Anonymous block that determines the number of courses in the StudentCourse table and (using the IF statement) if the number is greater than 10 sends out a message (using DBMS Output Putline) stating that “more than 10 courses have been established”. If the number is less than 10 send out a message stating “less than 10 courses established”.  Print out and hand in the code, the proof that it successfully compiled and show test results. No error processing required.

6.
Create a Named block that tests each student entry in the student table to see if the student is an instate student. Print out, (using the DBMS Output Putline) a line stating that each student is or is not an instate student and a count of the students in and out of state at the end of the program. Print out the code, the proof that it successfully compiled and show test results. No error processing required.

7.
	Create a Named block that takes the information provided by Named Parameters,
&Variable_Name, to determine if a student is registered in the specified course from the student/course table created above. Use the DBMS Output Putline to send a message indicating if the student specified is in the course specified. Print out the code, the proof that it successfully compiled and show test results. No error processing required.

8.
Create a Named block that uses the If construct to test if each student is male or female and the Case Construct to determine if the major is a Math, English, Comp Sci, or Geography major. Print out the code, the proof that it successfully compiled and show test results. No error processing required.


9.
Create a Named block that performs the same activity as in #8 above using the If construct in place of the Case Construct. Print out the code, the proof that it successfully compiled and show test results. No error processing required.

10.
Create a Named block that Inserts rows of data from the student table into a  temporary table and uses a loop with a counter to know when to exit. Set the counter equal to the Count of the rows in the student table so it will know when to end processing. Print out the code, the proof that it successfully compiled and show test results. No error processing required. Hint:(You will need to create the Temporary Table first. Use a loop to take each row from the student table and place it in the Temporary Table).


Student Table

Stu_ID  Lname      Fname Mi  Sex          Major       Home_State

10001    Smith       Ron     M   M          Math	            Tx
10002    Jones        Peter   A    M          English	Tx
10003    Peters       Anne   A    F           English	Me
10004    Johnson    John    J     M          CompSci	Ca
10005	  Penders    Alton   P     F           Math             Ga
10006    Allen        Diane  J      F	   Geography	Minn
10007	  Gill	       Jennifer	  F	   CompSci       Tx
10008	  Johns	       Roberta      F	   CompSci	 Tx
10009	  Wier	       Paul           M	   Math		 Ala
10010	  Evans       Richard      M          English          Tx


Course Table

Course_ID       Section#       C_Name                        C_Description

COSC1300       001	      Intro to Comp.		First Computer Course
ITSE2309         001	      Intro to DB		First Database Course
GEOG1791      002	      World Geography		Second Geography Course
COSC1315       001	      Intro to Prog.		Second Computer Course
ITSE1345         001	      Intro to DB Prog.		Second Database Course
ENGL2617       002	      English Literature		Second English Course
MATH1101      001	      Calculus 1			Second Math Course
ENGL1001       001	      American Literature	First English Course
MATH1011      001	      Trig. & Algebra		First Math Course
GEOG1010      001	      Texas Geography		First Geography Course

Student_Course Table

Stu_ID         Course_ID       Section#
10001	         MATH1101	001
10002	         ENGL2617         002
10003	         ENGL1001	001
10003	         ENGL2617         002
10003	         GEOG1010	001
10004	         COSC1315	001
10005	         MATH1101	001
10006	         GEOG1010	001
10006	         GEOG1791	002
10007	         COSC 1315	001
10007	         ITSE2309	001
10008	         COSC1315	001
10009	         ITSE2309	001
10010	         ENGL2617         002

LAB3
PL/SQL Programs (100 Points)
1. Write a PL/SQL procedure which will find the data for a given employee using the employee number. The procedure specification is as follows: Purpose: To retrieve and list the data for a given employee Input Parameter: The employee number Input/Output parameters: None Output Parameters: None Preconditions: The employee number should exist. If he/she does not exist, handle it with an exception and appropriate message. Post Conditions:)Print out each column in the employee row. The employee table is unchanged. - Use %ROWTYPE to define a structure in which to store the column values. - Write a simple driver to call and test the procedure. - Test one valid employee (Empno = 7654) and one invalid employee (Empno = 7888)
2.  Write a function which inputs two dates and compares the two dates. The function returns —1, 0, or +I depending on whether the 1st  date is less than, equal to, or greater than the 2' date. (The time component is not to be considered here).
Purpose: To compare two dates Input Parameters: 2 dates Input/Output parameters: None Output Parameters: None Return Value: Integer (-1, 0, +1) Preconditions: Dates in standard format Postconditions: Dates unchanged. Comparison Value Returned. - Write a simple driver to call and test the procedure - Test each of the three different possible comparison values.
3. Write a procedure which inputs an account ID and returns the customer information for that account.
Purpose: To find the customer information for a given account number Input Parameters: Account ID Input/Output Parameters: None Output Parameters: Row of customer table that has the account ID Preconditions: Account ID is valid Postconditions: Customer Table unchanged. If customer found, customer row returned, If customer not found, return Message "Cust_ID not valid" and customer row is returned as garbage. - Write a simple driver to call and test the procedure. The driver should print out the fields of the row that is returned.
4.  Write an anonymous block which updates the .Physician table.(As you can not update the Physician Table, you will have to create your own table based on the structure and contents of the .Physician Table). Use named parameters to get values for Phys_ID, Phys_name, Phys_phone, and Phys_speciality. If the value for Phys_ID is in the Physician Table, Update the values of the remaining columns. If the Phys_ID is not in the Physician Table, INSERT a row into the Physician Table with those values. - Hint: Use variables for each of the columns above and assign a named parameter to each of them., Then use the variable in the rest of the block. - Write a simple driver to test the block with a Phys_ID that is in the Physician Table and a Phys_ID that is not in the Physician Table.
5. Write a function that adjusts a string to a specific length. - If there are any leading spaces, delete them. - If the specified length is greater than the actual length of the string, the string is padded on the right by spaces. - If the specified length is less than the actual length of the string, the string is truncated on the right to the specified length.
Input Parameters: String, Specified Length Output Parameters: None Input/Output Parameters: None Return Value: VARCHAR2 (adjusted string)
Write a simple driver to test the function. Call the function with the following parameters: o String: 'Now is the Time.' • Specified length = 6 o String: 'Now is the Time.' • Specified length = 25 o String: 'bbbbNow is the Time.bbbbbbbbb' (Where b = Blank Space) • Specified length = 15
- Display the original string, the adjusted string and the length of the adjusted string.
Problems I - 5 For all of these procedures, hand in a printout showing:
1. The procedure to be executed
2. The execution of a driver to call and execute the code
3. The accomplished results on of the procedure/function (includes returns, messages, etc.)
4. A select and/or describe of the table(s) show the changes, if any

Pat_Nbr Pa't_Name Pat_Address Pat_City Pat_State Pat_ZIP Pat_Room Pat_Bed
1379 Cribbs, John 2110 Main St. Austin TX 78711 101 1
3249 Baker, Mary 3547 W. 42 nd  St. Berkeley CA 94117 137 2
4500 Garcia, Juan 1533 Telegraph Berkeley CA 94117 228 2
5116 Harris, Carol 4710 Ave. E Austin TX 78705 438 1
5872 Zimmer, Elka 7988 Cedar Cleveland OH 44060 137 1
6213 Rose, David 322 Bridge Ave. Redwood CA 94065 100 1
7459 Smith, Chris 788 Cummings Cleveland OH 44066 438 3
8031 Fitch, Sylvia 3380 Fox Ave. Madison WI 53711 420 4
8659 Hernandez, Juan 8300 Geneva Dr. Austin TX 78723 350 2

Physician Table-
Phys_ID Phys_Name Phys_Phone Phys_Specialty
101 Wilcox, Chris 512-329-1848 Eyes, Ears, Throat
102 Nusca, Jane 512-516-3947 Cardiovascular
103 Gomez, Juan 512-382-4987 Orthopedics
104 Li, Jan 512-516-3948 Cardiovascular
105 Simmons, Alex 512-442-5700 Hemotology
Treament Table
Pat_Nbr Phys_ID Trt_Procedure Trt Date
3249 101 13-08 12-FEB- 1999
1379 103 27-45 25-MAR-1999
3249 103 88-20 22-JAN-1999
5116 104 52-14 03-APR-1999
4500 101 13-08 04-FEB-1999
8031 102 52-14 15-MAR-2000
5116 104 52-14 05-FEB-2001
5872 105 60-00 13-FEB-2000
3249 103 88-20 24-JAN-2000
8659 104 60-00 08-APR-2001
Procedure Table /
Pro_Nbr Pro_Desc Pro—Charge
13-08 Throat culture 15.00
27-45 X-Ray 62.00
52-14 Cardiogram 135.00
60-00 Blood Analysis 58.00
88-20 MRI 800.00

LAB4
1.  Write a PL/SQL procedure which will determine whether a given range of customer has a purchase order or not. Use the explicit cursor to process the table data. The procedure specification is as follows: 

Purpose: To test whether a customer has at least one purchase order for a given range of
   customer numbers.
	Input arguments: 1) The low Cust_ID value for the customer number range.
			     2) The high Cust_ID value for the customer number range.
	Input/Output arguments:    NONE
 	Output arguments:     NONE
	Preconditions: The first Cust_ID parameter value should be less than the second Cust_ID
 parameter  value. If not, put out an appropriate error message.
	Postconditions: Order the output by Cust_ID. Print out the Cust_ID and either the message
 			 ‘has a purchase order’ or the message ‘does not have a purchase order’.

	Write a simple driver to call the procedure. Tets the following ranges of Cust_Ids.

•	90001 to 90008
•	90003 to 90007
•	90009 to 90010
•	90005 to 90004

2.  Construct a PL/SQL package named Hospital which operates on the Physician,
    Treatment, and Patient tables as you did in Lab #3 by creating your own tables. The Package should contain the
    following:
•	A PL/SQL table named t_patTrt defined in the specification which contains a RECORD with the following fields: Pat_Nbr, Trt_Procedure, Phys_ID, Phys_Name, Phys_Specialty.
•	One exception: Named e_DupPhysFound.
•	A Procedure named BuildPatTbl, which will build a table of all treatments for all patients. The table will be an output parameter. A second Input/Output Parameter will be the number of rows returned in the table. The indexes in the table will start at 1 and be incremented by 1. For each treatment, include Pat_Nbr, Trt_Procedure, Phys_ID, Phys_Name, and Phys_specialty in the table.
•	2 overload functions, both named FindPatient, to check to see if a patient is in the database eitherby patient number or name. That is, the input value could be either the patient number or name. RETURN true, if the patient is found: FALSE if the patient is not found.
•	A procedure named NewPhys which inserts a new physician into the physician table. The input parameters are: Phys_ID, Phys_Name, Phys_Phone, and Phys_Specialty. The procedure should check to see if the physician is already in the table. If he/she is in the table, raise the exception e_DupPhysFound. Do Not Check for any exceptions in this procedure.

3.  Write a driver to test the package above. The driver should do the following:
•	Call the FindPatient function with 	1) a valid Patient ID Number
  	2) a Valid Patient Name
  	3) an invalid Patient ID Number.
•	Use the NewPhys procedure to 		1) Insert a new physician into the Physician table
2) attempt to insert a physician who already exists in the Physician table.
3) Check for the exception e_DupPhysFound in this driver
•	Decalre a table of the type t_PatTrt.
•	Call the Procedure BuildPatTbl which will store patients and treatments in the above table. List the patients returned in the table. List all fields in the table for each patient.

4.  Modify and add data to your Physician, Patient, and Treatment tables so that the tables look like the following. Also be sure that the Primary Key and Foreign Key constraints are still in effect. Note that the Pat_Room and Pat_Bed have changed values in some cases. Also, a new table has been added.  

Patient Table

Pat_Nbr	    Pat_Name              Pat_Address            Pat_City       Pat_State      Pat_ZIP      Pat_Room     Pat_Bed
-----------    -------------------     -------------------       -------------    ------------     ----------      -------------     -----------
1379           Cribbs, John          2110 Main St.         Austin	    TX     	         78711             101       	1
3249	     Baker, Mary          3547 W. 42nd St.     Berkeley	    CA	         94117         	   137		2
4500	     Garcia, Juan	      1533 Telegraph       Berkeley	    CA	         94117             228		2
5116           Harris, Carol          4710 Ave. E	         Austin	    TX 	         78705	   438		1
5872	    Zimmer, Elka         7988 Cedar	         Cleveland       OH     	         44060	   137		1
6213	    Rose, David           322 Bridge Ave.      Redwood	    CA    	         94065	   100		1
7459	    Smith, Chris           788 Cummings       Cleveland       OH	         44066   	   438		3
8031	    Fitch, Sylvia	      3380 Fox Ave.        Madison	    WI 	         53711	   420		4
8659	    Hernandez, Juan    8300 Geneva Dr.    Austin	    TX     	         78723	   350		2

Physician Table

Phys_ID		Phys_Name		Phys_Phone		Phys_Specialty
-----------	------------------------	------------------		--------------------------
  101		Wilcox, Chris		512-329-1848		Eyes, Ears, Throat
  102		Nusca, Jane		512-516-3947		Cardiovascular
  103		Gomez, Juan		512-382-4987		Orthopedics
  104		Li, Jan			512-516-3948		Cardiovascular
  105		Simmons, Alex 		512-442-5700		Hemotology

Treament  Table

Pat_Nbr		Phys_ID		Trt_Procedure		Trt_Date
----------		-----------	------------------		------------
3249		101		13-08			12-FEB-1999
1379		103		27-45			25-MAR-1999
3249		103		88-20			22-JAN-1999
5116		104		52-14			03-APR-1999
4500		101		13-08			04-FEB-1999
8031		102		52-14			15-MAR-2000
5116		104		52-14			05-FEB-2001
5872		105		60-00			13-FEB-2000
3249		103		88-20			24-JAN-2000
8659		104		60-00			08-APR-2001

Procedure Table

Pro_Nbr		Pro_Desc		Pro_Charge
----------		-----------------------	---------------
13-08		Throat culture		  15.00
27-45		X-Ray			  62.00
52-14		Cardiogram	            	135.00
60-00		Blood Analysis		  58.00
88-20		MRI			800.00

1)	Assume that a treatment procedure can be given to a patient only once on a given date.
2)	A patient can receive the same treatment procedure from a different physician.

•	Hand in:
o	A listing of each table.
o	Show the commands used  to change these tables.

5. Write a Trigger for inserting into or updating the treatment table, which checks the treatment date to ensure that it is no later than today and no earlier than 3 months ago. If it violates this constraint, raise an application error
(-20100, ‘Invalid treatment date’)
•	Test by inserting 2 rows, one insert with an acceptable date, and one with an invalid date.
•	Hand-in:
o	Listing of the Trigger
o	Listing of the test results

6.
a. Create a new table called Trt_Stats to keep track of the number of times each Trt_Procedure is modified (INSERT, DELETE, or UPDATE):

	Trt_Stats (Trt_Procedure, Trt_INS_Count, Trt_DEL_Count, Trt_UPD_Count)

•	Hand-in:
o	CREATE TABLE statement
o	DESCRIBE TABLE statement

b. Write a TRIGGER for the Treatment Table which does the following:
•	Each time an INSERT is made into the Treatment Table, add 1 to the Trt_INS_Count for that Procedure if it exists in the table. If it does not exist in the table, add a row to the table for the procedure setting Trt_INS_Count to 1.
•	Each time a DELETE is made, add 1 to the Trt_DEL_Count for that Procedure if it exists in the table. If it does not exist in the table, add a row to the table for the procedure and set Trt_DEL_Count to 1.
•	Each time an UPDATE occurs for a Trt_Procedure, add 1 to the Trt_UPD_Count.  If it is not in the table, add a row to the table for the procedure and set Trt_UPD_Count to 1. If the Column Trt_Procedure is changed, add 1 to the Trt_UPD_Count for the old procedure.
•	Test by doing several INSERTs, DELETEs, and UPDATEs and then display the Trt_Statsmtable.

•	Hand-in:
o	Trigger Listing
o	Test Results
