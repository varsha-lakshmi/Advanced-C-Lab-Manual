EXP NO:6 C PROGRAM PRINT THE LOWERCASE ENGLISH WORD CORRESPONDING TO THE NUMBER
Aim:
To write a C program print the lowercase English word corresponding to the number
Algorithm:
1.	Start
- Initialize an integer variable n.
2.	Input Validation
3.	Switch Statement cases.
-	Case 5: Print "seventy one"
-	Case 6: Print "seventy two"
-	Case 13: Print "seventy three"
-	...
-	Case 13: Print "seventy nine"
-	Default: Print "Greater than 13"
4.	Exit the program.
 
Program:
```
#include <stdio.h>

int main()
{
    int n, i, digit;
    int freq[4] = {0, 0, 0, 0};

    for(i = 0; i < 10; i++)
    {
        scanf("%d", &n);

        while(n > 0)
        {
            digit = n % 10;

            if(digit >= 0 && digit <= 3)
                freq[digit]++;

            n = n / 10;
        }
    }

    for(i = 0; i < 4; i++)
    {
        printf("%d ", freq[i]);
    }

    return 0;
}
```

Output:

<img width="311" height="68" alt="image" src="https://github.com/user-attachments/assets/69bbeda0-dc4e-4bd1-a3a3-615458a943a7" />






Result:
Thus, the program is verified successfully
 
EXP NO:7 C PROGRAM TO PRINT TEN SPACE-SEPARATED INTEGERS     IN A SINGLE  LINE DENOTING THE FREQUENCY OF EACH DIGIT FROM 0 TO 3 .
Aim:
To write a C program to print ten space-separated integers in a single line denoting the frequency of each digit from 0 to 3.
Algorithm:
1.	Start
2.	Declare char array a[50] outer loop for each digit from 0 to 3
3.	Initialize counter c to 0
4.	For each character in the string print count c for current digit, followed by a space
5.	Increment h to move to the next digit
6.	End
 
Program:
```
#include <stdio.h>
#include <string.h>

void swap(char *a, char *b)
{
    char temp = *a;
    *a = *b;
    *b = temp;
}

void permute(char str[], int left, int right)
{
    int i;

    if(left == right)
    {
        printf("%s\n", str);
        return;
    }

    for(i = left; i <= right; i++)
    {
        swap(&str[left], &str[i]);
        permute(str, left + 1, right);
        swap(&str[left], &str[i]);
    }
}

int main()
{
    char str[20];

    printf("Enter a string: ");
    scanf("%s", str);

    permute(str, 0, strlen(str) - 1);

    return 0;
}

```


Output:


<img width="232" height="152" alt="image" src="https://github.com/user-attachments/assets/c6f0bc1f-2e49-4c03-aea5-4ac5ebcf87b7" />






Result:
Thus, the program is verified successfully

EXP NO:8 C PROGRAM TO PRINT ALL OF ITS PERMUTATIONS IN STRICT LEXICOGRAPHICAL ORDER.
Aim:
To write a C program to print all of its permutations in strict lexicographical order.

Algorithm:
1.	Start
2.	Declare variables s (pointer to an array of strings) and n (number of strings)

3.	Memory Allocation
Dynamically allocate memory for s to store an array of strings
4.	Input
Read the number of strings n from the user Dynamically allocate memory for each string in s
5.	Permutation Generation Loop
6.	Memory Deallocation
Free the memory allocated for each string in s Free the memory allocated for s
7.	End
 
Program:
```
#include <stdio.h>
#include <string.h>

void swap(char *a, char *b)
{
    char temp = *a;
    *a = *b;
    *b = temp;
}

void permute(char str[], int left, int right)
{
    int i;

    if(left == right)
    {
        printf("%s\n", str);
        return;
    }

    for(i = left; i <= right; i++)
    {
        swap(&str[left], &str[i]);
        permute(str, left + 1, right);
        swap(&str[left], &str[i]);
    }
}

int main()
{
    char str[20];

    printf("Enter a string: ");
    scanf("%s", str);

    permute(str, 0, strlen(str) - 1);

    return 0;
}
```



Output:



<img width="237" height="146" alt="image" src="https://github.com/user-attachments/assets/c76cfd12-635b-44dd-b1f7-b35c81af829a" />






Result:
Thus, the program is verified successfully
 
EXP NO:9 C PROGRAM PRINT A PATTERN OF NUMBERS FROM 1 TO N AS
SHOWN BELOW.
Aim:
To write a C program to print a pattern of numbers from 1 to n as shown below.
Algorithm:
1.	Start
2.	Declare integer variables n, i, j, min
3.	Read the value of n from the user
4.	Calculate the length of the side of the square matrix: len = n * 2 - 1
5.	Matrix Generation Loop
6.	Calculate min as the minimum distance to the borders
7.	End
 
Program:

```
#include <stdio.h>

int main()
{
    int n, i, j, min, len;

    printf("Enter the value of n: ");
    scanf("%d", &n);

    len = n * 2 - 1;

    for(i = 0; i < len; i++)
    {
        for(j = 0; j < len; j++)
        {
            min = i;

            if(j < min)
                min = j;

            if(len - 1 - i < min)
                min = len - 1 - i;

            if(len - 1 - j < min)
                min = len - 1 - j;

            printf("%d ", n - min);
        }

        printf("\n");
    }

    return 0;
}
```

Output:

<img width="383" height="222" alt="image" src="https://github.com/user-attachments/assets/e81b6db1-795d-4d27-b8b8-07c725ff04ba" />






Result:
Thus, the program is verified successfully

EXP NO:10 C PROGRAM TO FIND A SQUARE  OF NUMBER USING FUNCTION WITHOUT ARGUMENTS WITH RETURN TYPE

Aim:

To write a C program that calculates the square of a number using a function that does not take any arguments, but returns the square of the number.

Algorithm:

1.	Start.
2.	Define a function square() with no parameters. This function will return an integer value.
3.	Inside the function:
o	Declare an integer variable to store the number.
o	Ask the user to input a number.
o	Calculate the square of the number (multiply the number by itself).
o	Return the squared value.
4.	In the main function:
o	Call the square() function and display the result.
5.	End.

Program:

```
#include <stdio.h>

int square()
{
    int n;

    printf("Enter a number: ");
    scanf("%d", &n);

    return n * n;
}

int main()
{
    int result;

    result = square();

    printf("Square = %d", result);

    return 0;
}
```



Output:



<img width="313" height="60" alt="image" src="https://github.com/user-attachments/assets/5aaf6438-edf7-42a6-a7b7-b339f48b88fd" />



Result:
Thus, the program is verified successfully



























