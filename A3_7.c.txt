#include<stdio.h>
int main()
{
 int age;
 printf("Enter your age:\n");
 scanf("%d",&age);
 if (age >= 18)
  {
   if (age >= 21)
    { 
     printf("You can Vote ,and Drink\n");
    }
   else 
    { 
    printf("You can Vote ,not Drink\n"); 
    }
  }
 else 
  { 
 printf("You are not eligible for Voting or Drinking\n"); 
  }
 return 0;
}
