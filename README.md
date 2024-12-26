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
    }
    if (a > b && a > c)
        printf("%d is the greatest\n", a);
    else if (b > a && b > c)
        printf("%d is the greatest\n", b);
    else
        printf("%d is the greatest\n", c);
}

// 11. Grading based on percentage using if-else
void gradePercentage() {
    float percentage;
    printf("Enter percentage: ");
    if (scanf("%f", &percentage) != 1 || percentage < 0 || percentage > 100) {
        printf("Invalid input.\n");
        return;
    }
    if (percentage >= 90)
        printf("Grade: A\n");
    else if (percentage >= 80)
        printf("Grade: B\n");
    else if (percentage >= 70)
        printf("Grade: C\n");
    else if (percentage >= 60)
        printf("Grade: D\n");
    else
        printf("Grade: F\n");
}

// 12. Display greeting using switch-case
void greetingSwitchCase() {
    int option;
    printf("Enter 1 for Salaam, 2 for Aadab, 3 for Hello: ");
    if (scanf("%d", &option) != 1) {
        printf("Invalid input.\n");
        return;
    }
    switch (option) {
    case 1:
        printf("Salaam\n");
        break;
    case 2:
        printf("Aadab\n");
        break;
    case 3:
        printf("Hello\n");
        break;
    default:
        printf("Incorrect option\n");
    }
}

// 13. Display series 1 2 3 4 ... n
void displaySeries() {
    int n;
    printf("Enter n: ");
    if (scanf("%d", &n) != 1 || n <= 0) {
        printf("Invalid input.\n");
        return;
    }
    for (int i = 1; i <= n; i++) {
        printf("%d ", i);
    }
    printf("\n");
}
