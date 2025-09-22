#define _POSIX_C_SOURCE 200809L
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

int main() {

  char *buff = NULL;
  size_t len = 0;
  printf("Please enter some text: ");
  ssize_t num_char = getline(&buff, &len, stdin);
  if (num_char == -1) {
    perror("getline failed");
    exit(EXIT_FAILURE);
  }

  char *saveptr;
  char *ret = strtok_r(buff, " ", &saveptr);
  printf("Tokens:");
  while (ret != NULL) {
    printf("\n\t%s", ret);
    ret = strtok_r(NULL, " ", &saveptr);
  }

  free(buff);
}
