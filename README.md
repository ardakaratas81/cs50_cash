# cs50_cash
#include <stdio.h>
#include <cs50.h>
#include <math.h>

    int main (void){

        float dollars;
        do{
            dollars = get_float("change owed: ");
        } while(dollars < 0);

        int cents = round(dollars*100);
        int coins = 0;

        int denominations[] = {25, 10, 5, 1};
        int size = 4;
        for ( int i = 0; i < size; i++){
            coins += cents / denominations[i];
            cents %= denominations[i];
     
       } 
            printf("%i\n", coins);    
    }

