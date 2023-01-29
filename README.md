 FM_Codes        




Question 1.
#include<stdio.h>
#include<stdlib.h>
int main()
{
    printf("*\n\n**\n\n***\n\n****\n\n*****\n\n"); // \n here means print on new line
    return 0;
}



Question 2.
#include<stdio.h>
#include<stdlib.h>
int main()
{
    int number;
    char character;
    char string[100];  // This is an array of characters which is also known as string.
    double x;

    printf("Enter a number.\n");
    scanf(" %d", &number);     // Taking user inputs 
    printf("%d", number);

    printf("\nEnter a character.\n");
    scanf(" %c", &character);
    printf("%c", character);

    printf("\nEnter a string.\n");
    scanf(" %s", string);
    printf("%s", string);

    printf("\nEnter a number.\n");
    scanf(" %lf", &x);
    printf("%.2lf", x);

    return 0;

}


Question 3.
#include<stdio.h>
#include<stdlib.h>
int main()
{
    int a;
    printf("No of rows(upto 5): \n");
    scanf("%d", &a);

    if(a==1){      // Using if statements to jump to different cases which depends on user input.
        printf("*");
    }

    if(a==2){
        printf("* \n");
        printf("**");
    }

    if(a==3){
        printf("* \n");
        printf("** \n");
        printf("***");
    }

    if(a==4){
        printf("* \n");
        printf("** \n");
        printf("*** \n");
        printf("**** \n");
    }

    if(a==5){
        printf("* \n");
        printf("** \n");
        printf("*** \n");
        printf("**** \n");
        printf("*****");
    }
    
    return 0;
}



Question 4.
#include<stdio.h>
#include<stdlib.h>
#include<ctype.h>
#include<math.h>
#include<string.h>
int main()
{
    char str[100];
    int i,count = 0;
    printf("Enter a word \n"); //Taking user input.
    scanf("%s",str);
    for(i = 0; str[i] != '\0'; i++) //Using for loop for iterating different elements in the word
    {
        
        if( str[i] == 'a' ||
            str[i] == 'e' ||
            str[i] == 'i' || 
            str[i] == 'o' || 
            str[i] == 'u'    )
        {
            count++;               // For every satisfaction of the above if statements the count of vowel is incremented by 1. 
                                   // Here count++= count+1
        }
    }
    printf("vowel count = %d\n",count);
    
    return 0;
}




Question 5. a)
#include<stdio.h>
#include<stdlib.h>
int main()
{
    int n;
    int temp;
    printf("How many elements do you want in the array?\n");
    scanf(" %d", &n);      //Taking user input for how much elements he wants
    
    int array[n];
    for(int i=0; i < n; i++) // Using this loop will iterate for whatever times user has gave input. 
    {
        printf("array[%d]= ", i);
        scanf(" %d", &array[i]);
    }
    for(int i=0; i<n; i++)    //Implementing bubble sort here.
    {
        for(int j=0; j<n-1; j++)
        {
            if(array[j]>array[j+1])
            {
                temp = array[j];
                array[j]=array[j+1];
                array[j+1]=temp;
            }

        }
        printf("%d", array[i]);
    }
    return 0;
}


Question 5.b)
int main()
{
    int i, array[i], temp, n;
     for(int i=0; i<n-1; i++)    //Here we are implementing selection sort
    {
        int min = i;
        for(int j=i+1; j<n; j++)
        {
            if(array[j]<array[min])
            {
                min=j;
            }
            if(min!=i)
            {
                temp = array[i];
                array[i]=array[i+1];
                array[i+1]=temp;
                
            }
        }
        printf("%d", array[i]);
    }
    return 0;
}



Question 6.
#include<stdio.h>
#include<stdlib.h>
#include<ctype.h>
#include<math.h>
#include<string.h>
int main()
{
    double x;
    double y;
    double a, b, c;
    char operator;
    printf("Please enter which operation you want to execute(+,-,*,/,p,t). Here p stands for power and t for trigonometric function \n");
    scanf("%c", &operator);

    printf("Enter first value and second value(For power: first value is base and second value is power ; For trigonometry only first value) \n");
    scanf("%lf \t %lf", &x, &y);

    switch(operator)
    {
        case '+': a = x+y;
                  printf("Answer is : %.2lf", a);
                  break;
        case '-': a = x-y;
                  printf("Answer is : %.2lf", a);
                  break;
        case '*': a = x*y;
                  printf("Answer is : %.2lf", a);
                  break;
        case '/': a = x/y;
                  printf("Answer is : %.2lf", a);
                  break;
        case 'p': a = pow(x,y);
                  printf("Answer is : %.2lf", a);
                  break;
        case 't': a = sin(x);
                  b = cos(x);
                  c = tan(x);
                  printf("sin(%lf)= %lf \n", x,a);
                  printf("cos(%lf)= %lf \n", x,b);
                  printf("tan(%lf)= %lf \n", x,c);
                  break;
        default : printf("Please write a valid operator");
    }
    return 0;
}



Question 7.
#include<stdio.h>
#include<stdlib.h>
#include<ctype.h>
#include<math.h>
#include<string.h>
int main()
{
    char word[100];
    int len = strlen(word);
    int length = strlen(word)/2;
    int flag;
    printf("Please enter a word \n");
    scanf(" %s", word);

    for(int i=0; i<length; i++)
    {
        if(word[i]!=word[len-i-1])
        {
            flag = 1;
            break;
        }
    }
    if(flag==1)
    {
        printf("The word is not a palindrome.");
    }else
    {
        printf("The word is a palindrome.");
    }
    return 0;
}




Question 8.
#include<stdio.h>
#include<stdlib.h>
#include<ctype.h>
#include<math.h>
#include<string.h>
void sort(int array[], int s)
{
    for(int i=0; i<s-1 ; s++)
    {
        for(int j=0 ; j < s - i -1; j++)
        {
            if(array[j]>array[j+1])
            {
                int temp = array[j];
                array[j]=array[j+1];
                array[j+1]=temp;
            }
        }
    }
}

void print(int array[], int s)
{
    for(int i=0; i<s; i++)
    {
        printf("%d",array[i]);
    }
    printf("\n");
}

int main()
{
    int string[100],s;
    printf("Enter no of elements \n");
    scanf("%d", &s);
    printf("Enter the elements in the array");
    for(int i=0;i<s;i++)
    {
        scanf("%d", &string[i]);
    }
    sort(string,s);
    printf("Sorted array is:  \n");
    print(string,s);
    return 0;
}



Question 9.
#include<stdio.h>
#include<stdlib.h>
#include<ctype.h>
#include<math.h>
#include<string.h>
int main()
{
    int x;
    int array[x];
    printf("Enter no of elements: \n");
    scanf("%d", &x);
    printf("Enter the elements:  \n");
    for(int i=0; i<x; i++)
    {
        scanf("%d", &array[i]);
    }
    printf("size of array = %d \n", sizeof(array));
    return 0;

}




Question 10.
#include<stdio.h>
#include<stdlib.h>
#include<ctype.h>
#include<math.h>
#include<string.h>
int main() 
{

int a[100][100],i,j,sum=0,sum1=0,sum2=0;
printf("Enter the array:");
for(i=0;i<4;i++)
{
    for (j=0;j<4;j++)
  {
    scanf("%d",&a[i][j]);
  }
}
printf("the array is:");
for(i=0;i<4;i++)
{
    for(j=0;j<4;j++)
  {
    printf(" \t%d",a[i][j]);
  }
  printf("\n");
}
printf("the sum of the array is:");
for(i=0;i<4;i++)
{
for(j=0;j<4;j++)
  {
    sum=sum+a[i][j];
  }
}
printf("%d",sum);
printf("\nthe sum of the primary diagnol is:");
for(i=0;i<4;i++)
{
sum1=sum1+a[i][i];
}
printf("%d",sum1);
printf("the sum of the secondary diagnols:");
for(i=0;i<4;i++)
{
sum2=sum2+a[i][4-1-i];
}
printf("%d",sum2);

return 0;
}
