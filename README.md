#include <iostream>
#include <cstdlib>
#include <ctime>

int main() {
    
    std::srand(std::time(0));
    int randomNumber = std::rand() % 100 + 1; 
    int userGuess = 0;

    std::cout << "************************************************************************************" << std::endl;
     std::cout << "                       Welcome to the Number Guessing Game!                        " << std::endl;
    std::cout << "             I have selected a number between 1 and 100. Can you guess it?          " << std::endl;
    std::cout << "************************************************************************************" << std::endl;

    while (userGuess != randomNumber) {
        std::cout << "Enter your guess: ";
        std::cin >> userGuess;

        if (userGuess < randomNumber) {
            std::cout << "Too low! Try again." << std::endl;
        } else if (userGuess > randomNumber) {
            std::cout << "Too high! Try again." << std::endl;
        } else {
            std::cout << "Congratulations! You guessed the correct number: " << randomNumber << std::endl;
        }
    }

    return 0;
}
