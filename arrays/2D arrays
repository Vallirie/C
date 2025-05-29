#include <stdio.h>

int main (){
    int rows, columns;
    printf("Enter the rows of an array: ");
    scanf("%d", &rows);
    printf("Enter the columns of an array: ");
    scanf("%d", &columns);
    
    int arr[rows][columns];
    for (int i = 0; i < rows; i++){
        for (int j = 0; j < columns; j++){
            printf("Enter the [%d", i + 1);
            printf("][%d", j + 1);
            printf("] of an array: ");
            scanf("%d", &arr[i][j]);
        }
    }
    
    for (int i = 0; i < rows; i++){
        for (int j = 0; j < columns; j++){
            printf("\t%d", arr[i][j]);
        }
        printf("\n");
    }
    return 0;
}
