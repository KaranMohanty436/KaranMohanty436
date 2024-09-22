- 👋 Hi, I’m @Karan Mohanty
- 👀 I’m interested in hacking 
- 🌱 I’m currently learning b-tech CST 1st yr
- 📫 How to reach me
- 😄 Pronouns
- ⚡ Fun fact

## Let's Create a Simple Number Guessing Game in C!

**Here's a basic outline:**

1. **Generate a random number:** We'll use the `rand()` function to generate a random number within a specified range.
2. **Prompt the user:** Ask the user to guess the number.
3. **Compare the guess:** Check if the user's guess is correct, too high, or too low.
4. **Provide feedback:** Give the user hints based on their guess.
5. **Repeat:** Continue prompting the user until they guess the correct number.

**Here's the C code:**

```c
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    srand(time(NULL)); // Seed the random number generator
    int secretNumber = rand() % 100 + 1; // Generate a random number between 1 and 100
    int guess;
    int attempts = 0;

    printf("I'm thinking of a number between 1 and 100. Can you guess it?\n");

    do {
        printf("Enter your guess: ");
        scanf("%d", &guess);
        attempts++;

        if (guess == secretNumber) {
            printf("Congratulations! You guessed the number in %d attempts.\n", attempts);
        } else if (guess < secretNumber) {
            printf("Too low! Try again.\n");
        } else {
            printf("Too high! Try again.\n");
        }
    } while (guess != secretNumber);

    return 0;
}
```

**Explanation:**

- `srand(time(NULL))`: Seeds the random number generator using the current time for better randomness.
- `rand() % 100 + 1`: Generates a random number between 1 and 100.
- The `do-while` loop continues until the user guesses correctly.
- The `if-else` statements provide feedback based on the user's guess.

**Want to make it more challenging?** Consider adding features like:
- **Limited attempts:** Set a maximum number of tries.
- **Difficulty levels:** Adjust the range of random numbers.
- **Hints:** Provide hints after a certain number of incorrect guesses.

Would you like to add any of these features or explore another game idea?

Citations: [[1]](https://github.com/ThakurPrad33p/guessTheNumber), [[2]](https://github.com/NagarajuNarishetti/Menu-Driven-Application-for-Games), [[3]](https://github.com/Kensukeken-Lounge/Cpp-ProgrammingResources)
