# EX-11-EMI-CALCULATOR

## AIM

To write a program to prepare EMI calculator using function without return type and with arguments.

## ALGORITHM

1.	Start the program.
2.	Read principal amount, rate of interest and months.
3.	Pass these values as arguments to function.
4.	Calculate EMI using the formula, amt=(prpow(1+r,t))/(pow(1+r,t)-1)
5.	Display the result.
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <math.h>

void calculateEMI(float principal, float rate, int months) 
{
    float r = rate / (12 * 100);  
    float emi;
    float year = months*12;
    float powVal = pow(1 + r, year);

    emi = (principal * r * powVal) / (powVal - 1);

    printf("Monthly EMI is: %.2f\n", emi);
}

int main() 
{
    float principal, rate;
    int months;

    printf("Enter principal amount: ");
    scanf("%f", &principal);

    printf("Enter annual rate of interest (in %%): ");
    scanf("%f", &rate);

    printf("Enter loan duration in years: ");
    scanf("%d", &months);

    calculateEMI(principal, rate, months);

    return 0;
}
```

## OUTPUT

<img width="658" height="201" alt="image" src="https://github.com/user-attachments/assets/973311b8-13a8-48af-8e0a-74faaec8c444" />


## RESULT

Thus the program to prepare EMI calculator using function without return type with arguments has been executed successfully
 
 

# EX-12-FIBONACCI-SERIES
## AIM
To write a C program to generate the Fibonacci series for the value 6.

## ALGORITHM
1.	Start the program.
2.	Read number of terms to display.
3.	Add the previous two terms and store it in new term.
4.	Assign 2nd term to 1st term and 3rd term to 2nd term.
5.	Repeat steps 3 and 4 n number of times.
6.	Display the result.
7.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() 
{
    int n = 6;
    int t1 = 0, t2 = 1, nextTerm;
    int i;

    printf("Fibonacci Series for %d terms:\n", n);

    for (i = 1; i <= n; ++i) 
	{
        if (i == 1)
            printf("%d ", t1);
        else if (i == 2)
            printf("%d ", t2);
        else 
		{
            nextTerm = t1 + t2;        
            printf("%d ", nextTerm);   
            t1 = t2;                   
            t2 = nextTerm;             
        }
    }

    printf("\n");  // Newline after series output
    return 0;      // Step 7: End the program
}
```
## OUTPUT
<img width="677" height="151" alt="image" src="https://github.com/user-attachments/assets/bcff1bde-dd57-44eb-97d4-cb1bf7e03baa" />

## RESULT
Thus the program to generate the Fibonacci series for the value 6 has been executed successfully.
 
 


# EX-13-ONE-DIMENSIONAL-ARRAY
## AIM
To write a C program to read n elements as input and print the last element of the array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	Print the last element.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() 
{
    int n, i;
    
	printf("Enter number of elements: ");
    scanf("%d", &n);

    int arr[n];  

    printf("Enter %d elements:\n", n);
    for(i = 0; i < n; i++) 
	{
        scanf("%d", &arr[i]);
    }

  
    printf("Last element of the array is: %d\n", arr[n-1]);

   
    return 0;
}
```
## OUTPUT

<img width="665" height="207" alt="image" src="https://github.com/user-attachments/assets/469e7fd7-f0f7-41c6-b1a4-a8b7e3449525" />

## RESULT
Thus the program to read n elements as input and print the last element of the array has been executed successfully.
 
 


# EX-14-POSITIVE-ARRAY-ELEMENTS
## AIM
To write a C Program to count total number of positive elements in an array.

## ALGORITHM
1.	Start the program.
2.	Read a variable.
3.	Read the array values n number of times.
4.	If the array value can be divided by 2 then increment count by 1.
5.	Display result.
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int n, i, count = 0;
   
    printf("Enter the number of elements: ");
    scanf("%d", &n);

    int arr[n];

    printf("Enter %d elements:\n", n);
    for(i = 0; i < n; i++)
	{	
        scanf("%d", &arr[i]);
    }

    for(i = 0; i < n; i++)
	{
        if(arr[i] > 0)
		{
            count++;
        }
    }

   
    printf("Total number of positive elements: %d\n", count);

    return 0;
}
```

## OUTPUT
<img width="664" height="201" alt="image" src="https://github.com/user-attachments/assets/52f02138-1269-4184-a185-ad32c0d571b9" />

## RESULT
Thus the program to count total number of positive elements in an array has been executed successfully.


# EX -15 - Replace All Even Elements With 'E' In One Dimensional Array

## Aim:
To write a C program to replace all even elements with 'E' in one dimensional array

## Algorithm:
1.	Input the array:
  Read the size of the array.
  Input the elements of the array.
2.	Iterate through the array:
 	For each element of the array, check if the element is even (i.e., if the element modulo 2 equals 0).
3.	Replace even elements with 'E':
     If an element is even, replace that element with the character 'E'.
4.	Output the updated array:
 Print the updated array after replacements.

## Program:
```
#include <stdio.h>

int main() {
    int n, i;

    printf("Enter the size of the array: ");
    scanf("%d", &n);

   
    int arr[n];
    char result = 'E';  
    
    printf("Enter %d elements:\n", n);
    for(i = 0; i < n; i++) 
	{
        scanf("%d", &arr[i]);
    }

    printf("Updated array:\n");
    for(i = 0; i < n; i++) 
	{
        if(arr[i] % 2 == 0) 
		{
            printf("%c ",result);
        }
		else 
		{
            printf("%d ", arr[i]);  
        }
    }
    printf("\n");

    return 0;
}
```
## Output:
<img width="665" height="217" alt="image" src="https://github.com/user-attachments/assets/bb39fdd1-651a-48e3-bad9-9becfeab5ee9" />


## Result:

Thus, the program to replace all even elements with 'E' in one dimensional array was verified successfully.



