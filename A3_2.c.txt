#include<stdio.h>
int main()
{
int a = 21;
unsigned int b =300;
char ch = 'z';
float f = 4.75;
double d = 3.1469793;
long int li = 2345678910;
char str[] = "Hello World";

printf("Integer(%%d):%d\n",a);
printf("Unsigned(%%u):%u\n",b);
printf("Character(%%c):%c\n",ch);
printf("Float(%%f):%f\n",f);
printf("Double(%%lf):%lf\n",d);
printf("Long integer(%%ld):%ld\n",li);
printf("String(%%s):%s\n",str);
printf("Hex(%%x):%x\n",a);
printf("Octal(%%o):%o\n",a);
printf("Pointer(%%p):%p\n",&a);
printf("Percentage(%%):%%\n");
return 0 ;

}
