#include <stdio.h>

int main()
{
    FILE *source, *destination;
    char ch;

    source = fopen("source.txt", "r");

    if (source == NULL)
    {
        printf("Source file cannot be opened.");
        return 1;
    }

    destination = fopen("destination.txt", "w");

    if (destination == NULL)
    {
        printf("Destination file cannot be opened.");
        fclose(source);
        return 1;
    }

    while ((ch = fgetc(source)) != EOF)
    {
        fputc(ch, destination);
    }

    fclose(source);
    fclose(destination);

    printf("File copied successfully.");

    return 0;
}
