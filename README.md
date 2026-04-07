# guessing_game.c
A simple number guessing game in c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>


int main(){
  int random, guess; 
  int no_of_guess = 0;
  srand(time(NULL));


 printf("welcome to the world of Guessing  number\n");
 random = rand() % 100 +1; //Generating between 0 to 100 
 //printf("number generated is: %d", random);


    do {
    printf("\nplease enter your Guess between(1 to 100):");
    scanf("%d", &guess);
    no_of_guess++;

    if (guess < random) {
     printf("Guess larger number. \n" );
    } else if (guess > random) {
     printf("Guess smaller number.\n" );
    } else {
      printf("congratulations !!!you have successfully guessed the number in %d attempts",no_of_guess);
    }

  } while (guess != random);

  printf("\n Bye Bye,thanks for playing."); 
  printf("\n Developed by: Satyam Tiwari");
}
