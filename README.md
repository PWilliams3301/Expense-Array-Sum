Expense-Array-Sum
=================

//This program uses an array to allow the user to enter up to 25 transactions and computes the sum of the transactions at the end of the program.

#include <stdio.h>
#include <stdlib.h>
#define EXPENSE_ARRAY_SIZE 25


int main(){
    int num_expenses, k;
    double expense[EXPENSE_ARRAY_SIZE], expenseSum = 0;
    
    printf("This program will compute the total of up to 25 transactions.\n\n");
    printf("How many expenses will you be entering? : ");
    scanf("%d", &num_expenses);
    
    for (k = 0; k < num_expenses; ++k){
        printf("Enter expense %d:", k+1);
        scanf("%lf", &expense[k]);
        expenseSum += expense[k];
    }
    
    printf("Your expense sum is: $%lf", expenseSum);
    
    return 0;
}
