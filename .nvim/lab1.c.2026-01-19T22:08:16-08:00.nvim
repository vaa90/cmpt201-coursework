#define _POSIX_C_SOURCE 200809L
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main(void) {
    char *line = NULL;
    size_t len = 0;

    while (1) {
        printf("Please enter some text: ");

        if (getline(&line, &len, stdin) == -1) {
            perror("getline failed");
            exit(EXIT_FAILURE);
        }


        printf("Tokens:\n");

        char *saveptr;
        char *token = strtok_r(line, " ", &saveptr);

        while (token != NULL) {
            printf("  %s\n", token);
            token = strtok_r(NULL, " ", &saveptr);
        }
    }

    free(line);
    return 0;
}

