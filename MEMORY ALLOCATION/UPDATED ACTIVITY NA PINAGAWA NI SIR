#include <stdio.h>
#include <stdlib.h>
#include <string.h>

typedef struct{
    char name[100];
    char book[100];
    int year;
    int number;
    char company[100];
    char address[100];
    char status[100];
}school;

void menu();
void display(school * schools, int count);
void search(school *schools, int count);


int main(){
    school* schools = NULL;
    int count = 0;
    int choice;
    do{
    menu();
    printf("Enter a choice: ");
    scanf("%d", &choice);
    getchar();

    switch(choice){
        case 1: {
            schools = realloc(schools, (count + 1)* sizeof(school));
                if(schools == NULL){
                    printf("Memory allocation failed!\n");
                    exit(1);
                }
                    printf("A. Enter a Book Name: ");
                    fgets(schools[count].book, 100, stdin);
                    schools[count].book[strlen(schools[count].book)-1] = 0;
                    printf("B. Enter the Authors Name: ");
                    fgets(schools[count].name, 100, stdin);
                    schools[count].name[strlen(schools[count].name)-1] = 0;
                    printf("C. Enter the publishing company: ");
                    fgets(schools[count].company, 100, stdin);
                    schools[count].company[strlen(schools[count].company)-1] = 0;
                    printf("D. Enter the Renters Address: ");
                    fgets(schools[count].address, 100,stdin);
                    schools[count].address[strlen(schools[count].address)-1] = 0;
                    printf("E. Enter the status of the book [Available/Unavailable]: ");
                    fgets(schools[count].status,100,stdin);
                    schools[count].status[strlen(schools[count].status)-1] = 0;
                    printf("F. Publishing Year: ");
                    scanf("%d", &schools[count].year);
                    printf("G. Address Number: ");
                    scanf("%d", &schools[count].number);
                    

                count++;
                printf("The information has been added successfully!!\n\n");
                break;
        }  
        
        case 2: {
                display(schools, count);
            break;

        }
        case 3:
            if(count == 0){
                printf("There are no books to delete\n\n");
                break;
            }
            display(schools, count);
            int index;
            printf("\nEnter a book number that you wanted to delete (1 to %d): ", count);
            scanf("%d", &index);
            getchar();

            if (index < 1 || index > count){
                printf("Invalid number\n\n");
                break;
            }

            for (int i = index - 1; i < count -1; i++){
                schools[i] = schools[i + 1];
            }

            count--;
            schools = realloc(schools, count* sizeof(school));
            printf("The book has been deleted successfully\n\n");
            break;
        
        case 4:
            search(schools, count);
            break;


        case 5: 
            printf("Thank you for using our program!!");
            free(schools);
            return 0;
            break;
        
        default: 
            printf("Invalid choice. Please try again. \n\n");
    }
    }while (1);
    
}

void menu(){
     printf("WELCOME  TO RENTAL SHOP!!\n");
    printf("-----------------------------------\n");
    printf("- 1. Add a book                   -\n");
    printf("- 2. Display all of the books     -\n");
    printf("- 3. Delete a Book                -\n");
    printf("- 4. Search a Book                -\n");
    printf("- 5. Exit                         -\n");
    printf("-----------------------------------\n");
}

void display(school* schools, int count){
    if(count == 0){
        printf("\nNo book to display\n\n");
        return;
    }
    printf("\n--------THE BOOK RECORDS-----------\n");
    for(int i = 0; i < count; i++){
        printf("Book no. %d: \n", i + 1);
        printf("A. Book name: %s\n", schools[i].book);
        printf("B. Authors Name: %s\n", schools[i].name);
        printf("C. Publishing Company: %s\n", schools[i].company);
        printf("D. Renters Address: %s\n", schools[i].address);
        printf("E. Published Year: %d\n", schools[i].year);
        printf("F. Address Number: %d\n", schools[i].number);
        printf("G. Status: %s\n", schools[i].status);
    }
    printf("\n");
}

void search(school* schools, int count) {
    if (count == 0) {
        printf("No books available to search.\n\n");
        return;
    }

    char keyword[100];
    printf("Enter the book name to search: ");
    fgets(keyword, 100, stdin);
    keyword[strcspn(keyword, "\n")] = '\0'; 

    int found = 0;
    for (int i = 0; i < count; i++) {
        if (strstr(schools[i].book, keyword) != NULL) {
            printf("\nBook no. %d: \n", i + 1);
            printf("A. Book name: %s\n", schools[i].book);
            printf("B. Author's Name: %s\n", schools[i].name);
            printf("C. Publishing Company: %s\n", schools[i].company);
            printf("D. Renter's Address: %s\n", schools[i].address);
            printf("E. Published Year: %d\n", schools[i].year);
            printf("F. Address Number: %d\n", schools[i].number);
            printf("G. Status: %s\n", schools[i].status);
            found = 1;
        }
    }

    if (!found) {
        printf("No book found with that name.\n");
    }

    printf("\n");
}
