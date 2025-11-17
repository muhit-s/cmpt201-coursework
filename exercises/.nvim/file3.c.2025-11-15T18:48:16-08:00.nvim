#include <fcntl.h>
#include <stdio.h>
#include <sys/stat.h>
#include <unistd.h>

int main() {
  char *str = "testing\n";
  FILE *f = fopen("tmp", "w+");

  fprintf(f, "%s", str);
  fflush(f);
  while (1) {
    sleep(3);
  }
}
