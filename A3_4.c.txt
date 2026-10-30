#include<stdio.h>
int main()
{
 int age;
 printf("Enter your Age:\n");
 scanf("%d",&age);
 if(age >= 18)
  {
   printf("You can Vote\n");
  }
 else
  {
   printf("You cannot Vote\n");
  }
 return 0;
}
