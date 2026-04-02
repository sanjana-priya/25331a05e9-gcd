
#include <stdio.h>

int findGCD(int a, int b) {
    
    if (b == 0) {
        return a;
    }
    
    return findGCD(b, a % b);
}

int main() {
    int num1, num2, result;

    printf("Enter two positive integers: ");
    if (scanf("%d %d", &num1, &num2) != 2) {
        printf("Invalid input.\n");
        return 1;
    }
    
    result = findGCD(num1, num2);

    printf("The GCD of %d and %d is: %d\n", num1, num2, result);

    return 0;
}
