# Task-1
#include <stdio.h>

void addition();
void subtraction();
void multiplication();
void division();

int main() {
    int choice;

    while (1) {
        printf("\n\nSimple Calculator\n");
        printf("1. Addition\n");
        printf("2. Subtraction\n");
        printf("3. Multiplication\n");
        printf("4. Division\n");
        printf("5. Exit\n");
        printf("\nEnter your choice: ");
        scanf("%d", &choice);

        switch (choice) {
            case 1:
                addition();
                break;
            case 2:
                subtraction();
                break;
            case 3:
                multiplication();
                break;
            case 4:
                division();
                break;
            case 5:
                printf("Exiting...\n");
                return 0;
            default:
                printf("Invalid choice. Please try again.\n");
        }
    }
    return 0;
}

void addition() {
    float num1, num2;
    printf("\nEnter first numbers to add: ");
    scanf("%f",& num1 );
    printf("Enter second numbers to add: ");
    scanf("%f",&num2);
    printf("Result: %.2f\n", num1 + num2);
}

void subtraction() {
    float num1, num2;
    printf("\nEnter first numbers to subtract: ");
    scanf("%f",& num1 );
    printf("Enter second numbers to subtract: ");
    scanf("%f",&num2);
    printf("Result: %.2f\n", num1 - num2);
}

void multiplication() {
    float num1, num2;
    printf("\nEnter first numbers to multiply: ");
    scanf("%f",& num1 );
    printf("Enter second numbers to multiple: ");
    scanf("%f",&num2);
    printf("Result: %.2f\n", num1 * num2);
}

void division() {
    float num1, num2;
    printf("\nEnter first number for division ");
    scanf("%f", &num1);
    printf("Enter second number for division ");
    scanf("%f", &num2);
    if (num2 != 0)
        printf("Result: %.2f\n", num1 / num2);
    else
        printf("Error: Division by zero is not allowed.\n");
}



Task-b


#include<stdio.h>
#include<stdlib.h>
#include<time.h>
int main()
{
    int mynum, usernum ;
    srand(time(NULL));
    mynum = rand()%100+1;
    printf("\nWELCOME TO GUESS THE NUMBER GAME\n\n");
    printf("Hint:-Number lies between 0-100");
    while(1)
    {
        printf("\n\nENTER YOUR GUESS:");
        scanf("%d",& usernum);
        if(mynum == usernum)
        {
            printf("WINNER!!");
            printf("you guess it correct.");
            break;
        }
        else if (mynum > usernum)
        {
            printf("Too low,TRY AGAIN!!");
        }
        else {
            printf("Too high,TRY AGAIN!!");
        }
    }
    
    return 0;
}
