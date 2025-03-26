# EX-NO-6-Pseudo-Random-Number

# AIM: 

Implementation of Pseudorandom Number Generation Using Standard library


## ALGORITHM:

1)Prompt the user for the number of random numbers to generate.</br>
2)Request the user to input the minimum and maximum values for the random number range.</br>
3)Seed the random number generator using the current time to ensure different results on each run.</br>
4)For the specified number of times, generate a random number:</br>
    Use the formula rand() % (max - min + 1) + min to ensure the number falls within the specified range.</br>
5)Print each generated random number.</br>
6)End the program.</br>

## Program Code:

```
#include <stdio.h>

#define A 1664525
#define C 1013904223
#define M 4294967296 // 2^32

unsigned int lcg(unsigned int seed) {
    return (A * seed + C) % M;
}

int main() {
    unsigned int seed;
    int n;

    printf("Enter the seed value: ");
    scanf("%u", &seed);
    printf("Enter how many random numbers to generate: ");
    scanf("%d", &n);
    printf("Random numbers:\n");

    for (int i = 0; i < n; i++) {
        seed = lcg(seed);
        printf("%u\n", seed);
    }

    return 0;
}
```
## Output:
![image](https://github.com/user-attachments/assets/5dacfc1e-34a3-470b-bb0b-0d6303935a06)


## Result

The program for Pseudorandom Number Generation using the standard library is executed successfully.
