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
    int l, b, *p, *q;
    scanf("%d%d", &l, &b);
    p = &l;
    q = &b;
    printf("%d", (*p) * (*q));
    return 0;
}

```
## OUTPUT
		       	
![Screenshot 2025-05-17 163218](https://github.com/user-attachments/assets/3ad9a30c-6e8d-436e-9a8b-b168379f3ded)


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
    char *s = (char *)malloc(10 * sizeof(char));
    strcpy(s, "WELCOME");
    printf("%s", s);
    free(s);
    return 0;
}

```
## OUTPUT

![Screenshot 2025-05-17 163447](https://github.com/user-attachments/assets/f08c3e5b-92af-41a5-95dd-f8e36a98aa81)

## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully.



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

struct s {
    char n[20];
    int r;
    float m;
};

int main() {
    struct s a;
    scanf("%s %d %f", a.n, &a.r, &a.m);
    printf("%s %d %.2f", a.n, a.r, a.m);
    return 0;
}

```
## OUTPUT

![Screenshot 2025-05-17 163658](https://github.com/user-attachments/assets/36e259ae-d9ce-40df-b617-7a054702692e)

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

struct e {
    char n[20];
    int i;
    float b, g;
};

int main() {
    struct e a[3];
    int j;
    for(j=0; j<3; j++)
        scanf("%s %d %f", a[j].n, &a[j].i, &a[j].b);
    for(j=0; j<3; j++) {
        a[j].g = a[j].b + 0.2 * a[j].b + 0.1 * a[j].b;
        printf("%s %d %.2f\n", a[j].n, a[j].i, a[j].g);
    }
    return 0;
}

```
 ## OUTPUT

 ![Screenshot 2025-05-17 163925](https://github.com/user-attachments/assets/06167440-e5ad-4918-a705-f6d660569b86)


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
    float avg;
};

int main() {
    struct student s[2];
    int i, j;

    for(i = 0; i < 2; i++) {
        scanf("%s %d", s[i].name, &s[i].rollno);
        s[i].total = 0;
        for(j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
            s[i].total += s[i].subject[j];
        }
        s[i].avg = s[i].total / 5.0;
    }

    for(i = 0; i < 2; i++) {
        printf("%s %d Total: %d Average: %.2f\n", s[i].name, s[i].rollno, s[i].total, s[i].avg);
    }

    return 0;
}

```

## OUTPUT

 ![Screenshot 2025-05-17 164151](https://github.com/user-attachments/assets/505764ff-c0ce-432c-912b-64aaeea3b60f)




## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


