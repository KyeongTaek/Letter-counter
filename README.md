# friendly-winner
letter counter(for Hangul)
#define _CRT_SECURE_NO_WARNINGS
#include <stdio.h>
#include <string.h>
int main()
{
  char arr[10000];
  scanf("%[^\n]s", arr);
  int countofall, countofchar, i=0, j=0, k=0;
  char *ptr1=strchr(arr, ' ');
  char *ptr2=strchr(arr, ',');
  char *ptr3=strchr(arr, '.');
  countofall=strlen(arr);
  while(ptr1!=NULL)
  {
    i++;
    ptr1=strchr(ptr1+1, ' ');
  }
  while(ptr2!=NULL)
  {
    j++;
    ptr2=strchr(ptr2+1, ',');
  }
  while(ptr3!=NULL)
  {
    k++;
    ptr3=strchr(ptr3+1, '.');
  }
  countofchar=(countofall-i-j-k)/3;
  printf("%d자입니다\n", countofchar+i+j+k);
  return 0;
}
