#include<stdio.h>
int main()
{
 float number;
 printf("Enter your desired number:\n");
 scanf("%f",&number);
 if ( number==0 )
  {
   printf("Number is neither positive nor negative\n");
  }
 else if ( number > 0)
  { 
   printf("Number is postive\n");
  }
 else 
  {
   printf("Number is negative\n");
  }

 return 0;
}
