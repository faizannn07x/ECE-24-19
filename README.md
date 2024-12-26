# ECE-24-19
Programming for problem solving.

#include <stdio.h>

#include <stdio.h>
#include <math.h>
#include <string.h>

// 1. Display your name
void displayName() {
    printf("My name is John Doe\n");
}

// 2. Add two numbers and display the result
void addTwoNumbers() {
    int a, b;
    printf("Enter two numbers: ");
    if (scanf("%d %d", &a, &b) != 2) {
        printf("Invalid input.\n");
        return;
    }
    printf("Sum of %d and %d is %d\n", a, b, a + b);
}

// 3. Read two numbers from keyboard and compare them
void compareTwoNumbers() {
    int num1, num2;
    printf("Enter two numbers: ");
    if (scanf("%d %d", &num1, &num2) != 2) {
        printf("Invalid input.\n");
        return;
    }
    if (num1 > num2)
        printf("%d is greater than %d\n", num1, num2);
    else if (num1 < num2)
        printf("%d is less than %d\n", num1, num2);
    else
        printf("%d is equal to %d\n", num1, num2);
}

// 4. Swap two numbers
void swapTwoNumbers() {
    int a, b, temp;
    printf("Enter two numbers to swap: ");
    if (scanf("%d %d", &a, &b) != 2) {
        printf("Invalid input.\n");
        return;
    }
    printf("Before swap: a = %d, b = %d\n", a, b);
    temp = a;
    a = b;
    b = temp;
    printf("After swap: a = %d, b = %d\n", a, b);
}

// 5. Define and use a constant
void useConstant() {
    const float PI = 3.14159;
    float radius, area;
    printf("Enter radius of circle: ");
    if (scanf("%f", &radius) != 1 || radius < 0) {
        printf("Invalid input.\n");
        return;
    }
    area = PI * radius * radius;
    printf("Area of circle is %.2f\n", area);
}

// 6. Use math library functions
void useMathLibrary() {
    double num;
    printf("Enter a number: ");
    if (scanf("%lf", &num) != 1 || num < 0) {
        printf("Invalid input.\n");
        return;
    }
    printf("Square root of %.2f is %.2f\n", num, sqrt(num));
    printf("2 raised to the power of 3 is %.2f\n", pow(2, 3));
}

// 7. Check whether a number is even or odd
void checkEvenOdd() {
    int num;
    printf("Enter a number: ");
    if (scanf("%d", &num) != 1) {
        printf("Invalid input.\n");
        return;
    }
    printf("%d is %s\n", num, (num % 2 == 0) ? "Even" : "Odd");
}

// 8. Find roots of a quadratic equation
void quadraticRoots() {
    float a, b, c, discriminant, root1, root2;
    printf("Enter coefficients a, b, and c: ");
    if (scanf("%f %f %f", &a, &b, &c) != 3 || a == 0) {
        printf("Invalid input.\n");
        return;
    }
    discriminant = b * b - 4 * a * c;
    if (discriminant > 0) {
        root1 = (-b + sqrt(discriminant)) / (2 * a);
        root2 = (-b - sqrt(discriminant)) / (2 * a);
        printf("Roots are real and different: %.2f, %.2f\n", root1, root2);
    } else if (discriminant == 0) {
        root1 = -b / (2 * a);
        printf("Roots are real and same: %.2f\n", root1);
    } else {
        printf("Roots are complex and different.\n");
    }
}

// 9. Use ternary operator
void ternaryExample() {
    int num;
    printf("Enter a number: ");
    if (scanf("%d", &num) != 1) {
        printf("Invalid input.\n");
        return;
    }
    printf("%d is %s\n", num, (num % 2 == 0) ? "Even" : "Odd");
}

// 10. Compare three numbers using nested if-else
void compareThreeNumbers() {
    int a, b, c;
    printf("Enter three numbers: ");
    if (scanf("%d %d %d", &a, &b, &c) != 3) {
        printf("Invalid input.\n");
        return; 
        // Task 13: Display the series 1 2 3 ... n
#include <stdio.h>
int main() {
    int n;
    printf("Enter the value of n: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        printf("%d ", i);
    }
    return 0;
}

// Task 13: Display the series 1 2 3 ... n
#include <stdio.h>
int main() {
    int n;
    printf("Enter the value of n: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        printf("%d ", i);
    }
    return 0;
}

// Task 14: Display the series n n-1 ... 1
#include <stdio.h>
int main() {
    int n;
    printf("Enter the value of n: ");
    scanf("%d", &n);
    for (int i = n; i >= 1; i--) {
        printf("%d ", i);
    }
    return 0;
}

// Task 15: Display all even numbers from 1 to 100
#include <stdio.h>
int main() {
    for (int i = 2; i <= 100; i += 2) {
        printf("%d ", i);
    }
    return 0;
}

// Task 16: Find the sum of the series 1 2 3 ... n
#include <stdio.h>
int main() {
    int n, sum = 0;
    printf("Enter the value of n: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        sum += i;
    }
    printf("Sum = %d", sum);
    return 0;
}

// Task 17: Find the product of the series 1 2 3 ... n
#include <stdio.h>
int main() {
    int n, product = 1;
    printf("Enter the value of n: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        product *= i;
    }
    printf("Product = %d", product);
    return 0;
}

// Task 18: Find the factorial of a number entered by the user
#include <stdio.h>
int main() {
    int n, fact = 1;
    printf("Enter a number: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        fact *= i;
    }
    printf("Factorial = %d", fact);
    return 0;
}

// Task 19: Find all factors of a natural number
#include <stdio.h>
int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
    printf("Factors of %d are: ", n);
    for (int i = 1; i <= n; i++) {
        if (n % i == 0) {
            printf("%d ", i);
        }
    }
    return 0;
}

// Task 20: Check whether a number is prime or not
#include <stdio.h>
int main() {
    int n, isPrime = 1;
    printf("Enter a number: ");
    scanf("%d", &n);
    for (int i = 2; i <= n / 2; i++) {
        if (n % i == 0) {
            isPrime = 0;
            break;
        }
    }
    if (isPrime && n > 1)
        printf("%d is a prime number.", n);
    else
        printf("%d is not a prime number.", n);
    return 0;
}

// Task 21: Display the series 2 4 8 16 ...
#include <stdio.h>
int main() {
    int n, term = 2;
    printf("Enter the number of terms: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        printf("%d ", term);
        term *= 2;
    }
    return 0;
}

// Task 22: Display the series 2 4 16 256 ...
#include <stdio.h>
int main() {
    int n, term = 2;
    printf("Enter the number of terms: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        printf("%d ", term);
        term = term * term;
    }
    return 0;
}

// Task 23: Display the Fibonacci series up to n terms
#include <stdio.h>
int main() {
    int n, t1 = 0, t2 = 1, nextTerm;
    printf("Enter the number of terms: ");
    scanf("%d", &n);
    printf("Fibonacci series: ");
    for (int i = 1; i <= n; i++) {
        printf("%d ", t1);
        nextTerm = t1 + t2;
        t1 = t2;
        t2 = nextTerm;
    }
    return 0;
}

// Task 24: Display the table of all integers from 2 to 10
#include <stdio.h>
int main() {
    for (int i = 2; i <= 10; i++) {
        printf("Table of %d:\n", i);
        for (int j = 1; j <= 10; j++) {
            printf("%d x %d = %d\n", i, j, i * j);
        }
        printf("\n");
    }
    return 0;
}

// Task 25: Display the series 1 2 3 ... with nested loops
#include <stdio.h>
int main() {
    int n;
    printf("Enter the value of n: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        for (int j = 1; j <= i; j++) {
            printf("%d ", j);
        }
        printf("\n");
    }
    return 0;
}

// Task 26: Display the series 1 1/2 1/3 ...
#include <stdio.h>
int main() {
    int n;
    printf("Enter the value of n: ");
    scanf("%d", &n);
    double sum = 0;
    for (int i = 1; i <= n; i++) {
        sum += 1.0 / i;
        printf("1/%d ", i);
    }
    printf("\nSum = %.2f", sum);
    return 0;
}

// Task 27: Find sum of series 1 + 1/2 + 1/3 + ... + 1/n
#include <stdio.h>
int main() {
    int n;
    double sum = 0.0;
    printf("Enter the value of n: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        sum += 1.0 / i;
    }
    printf("Sum = %.2f", sum);
    return 0;
}

// Task 28: Display the digits of any natural number in reverse order
#include <stdio.h>
int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
    printf("Digits in reverse order: ");
    while (n != 0) {
        printf("%d ", n % 10);
        n /= 10;
    }
    return 0;
}

// Task 29: Check whether a number is Armstrong number or not
#include <stdio.h>
#include <math.h>
int main() {
    int n, originalNum, remainder, result = 0, numDigits = 0;
    printf("Enter a number: ");
    scanf("%d", &n);
    originalNum = n;
    while (originalNum != 0) {
        originalNum /= 10;
        ++numDigits;
    }
    originalNum = n;
    while (originalNum != 0) {
        remainder = originalNum % 10;
        result += pow(remainder, numDigits);
        originalNum /= 10;
    }
    if (result == n)
        printf("%d is an Armstrong number.", n);
    else
        printf("%d is not an Armstrong number.", n);
    return 0;
}

// Task 30: Find the GCD (Greatest Common Divisor) of two numbers
#include <stdio.h>
int main() {
    int a, b;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    while (a != b) {
        if (a > b)
            a -= b;
        else
            b -= a;
    }
    printf("GCD = %d", a);
    return 0;
}
// Task 31: Find the LCM (Least Common Multiple) of two numbers
#include <stdio.h>
int main() {
    int a, b, max;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    max = (a > b) ? a : b;
    while (1) {
        if (max % a == 0 && max % b == 0) {
            printf("LCM = %d", max);
            break;
        }
        ++max;
    }
    return 0;
}

// Task 32: Reverse a given string
#include <stdio.h>
#include <string.h>
int main() {
    char str[100], rev[100];
    int len, i;
    printf("Enter a string: ");
    scanf("%s", str);
    len = strlen(str);
    for (i = 0; i < len; i++) {
        rev[i] = str[len - i - 1];
    }
    rev[i] = '\0';
    printf("Reversed string: %s", rev);
    return 0;
}

// Task 33: Check whether a string is palindrome or not
#include <stdio.h>
#include <string.h>
int main() {
    char str[100];
    int len, i, isPalindrome = 1;
    printf("Enter a string: ");
    scanf("%s", str);
    len = strlen(str);
    for (i = 0; i < len / 2; i++) {
        if (str[i] != str[len - i - 1]) {
            isPalindrome = 0;
            break;
        }
    }
    if (isPalindrome)
        printf("The string is a palindrome.");
    else
        printf("The string is not a palindrome.");
    return 0;
}

// Task 34: Count the number of vowels in a string
#include <stdio.h>
#include <string.h>
int main() {
    char str[100];
    int count = 0;
    printf("Enter a string: ");
    scanf("%s", str);
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] == 'a' || str[i] == 'e' || str[i] == 'i' || str[i] == 'o' || str[i] == 'u' ||
            str[i] == 'A' || str[i] == 'E' || str[i] == 'I' || str[i] == 'O' || str[i] == 'U') {
            count++;
        }
    }
    printf("Number of vowels: %d", count);
    return 0;
}

// Task 35: Count the number of words in a string
#include <stdio.h>
#include <string.h>
int main() {
    char str[100];
    int count = 1;
    printf("Enter a string: ");
    scanf(" %[^"]", str);
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] == ' ')
            count++;
    }
    printf("Number of words: %d", count);
    return 0;
}

// Task 36: Convert a string to uppercase
#include <stdio.h>
#include <string.h>
int main() {
    char str[100];
    printf("Enter a string: ");
    scanf("%s", str);
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] >= 'a' && str[i] <= 'z') {
            str[i] = str[i] - 32;
        }
    }
    printf("Uppercase string: %s", str);
    return 0;
}

// Task 37: Convert a string to lowercase
#include <stdio.h>
#include <string.h>
int main() {
    char str[100];
    printf("Enter a string: ");
    scanf("%s", str);
    for (int i = 0; str[i] != '\0'; i++) {
        if (str[i] >= 'A' && str[i] <= 'Z') {
            str[i] = str[i] + 32;
        }
    }
    printf("Lowercase string: %s", str);
    return 0;
}

// Task 38: Find the length of a string
#include <stdio.h>
#include <string.h>
int main() {
    char str[100];
    printf("Enter a string: ");
    scanf("%s", str);
    printf("Length of the string: %ld", strlen(str));
    return 0;
}

// Task 39: Concatenate two strings
#include <stdio.h>
#include <string.h>
int main() {
    char str1[100], str2[100], result[200];
    printf("Enter first string: ");
    scanf("%s", str1);
    printf("Enter second string: ");
    scanf("%s", str2);
    strcpy(result, str1);
    strcat(result, str2);
    printf("Concatenated string: %s", result);
    return 0;
}

// Task 40: Compare two strings
#include <stdio.h>
#include <string.h>
int main() {
    char str1[100], str2[100];
    printf("Enter first string: ");
    scanf("%s", str1);
    printf("Enter second string: ");
    scanf("%s", str2);
    if (strcmp(str1, str2) == 0)
        printf("Strings are equal.");
    else
        printf("Strings are not equal.");
    return 0;
}

// Task 41: Swap two numbers using a temporary variable
#include <stdio.h>
int main() {
    int a, b, temp;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    temp = a;
    a = b;
    b = temp;
    printf("After swapping: a = %d, b = %d", a, b);
    return 0;
}

// Task 42: Swap two numbers without using a temporary variable
#include <stdio.h>
int main() {
    int a, b;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    a = a + b;
    b = a - b;
    a = a - b;
    printf("After swapping: a = %d, b = %d", a, b);
    return 0;
}

// Task 43: Generate a random number
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
int main() {
    srand(time(0));
    printf("Random number: %d", rand());
    return 0;
}

// Task 44: Generate a random number within a range
#include <stdio.h>
#include <stdlib.h>
#include <time.h>
int main() {
    int lower, upper;
    printf("Enter the lower and upper limit: ");
    scanf("%d %d", &lower, &upper);
    srand(time(0));
    printf("Random number: %d", (rand() % (upper - lower + 1)) + lower);
    return 0;
}

// Task 45: Implement a calculator
#include <stdio.h>
int main() {
    char operator;
    double num1, num2, result;
    printf("Enter an operator (+, -, *, /): ");
    scanf(" %c", &operator);
    printf("Enter two numbers: ");
    scanf("%lf %lf", &num1, &num2);
    switch (operator) {
        case '+':
