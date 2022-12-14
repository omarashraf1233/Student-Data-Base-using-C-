# Student-Data-Base-using-C-
Create a database module "SimpleDb" that holds the following parameters:
1- Student ID
2- Student Year
3- Course_1 ID
4- Course_1 Grade
5- Course_2 ID
6- Course_2 Grade
7- Course_3 ID
8- Course_3 Grade

Note: The maximum size of the database is 10 entries

The following Interfaces should be provided by the developed module:

1- bool SDB_IsFull(void)
//Description: Check if the database is full
//Return Value: Return 1 if the the database is full, otherwise 0

2- uint8 SDB_GetUsedSize(void)
//Description: Get the number of entries in the database
//Return: Return the number of entries

3- bool SDB_AddEntry(uint8 id, uint8 year, uint8* subjects, uint8* grades)
Description: Add new entry to the database
//Return: Return 1 if the new entry is successfully added; otherwise 0
//Input Parameter - id: Student ID
//Input Paramater - year: Student Year
//Input Parameter - subjects: Pointer to 3 subject IDs, with each subject id is a uint8 value
//Input Parameter - grades: Pointer to 3 grades, with each grade is a uint8 value
//The allowed range for the grade is only from 0 to 100
//Assume that the caller will always provide the 3 subjects with their grades

4- void SDB_DeleteEntry(uint8 id)
//Description: Delete the entry with the given ID
//Input Parameter - id: ID of the entry to be deleted

5- bool SDB_ReadEntry(uint8 id, uint8* year, uint8* subjects, uint8* grades)
//Description: Read an entry matching the provided ID
//Return Value: Return 1 if the entry exist, otherwise 0
//Input Parameter - id: Student ID
//Output Parameter - year: Pointer to the student year
//Output Parameter - subjects: Pointer to the subjects
//Output Parameter - grades: Pointer to the grades

6- void SDB_GetIdList(uint8* count, uint8* list)
//Description: Get the list of IDs of the students
//Output Parameter - count: Pointer to the number of entries currently exists in the 
database
//Output Parameter - list: Pointer to the list of IDs

7- bool SDB_IsIdExist(uint8 ID)
//Description: Checks if the the provided student ID exists
//Return Value: Return 1 if ID exists in the database, otherwise 0
