
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




