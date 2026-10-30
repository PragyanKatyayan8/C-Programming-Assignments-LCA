#include <stdio.h>
#include <string.h>

int main()
{
    char str[] = "banana";

    char *ptr = strrchr(str, 'a');

    if(ptr != NULL)
        printf("%s\n", ptr);
    else
        printf("Not found\n");

    return 0;
}
