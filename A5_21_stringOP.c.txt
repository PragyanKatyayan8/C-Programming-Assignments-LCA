#include <stdio.h>
#include <string.h>
#include <ctype.h>

int main() {
    int choice, i;
    char str1[100], str2[100], ch, sub[50];
    char *ptr;

    while (1) {
        printf("\n===== String Operations Menu =====\n");
        printf("1. Find length (strlen)\n");
        printf("2. Copy string (strcpy)\n");
        printf("3. Concatenate strings (strcat)\n");
        printf("4. Compare strings (strcmp)\n");
        printf("5. Find character (strchr)\n");
        printf("6. Find substring (strstr)\n");
        printf("7. Tokenize string (strtok)\n");
        printf("8. Convert to uppercase\n");
        printf("9. Convert to lowercase\n");
        printf("10. Exit\n");
        printf("Enter your choice: ");
        scanf("%d", &choice);
        getchar();

        switch (choice) {
            case 1:
                printf("Enter string: ");
                fgets(str1, 100, stdin);
                str1[strcspn(str1, "\n")] = '\0';
                printf("Length = %zu\n", strlen(str1));
                break;

            case 2:
                printf("Enter source string: ");
                fgets(str1, 100, stdin);
                str1[strcspn(str1, "\n")] = '\0';
                strcpy(str2, str1);
                printf("Copied string: %s\n", str2);
                break;

            case 3:
                printf("Enter first string: ");
                fgets(str1, 100, stdin);
                str1[strcspn(str1, "\n")] = '\0';

                printf("Enter second string: ");
                fgets(str2, 100, stdin);
                str2[strcspn(str2, "\n")] = '\0';

                strcat(str1, str2);
                printf("Concatenated string: %s\n", str1);
                break;

            case 4:
                printf("Enter first string: ");
                fgets(str1, 100, stdin);
                str1[strcspn(str1, "\n")] = '\0';

                printf("Enter second string: ");
                fgets(str2, 100, stdin);
                str2[strcspn(str2, "\n")] = '\0';

                if (strcmp(str1, str2) == 0)
                    printf("Strings are equal\n");
                else
                    printf("Strings are not equal\n");
                break;

            case 5:
                printf("Enter string: ");
                fgets(str1, 100, stdin);
                str1[strcspn(str1, "\n")] = '\0';

                printf("Enter character to find: ");
                scanf("%c", &ch);
                getchar();

                ptr = strchr(str1, ch);

                if (ptr != NULL)
                    printf("Character found at position %ld\n",
                           (long)(ptr - str1) + 1);
                else
                    printf("Character not found\n");
                break;

            case 6:
                printf("Enter main string: ");
                fgets(str1, 100, stdin);
                str1[strcspn(str1, "\n")] = '\0';

                printf("Enter substring: ");
                fgets(sub, 50, stdin);
                sub[strcspn(sub, "\n")] = '\0';

                ptr = strstr(str1, sub);

                if (ptr != NULL)
                    printf("Substring found\n");
                else
                    printf("Substring not found\n");
                break;

            case 7:
                printf("Enter a string separated by spaces: ");
                fgets(str1, 100, stdin);
                str1[strcspn(str1, "\n")] = '\0';

                ptr = strtok(str1, " ,");
                printf("Tokens:\n");

                while (ptr != NULL) {
                    printf("%s\n", ptr);
                    ptr = strtok(NULL, " ,");
                }
                break;

            case 8:
                printf("Enter string: ");
                fgets(str1, 100, stdin);
                str1[strcspn(str1, "\n")] = '\0';

                for (i = 0; str1[i] != '\0'; i++)
                    str1[i] = toupper((unsigned char)str1[i]);

                printf("Uppercase: %s\n", str1);
                break;

            case 9:
                printf("Enter string: ");
                fgets(str1, 100, stdin);
                str1[strcspn(str1, "\n")] = '\0';

                for (i = 0; str1[i] != '\0'; i++)
                    str1[i] = tolower((unsigned char)str1[i]);

                printf("Lowercase: %s\n", str1);
                break;

            case 10:
                printf("Exiting...\n");
                return 0;

            default:
                printf("Invalid choice!\n");
        }
    }

    return 0;
}
