#include <stdio.h>

int main (){
int size;
printf("Enter the size of a first and second array: ");
scanf("%d", &size);

int arr1[size];
for (int i = 0; i < size; i++){
printf("Enter the %d", i + 1);
printf(" for the first array: ");
scanf("%d", &arr1[i]);
}

int arr2[size];
printf("\n");
for (int i = 0; i < size; i++){
printf("Enter the %d", i + 1);
printf(" for the first array: ");
scanf("%d", &arr2[i]);
}

int highest = 0;
for (int i = 0; i < size; i++){
if (arr1[i] > arr2[i]){
if (arr1[i] > highest)
highest = arr1[i];
}
else if (arr2[i] < arr2[i]){
if (arr2[i] > highest)
highest = arr2[i];
}
}

int arr3[1];
arr3[0] = highest;

printf("%d", arr3[0]);



return 0;

}
