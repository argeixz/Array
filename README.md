#include <stdio.h>
 
int main() {
    int size = 5;
    int numbers[size];
    
    for (int i = 0; i < size; i++){
    printf("Enter a numbers %d/%d:\n", i+1, size);
    scanf("%d",&numbers[i]);
    }
    for ( int i = 0; i <size; i++){
    printf("%d", numbers[i]);
    }
   printf("\n");
     for ( int i = size - 1; i >=0; i--){
    printf("%d", numbers[i]);
    }
    int tail = size - 1;
    int palindrome = 1;
    for (int head = 0; head > size/2;head++){
        if (numbers[head] != numbers[tail]){
            palindrome = 0;
            break;
        }
            tail--;
       }
       if (palindrome){
            printf("\nPalindrome!!");
        }
       else {
            printf("\nNot Palindrome");
        }
        return 0;
    }
