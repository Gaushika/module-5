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
```

#include <stdio.h>

int main() {
    float l, b, a;
    float *ptrL = &l;
    float *ptrB = &b;

    printf("Enter length of the rectangle: ");
    scanf("%f", ptrL);

    printf("Enter breadth of the rectangle: ");
    scanf("%f", ptrB);

    a = (*ptrL) * (*ptrB);

    printf("Area of the rectangle = %.2f\n", a);

    return 0;
}



```
## OUTPUT
	<img width="531" height="316" alt="image" src="https://github.com/user-attachments/assets/0afaae24-ab8e-4dad-befe-2db2608ab849" />
	       	


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
```
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {
    char *str;
    int length;

    char input[] = "WELCOME";
    length = strlen(input) + 1;

    str = (char *)malloc(length * sizeof(char));

    if (str == NULL) {
        printf("Memory allocation failed.\n");
        return 1;
    }

    strcpy(str, input);

    printf("The string is: %s\n", str);

    free(str);

    return 0;
}


```
## OUTPUT

<img width="488" height="271" alt="image" src="https://github.com/user-attachments/assets/47641594-8e6c-4a0a-9ed6-45e7894e1d2f" />


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
```
#include <stdio.h>

struct student {
    char name[50];
    int roll;
    float marks;
};

int main() {
    struct student s;

    printf("Enter student name: ");
    scanf(" %[^\n]", s.name);

    printf("Enter roll number: ");
    scanf("%d", &s.roll);

    printf("Enter marks: ");
    scanf("%f", &s.marks);

    printf("\nStudent Information:\n");
    printf("Name: %s\n", s.name);
    printf("Roll Number: %d\n", s.roll);
    printf("Marks: %.2f\n", s.marks);

    return 0;
}


```

## OUTPUT
<img width="695" height="466" alt="image" src="https://github.com/user-attachments/assets/6fcef7a1-f627-4c23-ac7a-300ce1ee4c3a" />


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
```
#include <stdio.h>

struct employee {
    char name[50];
    int id;
    float basic, hra, da, gross;
};

int main() {
    struct employee emp[3];
    int i;

    for (i = 0; i < 3; i++) {
        printf("Enter details of employee %d:\n", i + 1);

        printf("Name: ");
        scanf(" %[^\n]", emp[i].name);

        printf("ID: ");
        scanf("%d", &emp[i].id);

        printf("Basic Salary: ");
        scanf("%f", &emp[i].basic);

        printf("HRA: ");
        scanf("%f", &emp[i].hra);

        printf("DA: ");
        scanf("%f", &emp[i].da);

        emp[i].gross = emp[i].basic + emp[i].hra + emp[i].da;

        printf("\n");
    }

    printf("Employee Details with Gross Salary:\n");
    for (i = 0; i < 3; i++) {
        printf("Employee %d:\n", i + 1);
        printf("Name: %s\n", emp[i].name);
        printf("ID: %d\n", emp[i].id);
        printf("Gross Salary: %.2f\n\n", emp[i].gross);
    }

    return 0;
}


```

 ## OUTPUT
<img width="512" height="808" alt="image" src="https://github.com/user-attachments/assets/cbb1e973-95be-45e8-a1b5-e92d5300955b" />

 

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
```
#include <stdio.h>

struct student {
    char name[10];
    int rollno;
    int subject[5];
    int total;
};

int main() {
    struct student s[2];
    int i, j;

    for (i = 0; i < 2; i++) {
        printf("Enter marks for student %d:\n", i + 1);
        s[i].total = 0;
        for (j = 0; j < 5; j++) {
            printf("Subject %d: ", j + 1);
            scanf("%d", &s[i].subject[j]);
            s[i].total += s[i].subject[j];
        }
    }

    for (i = 0; i < 2; i++) {
        printf("Total marks of student %d = %d\n", i + 1, s[i].total);
        printf("Average marks of student %d = %.2f\n", i + 1, s[i].total / 5.0);
    }

    return 0;
}


```

## OUTPUT

 <img width="513" height="685" alt="image" src="https://github.com/user-attachments/assets/2e693942-e9cd-4f80-ab17-08d1cabf7872" />


## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


