#include <stdio.h>
#include <string.h>

int main()
{
    char s1[] = "HelloWorld";
    char s2[] = "HelloC";

    if(strncmp(s1, s2, 5) == 0)
        printf("First 5 chars same\n");
    else
        printf("Different\n");

    return 0;
}
