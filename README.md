# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
	#include <stdio.h>
	
	int main() {
	    int length, breadth, area;
	    int *lptr = &length, *bptr = &breadth;
	
	    printf("Enter length and breadth of the rectangle: ");
	    scanf("%d%d", lptr, bptr);
	
	    area = (*lptr) * (*bptr);
	
	    printf("Area of rectangle: %d\n", area);
	
	    return 0;
	}

## OUTPUT:
![image](https://github.com/user-attachments/assets/59977749-86e2-43b9-abe6-ce1d3afee768)

## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
	#include <stdio.h>
	#include <stdlib.h>
	#include <string.h>
	
	int main() {
	    char *ptr;
	
	    ptr = (char *)malloc(8 * sizeof(char)); // 7 letters + 1 for '\0'
	
	    if (ptr == NULL) {
	        printf("Memory allocation failed.\n");
	        return 1;
	    }
	
	    strcpy(ptr, "WELCOME");
	
	    printf("%s\n", ptr);
	
	    free(ptr);
	
	    return 0;
	}

## OUTPUT
![image](https://github.com/user-attachments/assets/0b046586-6af2-4a15-986f-5301732d6ba2)

## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully

# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
	#include <stdio.h>
	
	struct Student {
	    char name[50];
	    int age;
	    float marks;
	};
	
	int main() {
	    struct Student s;
	
	    printf("Enter student's name: ");
	    fgets(s.name, sizeof(s.name), stdin);
	
	    printf("Enter student's age: ");
	    scanf("%d", &s.age);
	
	    printf("Enter student's marks: ");
	    scanf("%f", &s.marks);
	
	    printf("\nStudent Information:\n");
	    printf("Name: %s", s.name);
	    printf("Age: %d\n", s.age);
	    printf("Marks: %.2f\n", s.marks);
	
	    return 0;
	}

## OUTPUT:
![image](https://github.com/user-attachments/assets/0a695223-08d5-4d18-9ada-ac0f92c867dd)

## RESULT

Thus the program to store the student information and display it using structure has been executed successfully

# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
	#include <stdio.h>
	
	struct Employee {
	    char name[50];
	    int id;
	    float basicSalary;
	    float grossSalary;
	};
	
	int main() {
	    struct Employee emp[3];
	
	    for (int i = 0; i < 3; i++) {
	        printf("Enter details for employee %d:\n", i + 1);
	        printf("Name: ");
	        scanf("%s", emp[i].name);
	        printf("ID: ");
	        scanf("%d", &emp[i].id);
	        printf("Basic Salary: ");
	        scanf("%f", &emp[i].basicSalary);
	
	        emp[i].grossSalary = emp[i].basicSalary + (0.8 * emp[i].basicSalary) + (0.2 * emp[i].basicSalary);
	    }
	
	    printf("\nEmployee Details with Gross Salary:\n");
	    for (int i = 0; i < 3; i++) {
	        printf("Name: %s\n", emp[i].name);
	        printf("ID: %d\n", emp[i].id);
	        printf("Basic Salary: %.2f\n", emp[i].basicSalary);
	        printf("Gross Salary: %.2f\n\n", emp[i].grossSalary);
	    }
	
	    return 0;
	}

 ## OUTPUT:
 ![image](https://github.com/user-attachments/assets/11120889-55b9-4faf-b755-57571d604d51)

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure

# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
	#include <stdio.h>
	
	struct Student {
	    char name[50];
	    int marks[5];
	    int total;
	    float average;
	};
	
	int main() {
	    struct Student s;
	    s.total = 0;
	
	    printf("Enter student's name: ");
	    fgets(s.name, sizeof(s.name), stdin);
	
	    printf("Enter marks for 5 subjects:\n");
	    for (int i = 0; i < 5; i++) {
	        printf("Subject %d: ", i + 1);
	        scanf("%d", &s.marks[i]);
	        s.total += s.marks[i];
	    }
	
	    s.average = s.total / 5.0;
	
	    printf("\nStudent Information:\n");
	    printf("Name: %s", s.name);
	    printf("Total Marks: %d\n", s.total);
	    printf("Average Marks: %.2f\n", s.average);
	
	    return 0;
	}

## OUTPUT
![image](https://github.com/user-attachments/assets/19b3c132-c8d7-4829-aca0-4fae569c2c69)

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	
