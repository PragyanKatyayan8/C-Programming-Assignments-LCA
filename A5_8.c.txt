#include <stdio.h>
#include <string.h>

int main()
{
    char s1[] = "apple";
    char s2[] = "banana";

    int res = strcmp(s1, s2);

    if(res == 0)
        printf("Equal\n");
    else if(res < 0)
        printf("s1 comes before s2\n");
    else
        printf("s1 comes after s2\n");

    return 0;
}
