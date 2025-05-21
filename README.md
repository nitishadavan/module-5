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
# include <stdio.h>
int calc(float *l ,float *w,float *area)
{
    *area=(*l)*(*w);
    return 0;
}
int main()
{
    float l,w,area;
    scanf("%f %f",&l,&w);
    calc(&l,&w,&area);
    printf("Area of rectangle = %.6f sq. units",area);
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/8c4e0d1e-25aa-4ff2-81a0-c2ce39a3638e)
		       	
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
#include<string.h>
#include<stdlib.h>
int main()
{
    char*p;
    p=(char *)malloc(sizeof(char));
    strcat(p,"WELCOME");
   
    printf("%s",p);
    free(p);
}
```
## OUTPUT
![image](https://github.com/user-attachments/assets/9ceae7c5-b51b-4fd3-8f88-4f4119649d88)

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
```
# include <stdio.h>
struct stud
{
    char name[50];
    int roll;
    float marks;
}stud;
int main()
{
   
    scanf("%s",stud.name);
    scanf("%d",&stud.roll);
    scanf("%f",&stud.marks);
    printf("Displaying Information:\n");
    printf("Name: %s\n",stud.name);
    printf("Roll number: %d\n",stud.roll);
    printf("Marks: %.1f\n",stud.marks);
    return 0;
}
```

## OUTPUT

![image](https://github.com/user-attachments/assets/151defcf-4015-4e1c-ac98-429238ae34e8)

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
# include <stdio.h>
struct emp
{
    int empno;
    char dept[50];
    int salary;
};
int main()
{
    struct emp arr[3];
    int da,hra;
    float gs;
    printf("Details of the Employee:\n");
    for(int i=0;i<3;i++)
    {
        scanf("%d\n%s\n%d",&arr[i].empno,arr[i].dept,&arr[i].salary);
        da=arr[i].salary/10;
        hra=arr[i].salary*3/10;
        gs=arr[i].salary+da+hra;
        printf("%d %s %d %d %d %.2f\n",arr[i].empno,arr[i].dept,arr[i].salary,da,hra,gs);
    }
    
}
```

## OUTPUT
![image](https://github.com/user-attachments/assets/394bfe0a-dd20-4aea-bfca-29049517e994)

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
#include<stdio.h>
struct student
{
    char name[10];//10 b
    int rollno;//4 b
    int subject[5],total;//24
};//38
int main()
{
    int a;
    scanf("%d",&a);
    struct student sri;
    for(int i=0;i<a;i++){
        sri.total=0;
        for(int j=0;j<5;j++){
            scanf("%d",&sri.subject[j]);
            sri.total+=sri.subject[j];
        }
        printf("%d\n",sri.total);
    }
}
```      

## OUTPUT
![image](https://github.com/user-attachments/assets/3c14d1a5-363a-403f-a32b-60bee89bbe7a)

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	
