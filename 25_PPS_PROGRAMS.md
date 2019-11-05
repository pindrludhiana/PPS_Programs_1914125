
<strong>PPS Programs</strong>.

<strong>01.Adding 2 Integers </strong>.

<strong>02.Average Of N Numbers</strong>.

<strong>03.Days Of Week</strong>.

<strong>04.Finding Odd Or Even</strong>.

<strong>05.Table Using For Loop</strong>.

<strong>06.Armstrong Number</strong>.

<strong>07.Calculator</strong>.

<strong>08.Bubble Sort</strong>.

<strong>09.Binary Search</strong>.

<strong>10.Factorial Of A Number</strong>.

<strong>11.Fizz Buzz</strong>.

<strong>12.Sum of First 100 Numbers</strong>.

<strong>13.Greater Of 2 Numbers</strong>.

<strong>14.Greater Of 3 Numbers </strong>.

<strong>15.GCD Of Numbers </strong>.

<strong>16.Leap Year Or Not </strong>.

<strong>17.Linear Search</strong>.

<strong>18.Matrix Addition</strong>.

<strong>19.Transpose Of Matrix</strong>.

<strong>20.Sum Of Digit Of Number</strong>.

<strong>21.Palindrome Number</strong>.

<strong>22.Call By Value </strong>.

<strong>23.Call By Reference </strong>.

<strong>24.Employees Details</strong>.

<strong>25.Product Of 2 Fractions</strong>..



# PROGRAM CODES:

## 01.Adding 2 Integers:

#include <stdio.h>

int main()

{
    
    int first, second, sum;

    printf("Enter two integers to add\n");

    scanf("%d%d", &first, &second);

    sum = first + second ;

    printf("Sum of entered numbers = %d\n",sum);

    return 0;
}



### Output:
 

 Enter two integers to add

 4

 5

 Sum of entered numbers = 9



## -----------------------------


## 02.Average Of N Numbers:

#include <stdio.h>

int main()

{

    int n, i;

    float num[100], sum = 0.0, average;

    printf("Enter the numbers of elements: ");

    scanf("%d", &n);

    while (n > 100 || n <= 0)

    {
        printf("Error! number should in range of (1 to 100).\n");
        printf("Enter the number again: ");
        scanf("%d", &n);
    }
    for(i = 0; i < n; ++i)
    {
        printf("%d. Enter number: ", i+1);

        scanf("%f", &num[i]);

        sum += num[i];

    }

    average = sum / n;

    printf("Average = %.2f", average);

    return 0;

}

### Output:

 Enter the numbers of elements:6

1. Enter number: 45.3
2. Enter number: 67.5
3. Enter number: -45.6
4. Enter number: 20.34
5. Enter number: 33
6. Enter number: 45.6

 Average =  27.69



## -----------------------------


## 03.Days Of Week:

#include <stdio.h>

 int main()

 {

     int week; 

     printf("Enter week number(1-7): "); 

     scanf("%d", &week);

     switch(week)

     { 
        case 1: printf("Monday"); 
        break; 
        case 2: printf("Tuesday"); 
        break; 
        case 3: printf("Wednesday"); 
        break; 
        case 4: printf("Thursday"); 
        break; 
        case 5: printf("Friday"); 
        break; 
        case 6: printf("Saturday");
        break;
        case 7: printf("Sunday"); 
        break;

        default: printf("Invalid input! Please enter week number between 1-7.");
     } 

     return 0; 

 }

### Output:
Enter week number(1-7): 7
Sunday



## -----------------------------


## 04.Finding Odd Or Even:

#include <stdio.h>

 int main()

{

     int n;

     printf("Enter an integer\n");

     scanf("%d",&n);

     if ( n%2 == 0 )

     printf("Even\n");

     else

     printf("Odd\n");

     return 0;
}

### Output:

Enter an integer

45

Odd



## -----------------------------


## 05.Table Using For Loop:

#include <stdio.h>

int main()

{

        int n, i;

        printf("Enter an integer: ");

        scanf("%d",&n);

        for(i=1; i<=10; ++i)

    {

        printf("%d * %d = %d \n", n, i, n*i);

    }
    
    return 0;

}


### Output:

Enter an integer: 9

9 * 1 = 9

9 * 2 = 18

9 * 3 = 27

9 * 4 = 36

9 * 5 = 45

9 * 6 = 54

9 * 7 = 63

9 * 8 = 72

9 * 9 = 81

9 * 10 = 90




## -----------------------------


## 06.Armstrong Number:

#include<stdio.h>

int main()

{

               int sum=0,digit;

               int n, temp;

               printf("enter any positive integer number");

               scanf("%d",&n);

               temp=n;
   
               while(temp>0)
  
        {

               digit=temp%10;

               temp/=10;

               sum=sum+digit*digit*digit;

        }

               if(n==sum)

               printf("\n %d is a armstrong number\n",n);

               else

               printf("\n %d is not a armstrong number\n",n);

               return 0;


}


### Output:

enter any positive integer number

153     

153 is a armstrong number



## -----------------------------


## 07.Calculator:

#include <stdio.h>

int main() 

{

    char operator;

    double firstNumber,secondNumber;

    printf("Enter an operator (+, -, *,): ");

    scanf("%c", &operator);

    printf("Enter two operands: ");

    scanf("%lf %lf",&firstNumber, &secondNumber);

    switch(operator)

    {

        case '+':

            printf("%.1lf + %.1lf = %.1lf",firstNumber, secondNumber, firstNumber + secondNumber);
            
            break;

            case '-':

            printf("%.1lf - %.1lf = %.1lf",firstNumber, secondNumber, firstNumber - secondNumber);
            
            break;

            case '*':

            printf("%.1lf * %.1lf = %.1lf",firstNumber, secondNumber, firstNumber * secondNumber);
            
            break;

            case '/':

            printf("%.1lf / %.1lf = %.1lf",firstNumber, secondNumber, firstNumber / secondNumber);
            
            break;
        
           default:

            printf("Error! operator is not correct");

    }

    
            return 0;
}

### Output:

Enter an operator (+, -, *,): *

Enter two operands: 1.5

4.5

1.5 * 4.5 = 6.8



## -----------------------------

## 08.Bubble Sort:

#include <stdio.h>
 
int main()

{

       int array[100], n, c, d, swap;

 
       printf("Enter number of elements\n");


       scanf("%d", &n);

 
       printf("Enter %d integers\n", n);

 
       for (c = 0; c < n; c++)


       scanf("%d", &array[c]);

 
       for (c = 0 ; c < n - 1; c++)

      {

       for (d = 0 ; d < n - c - 1; d++)

    {

      if (array[d] > array[d+1]) /* For decreasing order use < */

      {

        swap       = array[d];

        array[d]   = array[d+1];

        array[d+1] = swap;

      }

    }

     }
 
       printf("Sorted list in ascending order:\n");
 
       for (c = 0; c < n; c++)

       printf("%d\n", array[c]);
 
       return 0;

}

### Output:

Enter number of elements
6

Enter 6 integers

2

-4

7

8

4

7

Sorted list in ascending order:

-4

2

4

7

7

8



## -----------------------------
