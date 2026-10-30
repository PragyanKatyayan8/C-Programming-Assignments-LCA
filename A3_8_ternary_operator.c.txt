#include<stdio.h>
int main()
{
 int age;
 printf("Enter your age:\n");
 scanf("%d",&age);
 char *msg = (age >= 18) ? "You are an Adult" : " You are a Minor" ;
 printf("%s\n", msg);
 return 0 ;
}
