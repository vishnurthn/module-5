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
    float length, breadth, area;
    float *ptrLength, *ptrBreadth;

    
    ptrLength = &length;
    ptrBreadth = &breadth;

    
    printf("Enter the length of the rectangle: ");
    scanf("%f", ptrLength);

    printf("Enter the breadth of the rectangle: ");
    scanf("%f", ptrBreadth);


    area = (*ptrLength) * (*ptrBreadth);

    printf("The area of the rectangle is: %.2f\n", area);

    return 0;
    }



## OUTPUT

    Enter the length of the rectangle: 5.5
    Enter the breadth of the rectangle: 3.2
    The area of the rectangle is: 17.60


## NAME: Vishnu Rathan B
# REG NO:212224240185


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

    int main() {
    char *str;

   
    str = (char *)malloc(8 * sizeof(char));

   
    if (str == NULL) {
        printf("Memory allocation failed!\n");
        return 1;
    }

    str[0] = 'W';
    str[1] = 'E';
    str[2] = 'L';
    str[3] = 'C';
    str[4] = 'O';
    str[5] = 'M';
    str[6] = 'E';
    str[7] = '\0'; // null-terminator for string

   
    printf("%s\n", str);

    
    free(str);

    return 0;
    }


## OUTPUT

WELCOME


## NAME: Vishnu Rathan B
# REG NO:212224240185



## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



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
    int roll_no;
    char name[50];
    float marks;
    };

    int main() {
    struct Student s;

    
    printf("Enter student's roll number: ");
    scanf("%d", &s.roll_no);

    printf("Enter student's name: ");
    scanf("%s", s.name);

    printf("Enter student's marks: ");
    scanf("%f", &s.marks);

    
    printf("\n--- Student Information ---\n");
    printf("Roll Number: %d\n", s.roll_no);
    printf("Name: %s\n", s.name);
    printf("Marks: %.2f\n", s.marks);

    return 0;
    }



## OUTPUT

    Enter student's roll number: 101
    Enter student's name: yash
    Enter student's marks: 89.5

    --- Student Information ---
    Roll Number: 101
    Name: yash
    Marks: 89.50


## NAME: Vishnu Rathan B
# REG NO:212224240185



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
    int id;
    char name[50];
    float basic_salary;
    float hra;  // House Rent Allowance
    float da;   // Dearness Allowance
    float gross_salary;
    };

    int main() {
    struct Employee emp[3];
    int i;

   
    for(i = 0; i < 3; i++) {
        printf("\nEnter details for Employee %d:\n", i + 1);

        printf("ID: ");
        scanf("%d", &emp[i].id);

        printf("Name: ");
        scanf("%s", emp[i].name);

        printf("Basic Salary: ");
        scanf("%f", &emp[i].basic_salary);

        printf("HRA: ");
        scanf("%f", &emp[i].hra);

        printf("DA: ");
        scanf("%f", &emp[i].da);

        
        emp[i].gross_salary = emp[i].basic_salary + emp[i].hra + emp[i].da;
    }

    
    printf("\n--- Employee Details ---\n");
    for(i = 0; i < 3; i++) {
        printf("\nEmployee %d:\n", i + 1);
        printf("ID: %d\n", emp[i].id);
        printf("Name: %s\n", emp[i].name);
        printf("Basic Salary: %.2f\n", emp[i].basic_salary);
        printf("HRA: %.2f\n", emp[i].hra);
        printf("DA: %.2f\n", emp[i].da);
        printf("Gross Salary: %.2f\n", emp[i].gross_salary);
    }

    return 0;
    }



 ## OUTPUT

    Enter details for Employee 1:
    ID: 101
    Name: Aman
    Basic Salary: 25000
    HRA: 5000
    DA: 3000

    Enter details for Employee 2:
    ID: 102
    Name: Riya
    Basic Salary: 30000
    HRA: 6000
    DA: 4000

    Enter details for Employee 3:
    ID: 103
    Name: Arjun
    Basic Salary: 20000
    HRA: 4000
    DA: 2000

    --- Employee Details ---

    Employee 1:
    ID: 101
    Name: Aman
    Basic Salary: 25000.00
    HRA: 5000.00
    DA: 3000.00
    Gross Salary: 33000.00

    Employee 2:
    ID: 102
    Name: Riya
    Basic Salary: 30000.00
    HRA: 6000.00
    DA: 4000.00
    Gross Salary: 40000.00

    Employee 3:
    ID: 103 
    Name: Arjun
    Basic Salary: 20000.00
    HRA: 4000.00
    DA: 2000.00
    Gross Salary: 26000.00




## NAME: Vishnu Rathan B
# REG NO:212224240185
 

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
    int roll_no;
    float marks[5];
    float total;
    float average;
    };

    int main() {
    struct Student s;
    int i;

   
    printf("Enter student's name: ");
    scanf("%s", s.name);

    printf("Enter student's roll number: ");
    scanf("%d", &s.roll_no);

    printf("Enter marks for 5 subjects:\n");
    s.total = 0;
    for(i = 0; i < 5; i++) {
        printf("Subject %d: ", i + 1);
        scanf("%f", &s.marks[i]);
        s.total += s.marks[i];
    }

    
    s.average = s.total / 5;

   
    printf("\n--- Student Result ---\n");
    printf("Name: %s\n", s.name);
    printf("Roll Number: %d\n", s.roll_no);
    printf("Total Marks: %.2f\n", s.total);
    printf("Average Marks: %.2f\n", s.average);

    return 0;
    }



## OUTPUT

    Enter student's name: Rahul
    Enter student's roll number: 10
    Enter marks for 5 subjects:
    Subject 1: 85
    Subject 2: 78
    Subject 3: 92
    Subject 4: 88
    Subject 5: 76

    --- Student Result ---
    Name: Rahul
    Roll Number: 10
    Total Marks: 419.00
    Average Marks: 83.80




## NAME: Vishnu Rathan B
# REG NO:212224240185

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


