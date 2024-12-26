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


        // Task 46: Find the largest of three numbers
#include <stdio.h>
int main() {
    int a, b, c;
    printf("Enter three numbers: ");
    scanf("%d %d %d", &a, &b, &c);
    if (a >= b && a >= c)
        printf("%d is the largest number.", a);
    else if (b >= a && b >= c)
        printf("%d is the largest number.", b);
    else
        printf("%d is the largest number.", c);
    return 0;
}

// Task 47: Check if a number is even or odd
#include <stdio.h>
int main() {
    int num;
    printf("Enter a number: ");
    scanf("%d", &num);
    if (num % 2 == 0)
        printf("%d is even.", num);
    else
        printf("%d is odd.", num);
    return 0;
}

// Task 48: Check if a year is a leap year
#include <stdio.h>
int main() {
    int year;
    printf("Enter a year: ");
    scanf("%d", &year);
    if ((year % 4 == 0 && year % 100 != 0) || year % 400 == 0)
        printf("%d is a leap year.", year);
    else
        printf("%d is not a leap year.", year);
    return 0;
}

// Task 49: Check if a character is a vowel or consonant
#include <stdio.h>
int main() {
    char ch;
    printf("Enter a character: ");
    scanf(" %c", &ch);
    if (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u' ||
        ch == 'A' || ch == 'E' || ch == 'I' || ch == 'O' || ch == 'U')
        printf("%c is a vowel.", ch);
    else
        printf("%c is a consonant.", ch);
    return 0;
}

// Task 50: Find the ASCII value of a character
#include <stdio.h>
int main() {
    char ch;
    printf("Enter a character: ");
    scanf(" %c", &ch);
    printf("ASCII value of %c is %d.", ch, ch);
    return 0;
}

// Task 51: Display multiplication table of a number
#include <stdio.h>
int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
    for (int i = 1; i <= 10; i++) {
        printf("%d x %d = %d\n", n, i, n * i);
    }
    return 0;
}

// Task 52: Find the sum of natural numbers up to n
#include <stdio.h>
int main() {
    int n, sum = 0;
    printf("Enter a number: ");
    scanf("%d", &n);
    for (int i = 1; i <= n; i++) {
        sum += i;
    }
    printf("Sum = %d", sum);
    return 0;
}

// Task 53: Find the sum of digits of a number
#include <stdio.h>
int main() {
    int n, sum = 0;
    printf("Enter a number: ");
    scanf("%d", &n);
    while (n != 0) {
        sum += n % 10;
        n /= 10;
    }
    printf("Sum of digits = %d", sum);
    return 0;
}

// Task 54: Reverse a number
#include <stdio.h>
int main() {
    int n, reverse = 0;
    printf("Enter a number: ");
    scanf("%d", &n);
    while (n != 0) {
        reverse = reverse * 10 + n % 10;
        n /= 10;
    }
    printf("Reversed number = %d", reverse);
    return 0;
}

// Task 55: Check if a number is a palindrome
#include <stdio.h>
int main() {
    int n, original, reverse = 0;
    printf("Enter a number: ");
    scanf("%d", &n);
    original = n;
    while (n != 0) {
        reverse = reverse * 10 + n % 10;
        n /= 10;
    }
    if (original == reverse)
        printf("%d is a palindrome.", original);
    else
        printf("%d is not a palindrome.", original);
    return 0;
}

// Task 56: Find the factorial of a number using recursion
#include <stdio.h>
long long factorial(int n) {
    if (n == 0 || n == 1)
        return 1;
    return n * factorial(n - 1);
}
int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
    printf("Factorial of %d = %lld", n, factorial(n));
    return 0;
}

// Task 57: Generate Fibonacci series up to n terms using recursion
#include <stdio.h>
int fibonacci(int n) {
    if (n == 0)
        return 0;
    if (n == 1)
        return 1;
    return fibonacci(n - 1) + fibonacci(n - 2);
}
int main() {
    int n;
    printf("Enter the number of terms: ");
    scanf("%d", &n);
    printf("Fibonacci series: ");
    for (int i = 0; i < n; i++) {
        printf("%d ", fibonacci(i));
    }
    return 0;
}

// Task 58: Find GCD of two numbers using recursion
#include <stdio.h>
int gcd(int a, int b) {
    if (b == 0)
        return a;
    return gcd(b, a % b);
}
int main() {
    int a, b;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    printf("GCD = %d", gcd(a, b));
    return 0;
}

// Task 59: Find LCM of two numbers using GCD
#include <stdio.h>
int gcd(int a, int b) {
    if (b == 0)
        return a;
    return gcd(b, a % b);
}
int main() {
    int a, b;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    printf("LCM = %d", (a * b) / gcd(a, b));
    return 0;
}

// Task 60: Convert binary to decimal
#include <stdio.h>
#include <math.h>
int main() {
    int binary, decimal = 0, base = 0;
    printf("Enter a binary number: ");
    scanf("%d", &binary);
    while (binary != 0) {
        decimal += (binary % 10) * pow(2, base);
        binary /= 10;
        base++;
    }
    printf("Decimal equivalent = %d", decimal);
    return 0;
}

// Task 61: Convert decimal to binary
#include <stdio.h>
int main() {
    int decimal, binary[32], index = 0;
    printf("Enter a decimal number: ");
    scanf("%d", &decimal);
    while (decimal != 0) {
        binary[index++] = decimal % 2;
        decimal /= 2;
    }
    printf("Binary equivalent: ");
    for (int i = index - 1; i >= 0; i--) {
        printf("%d", binary[i]);
    }
    return 0;
}

// Task 62: Check if a number is a power of 2
#include <stdio.h>
int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
    if (n > 0 && (n & (n - 1)) == 0)
        printf("%d is a power of 2.", n);
    else
        printf("%d is not a power of 2.", n);
    return 0;
}

// Task 63: Swap two numbers using bitwise XOR
#include <stdio.h>
int main() {
    int a, b;
    printf("Enter two numbers: ");
    scanf("%d %d", &a, &b);
    a = a ^ b;
    b = a ^ b;
    a = a ^ b;
    printf("After swapping: a = %d, b = %d", a, b);
    return 0;
}

// Task 64: Count the number of set bits in a number
#include <stdio.h>
int main() {
    int n, count = 0;
    printf("Enter a number: ");
    scanf("%d", &n);
    while (n != 0) {
        count += n & 1;
        n >>= 1;
    }
    printf("Number of set bits = %d", count);
    return 0;
}

// Task 65: Check if a number is a palindrome using recursion
#include <stdio.h>
int reverse(int n, int temp) {
    if (n == 0)
        return temp;
    temp = (temp * 10) + (n % 10);
    return reverse(n / 10, temp);
}
int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
    if (n == reverse(n, 0))
        printf("%d is a palindrome.", n);
    else
        printf("%d is not a palindrome.", n);
    return 0;
}

// Task 66: Calculate power of a number using recursion
#include <stdio.h>
long long power(int base, int exp) {
    if (exp == 0)
        return 1;
    return base * power(base, exp - 1);
}
int main() {
    int base, exp;
    printf("Enter base and exponent: ");
    scanf("%d %d", &base, &exp);
    printf("%d^%d = %lld", base, exp, power(base, exp));
    return 0;
}

// Task 67: Find the nth Fibonacci number using recursion
#include <stdio.h>
int fibonacci(int n) {
    if (n <= 1)
        return n;
    return fibonacci(n - 1) + fibonacci(n - 2);
}
int main() {
    int n;
    printf("Enter the term: ");
    scanf("%d", &n);
    printf("%dth Fibonacci number = %d", n, fibonacci(n));
    return 0;
}

// Task 68: Check if a string is palindrome using recursion
#include <stdio.h>
#include <string.h>
int isPalindrome(char str[], int start, int end) {
    if (start >= end)
        return 1;
    if (str[start] != str[end])
        return 0;
    return isPalindrome(str, start + 1, end - 1);
}
int main() {
    char str[100];
    printf("Enter a string: ");
    scanf("%s", str);
    if (isPalindrome(str, 0, strlen(str) - 1))
        printf("The string is a palindrome.");
    else
        printf("The string is not a palindrome.");
    return 0;
}

// Task 69: Find the sum of an array using recursion
#include <stdio.h>
int sumArray(int arr[], int n) {
    if (n == 0)
        return 0;
    return arr[n - 1] + sumArray(arr, n - 1);
}
int main() {
    int n;
    printf("Enter the number of elements: ");
    scanf("%d", &n);
    int arr[n];
    printf("Enter the elements: ");
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
    printf("Sum of array elements = %d", sumArray(arr, n));
    return 0;
}

// Task 70: Reverse an array using recursion
#include <stdio.h>
void reverseArray(int arr[], int start, int end) {
    if (start >= end)
        return;
    int temp = arr[start];
    arr[start] = arr[end];
    arr[end] = temp;
    reverseArray(arr, start + 1, end - 1);
}
int main() {
    int n;
    printf("Enter the number of elements: ");
    scanf("%d", &n);
    int arr[n];
    printf("Enter the elements: ");
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
    reverseArray(arr, 0, n - 1);
    printf("Reversed array: ");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }
    return 0;
}

// Task 71: Find the maximum element in an array using recursion
#include <stdio.h>
int findMax(int arr[], int n) {
    if (n == 1)
        return arr[0];
    int max = findMax(arr, n - 1);
    return (arr[n - 1] > max) ? arr[n - 1] : max;
}
int main() {
    int n;
    printf("Enter the number of elements: ");
    scanf("%d", &n);
    int arr[n];
    printf("Enter the elements: ");
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
    }
    printf("Maximum element = %d", findMax(arr, n));
    return 0;
}

// Task 72: Calculate the sum of digits of a number using recursion
#include <stdio.h>
int sumDigits(int n) {
    if (n == 0)
        return 0;
    return (n % 10) + sumDigits(n / 10);
}
int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
    printf("Sum of digits = %d", sumDigits(n));
    return 0;
}

// Task 73: Check if a number is prime using recursion
#include <stdio.h>
int isPrime(int n, int i) {
    if (n <= 2)
        return (n == 2) ? 1 : 0;
    if (n % i == 0)
        return 0;
    if (i * i > n)
        return 1;
    return isPrime(n, i + 1);
}
int main() {
    int n;
    printf("Enter a number: ");
    scanf("%d", &n);
    if (isPrime(n, 2))
        printf("%d is a prime number.", n);
    else
        printf("%d is not a prime number.", n);
    return 0;
}

// Task 74: Find the nth power of a number using recursion
#include <stdio.h>
long long power(int base, int exp) {
    if (exp == 0)
        return 1;
    return base * power(base, exp - 1);
}
int main() {
    int base, exp;
    printf("Enter base and exponent: ");
    scanf("%d %d", &base, &exp);
    printf("%d^%d = %lld", base, exp, power(base, exp));
    return 0;
}

