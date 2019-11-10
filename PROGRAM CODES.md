 ***************************


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

* **_Output:_**
 

 Enter two integers to add
 4

 5

 Sum of entered numbers = 9



---------


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

* **_Output:_**

 Enter the numbers of elements:6

1. Enter number: 45.3
2. Enter number: 67.5
3. Enter number: -45.6
4. Enter number: 20.34
5. Enter number: 33
6. Enter number: 45.6

 Average =  27.69



--------


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

* **_Output:_**

Enter week number(1-7): 7

Sunday



----------


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

* **_Output:_**

Enter an integer

45

Odd



------------


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


* **_Output:_**

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




------------


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


* **_Output:_**

enter any positive integer number

153     

153 is a armstrong number



 -----------------------------


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

* **_Output:_**

Enter an operator (+, -, *,): *

Enter two operands: 1.5

4.5

1.5 * 4.5 = 6.8



-----------------------------

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

* **_Output:_**

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



-----------------------------


## 09.Binary Search:

#include<stdio.h>
        
int check(int b[],int m,int o)

{       

        int p=-1,mid;

        int f=1,l=m;

        mid=(f+l)/2;           

        while(f<=l)

     {

        mid=(f+l)/2;

        if(b[mid]==o)

        {

                p=mid;

                break;

        }

        else if(o>b[mid])

        {

                f=mid+1;

        }

        else if (o<b[mid])

        {

                l=mid-1;

        }

        
        }       

                        return p;

        
        }     

       
        void main()

        {     
  
        int n,num,index;

        printf("enter the array size\n");

        scanf("%d",&n);

        int a[n];

        printf("enter the array elements in assending order\n");

        for(int i=1;i<=n;i++)

        {

                scanf("%d",&a[i]);

        }

        printf("now enter the number which you want to check\n whether it is present or not in entered array\n");
        
       
        scanf("%d",&num);

        index=check(a,n,num);

        if(index==-1)   

        printf("element is not found\n");

        else

        printf("element is found at the position %d \n",index);

}


* **_Output:_**

enter the array size

8       

enter the array elements in assending order

1       

2               

3       

4       

5       

6       

7       

8       

now enter the number which you want to check

 whether it is present or not in entered array

6       

element is found at the position 6



 -----------------------------


## 10.Factorial Of A Number:


#include <stdio.h>

long factorial(int);

int main()

{

       int number;

       long fact = 1;

       printf("Enter a number to calculate it's factorial\n");

       scanf("%d", &number);

       printf("%d! = %ld\n", number, factorial(number));

       return 0;

     }

       long factorial(int n)

     {

       int c;

       long result = 1;

       for (c = 1; c <= n; c++)

       result = result * c;
    
       return result;

}

* **_Output:_**

Enter a number to calculate it's factorial

6

!6 = 720



 -----------------------------


## 11.FizzBuzz:

#include<stdio.h>

int main()

    { 

    for(int i=1;i<=30;i++) 

        { if(i%15==0) 

        printf("fizzbuzz\n"); 

        else if(i%5==0) 

        printf("buzz\n"); 

        else if(i%3==0) 

        printf("fizz\n"); 

        else {printf("%d\n",i);

            } 

        } 

    return 0;
}

* **_Output:_**

1      
                
2                
               
fizz                    



 -----------------------------


## 12.Sum of First 100 Numbers:

#include <stdio.h>

int main()

{

    int n, i, sum = 0;
    
    printf("Enter a positive integer: ");

    scanf("%d",&n);

    for(i=1; i <= n; ++i)

    {

        sum += i;   // sum = sum+i;

    }

    printf("Sum = %d",sum);

    return 0;

}
 

* **_Output:_**

Enter a positive integer: 100

Sum = 5050



 -----------------------------


## 13.Greater Of 2 Numbers:

#include<stdio.h>

void main()

{       

        float a,b;

        printf("enter first number\n");

        scanf("%f",&a);

        printf("enter the second nummber\n");

        scanf("%f",&b);

        if(a>b)

                printf("%f is greater\n",a);

        else if(b>a)

                printf("%f is greater\n",b);

        else    

                printf("both numbers are equal\n");

}

* **_Output:_**

enter first number

3           

enter the second nummber

3

both numbers are equal



 -----------------------------


## 14.Greater Of 3 Numbers:

#include<stdio.h>

void main()

{

     int a,b,c;

     printf("enter the three numbers which you want to compare \n");

     scanf("%d%d%d",&a,&b,&c);

     if(a>b&&a>c)

     printf("\n%d is the greatest number\n",a);

     else if(b>a&&b>c)

     printf("\n%d is the greatest number\n",b);

     else 

     printf("\n%d is the greatest number\n",c);

}


* **_Output:_**

enter the three numbers which you want to compare 

1

13

8

13 is the greatest number




-----------------------------



## 15.GCD Of Numbers:

#include<stdio.h>

int main()
{

     int m,n,r=1;

     printf("\n Enter value for m,n\n");

     scanf("%d%d",&m,&n);

     while(r!=0)

    {

     r=n%m;

     n=m;

     m=r;

    }

     printf("\n GCD=%d \n",n);

     return 0;

}

* **_Output:_**

Enter value for m,n

12 14

GCD=2




-----------------------------


## 16.Leap Year Or Not:

#include<stdio.h>

int main()

{
        int a;

        printf("enter the year\n");

        scanf("%d",&a);

        if(a%4==0)

        printf("it is a leap year\n");

        else

                printf("it is not a leap year\n");

}

* **_Output:_**

--------------------------------------------------------

enter the year  

2019

it is not a leap year

**____________**

enter the year

2020

it is a leap year

**____________**




 -----------------------------


## 17.Linear Search:

#include <stdio.h>

int main()

{

      int array[100], search, c, n;

      printf("Enter the number of elements in array\n");

      scanf("%d",&n);

      printf("Enter %d integer(s)\n", n);

      for (c = 0; c < n; c++)

      scanf("%d", &array[c]);

      printf("Enter the number to search\n");

      scanf("%d", &search);


      for (c = 0; c < n; c++)

      {
  
      if (array[c] == search)

      {


      printf("%d is present at location %d.\n", search, c+1);

      break;

      }

      }

      if (c == n)

      printf("%d is not present in array.\n", search);

      return 0;
}

* **_Output:_**

Enter the number of elements in array

5

Enter 5 numbers

5

6

4

2

9
Enter the number to search

4 is present at location 3.



-----------------------------


## 18.Matrix Addition:

#include <stdio.h>

int main()

{

          int m, n, c, d, first[10][10], second[10][10], sum[10][10];


          printf("Enter the number of rows and columns of matrix\n");

          scanf("%d%d", &m, &n);

          printf("Enter the elements of first matrix\n");

          for ( c = 0 ; c < m ; c++ )

          for ( d = 0 ; d < n ; d++ )

          scanf("%d", &first[c][d]);

          printf("Enter the elements of second matrix\n");

          for ( c = 0 ; c < m ; c++ )

          for ( d = 0 ; d < n ; d++ )

          scanf("%d", &second[c][d]);

          for ( c = 0 ; c < m ; c++ )

          for ( d = 0 ; d < n ; d++ )

          sum[c][d] = first[c][d] + second[c][d];

          printf("Sum of entered matrices:-\n");

          for ( c = 0 ; c < m ; c++ )

          {

          for ( d = 0 ; d < n ; d++ )

          printf("%d\t", sum[c][d]);

          printf("\n");

          }

          return 0;
}

* **_Output:_**

Enter the number of rows and columns of matrix

2

2

Enter the elements of first matrix

1 2

3 4

Enter the elements of second matrix

5 6

2 1

Sum of entered matrices:-

6 8

5 5



 -----------------------------


## 19.Transpose Of Matrix:


#include <stdio.h>

int main()

{

         int m, n, c, d, matrix[10][10], transpose[10][10];

         printf("Enter the number of rows and columns of matrix \n ");

         scanf("%d%d",&m,&n); printf("Enter the elements of matrix \n");

         for( c = 0 ; c < m ; c++ )

         {

         for( d = 0 ; d < n ; d++ )

         {

         scanf("%d",&matrix[c][d]);

         }

         }

         for( c = 0 ; c < m ; c++ )

         {

         for( d = 0 ; d < n ; d++ )

         {

         transpose[d][c] = matrix[c][d];

         }

         }

         printf("Transpose of entered matrix :-\n");

         for( c = 0 ; c < n ; c++ )

         {

         for( d = 0 ; d < m ; d++ )

         {
         printf("%d\t",transpose[c][d]);

         }

         printf("\n");

         }

         return 0;

}

* **_Output:_**

Enter the number of rows and columns of matrix

2

3

Enter the elements of matrix

1 2 3

4 5 6

Transpose of entered matrix :-

1  4

2  5

3  6



 -----------------------------


## 20.Sum Of Digit Of Number:

  
#include<stdio.h>

int main()

{

        int a,sum=0,c;

        printf("enter the number\n");

        scanf("%d",&a);

        while(a!=0)

        {

        c=a%10;

        sum+=c;

        a=a/10;

        }

        printf("sum of digits is %d\n",sum);

}


* **_Output:_**

enter the number

265      

sum of digits is 13




 -----------------------------


## 21.Palindrome Number:

#include <stdio.h>

int main()

{

       int n, reverse = 0, temp;

       printf("Enter a number to check if it is a palindrome or not\n");

       scanf("%d",&n);

       temp = n;

       while( temp != 0 )

       {

       reverse = reverse * 10;

       reverse = reverse + temp%10;

       temp = temp/10;

       }


       if ( n == reverse )

       printf("%d is a palindrome number.\n", n);

       else

       printf("%d is not a palindrome number.\n", n);

       return 0;

}

* **_Output:_**

Enter a number to check if it is a palindrome or not

12321

12321 is a palindrome number




 -----------------------------


## 22.Call By Value:

#include <stdio.h>
 
int main()

{

      int x, y, t;
 
      printf("Enter two integers\n");

      scanf("%d%d", &x, &y);
 
      printf("Before Swapping\nFirst integer = %d\nSecond integer = %d\n", x, y);
  
      t = x;

      x = y;

      y = t;
 
      printf("After Swapping\nFirst integer = %d\nSecond integer = %d\n", x, y);
  
      return 0;

}

* **_Output:_**

Enter two integers                                                                                                                              
12                                                                                                                                       
13                                                                                                                                      
Before Swapping                                                                                                                                 
First integer = 12                                                                                                                         
Second integer = 13                                                                                                                          
After Swapping                                                                                                                                  
First integer = 13                                                                                                                          
Second integer = 12




 -----------------------------

## 23.Call By Reference:

#include <stdio.h>

         void call_by_reference(int *y) {

         printf("Inside call_by_reference y = %d before adding 10.\n", *y);

         (*y) += 10;

         printf("Inside call_by_reference y = %d after adding 10.\n", *y);

         }

         int main() {

         int b=10;

         printf("b = %d before function call_by_reference.\n", b);

         call_by_reference(&b);

         printf("b = %d after function call_by_reference.\n", b);

         return 0;

}

* **_Output:_**

b = 10 before function call_by_reference.

Inside call_by_reference y = 10 before adding 10.

Inside call_by_reference y = 20 after adding 10.

b = 20 after function call_by_reference



-----------------------------


## 24.Employees Details:

  
#include <stdio.h>
 

        struct employee{

        char    name[30];

        int     empId;

        float   salary;

        };
 
        int main()

        {
    
        struct employee emp;
     
    
        printf("\nEnter details :\n");

        printf("Name ?:");          gets(emp.name);

        printf("ID ?:");            scanf("%d",&emp.empId);

        printf("Salary ?:");        scanf("%f",&emp.salary);
     
   
       printf("\nEntered detail is:");

       printf("Name: %s"   ,emp.name);

       printf("Id: %d"     ,emp.empId);

       printf("Salary: %f\n",emp.salary);

      return 0;

}

* **_Output:_**

Enter details :

Name ? :Bhupinder

ID ? :1914125

Salary ?:15,00000000

Entered detail is:

Name: Bhupinder

Id: 1914125

Salary: 15,000000



 -----------------------------


## 25.Product Of 2 Fractions:

#include<stdio.h>

       struct fraction

       {
       int num;

       int den;

       };

       int main()

       {

       int rnum,rden;

       struct fraction f1,f2; 

       printf("enter numerator and denominator of first fraction\n");

       scanf("%d%d",&f1.num,&f1.den);

       printf("enter numerator and denominator of second fraction\n");

       scanf("%d%d",&f2.num,&f2.den); 

       rnum=f1.num*f2.num;

       rden=f1.den*f2.den;

       printf("\nproduct is : %d/%d\n",rnum,rden);

}

* **_Output:_**

enter numerator and denominator of first fraction

1 8



enter numerator and denominator of second fraction

1 8

product is :

1/64


***************************


