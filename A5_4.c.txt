#include <stdio.h>
#include <string.h>

int main()
{
    char src[] = "Hello";
    char dest[20];

    strcpy(dest, src);

    printf("%s\n", dest);

    return 0;
}
