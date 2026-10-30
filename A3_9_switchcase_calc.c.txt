#include <stdio.h>

int main() 
{
 char op;
 float a, b, result;

 while (1) 
 {
  printf("\nEnter operator (+, -, *, /, %%, x [to exit] ): \n");
  scanf(" %c", &op);
  if (op != '+' && op != '-' && op != '*' && op != '/' && op != '%' && op != 'x' && op != 'X' ) 
  {
   printf("Error: Invalid operator!\n");
   continue;
  }
  if (op == 'x' || op == 'X') 
  {
   printf("Exiting calculator.\n");
   break;
  }
  printf("Enter two numbers: ");
  if (scanf("%f %f", &a, &b) != 2) 
  {
   printf("Error: Please enter valid numbers!\n");
   while (getchar() != '\n');
   continue;
  }

  switch (op) 
   {
    case '+':
    result = a + b;
    printf("Result = %.2f\n", result);
    break;

    case '-':
    result = a - b;
    printf("Result = %.2f\n", result);
    break;

    case '*':
    result = a * b;
    printf("Result = %.2f\n", result);
    break;

    case '/':
    if (b != 0)
    {
     result = a / b;
     printf("Result = %.2f\n", result);
    } 
    else 
    {
     printf("Error: Cannot divide by zero!\n");
    }
    break;

    case '%':
    if (a == (int)a && b == (int)b) 
    {
     if ((int)b != 0) 
     {
      result = (int)a % (int)b;
      printf("Result = %.0f\n", result);
     } 
     else 
     {
      printf("Error: Modulus by zero is not allowed!\n");
     }
    } 
    else 
    {
     printf("Error: Modulus requires integers!\n");
    }
     break;

    default:
    printf("Error: Invalid operator!\n");
   }
  }

    return 0;
}
