#include <fcntl.h>
#include <stdio.h>
#include <sys/stat.h>
#include <unistd.h>

int main() {
  int file = open("tmp", O_RDWR | O_CREAT); //, S_IRUSR | S_IWUSR);
  write(file, "this is a test", 14);
  lseek(file, -7, SEEK_CUR);
  char result[14];
  read(file, result, 14);
  write(1, result, 7);
  printf("\n");
}
