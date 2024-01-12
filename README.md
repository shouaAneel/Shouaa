# Shouaa
pf assignment
#include <stdio.h>
#include <math.h>

// Function declarations
double add(double a, double b);
double subtract(double a, double b);
double multiply(double a, double b);
double divide(double a, double b);
double sine(double angle);
double cosine(double angle);
double tangent(double angle);
double arcsine(double value);
double arccosine(double value);
double arctangent(double value);
double exponentiation(double base, double exponent);
double squareRoot(double value);
double cubeRoot(double value);
double nthRoot(double value, double n);
double factorial(double n);
double absoluteValue(double value);
double logarithm(double value);
double naturalLogarithm(double value);
double customBaseLogarithm(double base, double value);

int main() {
    int choice;
    double a, b, result;
    while (1) {
        // Display menu
        printf("\nScientific Calculator Menu:\n");
        printf("1. Addition\n");
        printf("2. Subtraction\n");
        printf("3. Multiplication\n");
        printf("4. Division\n");
        printf("5. Sine\n");
        printf("6. Cosine\n");
        printf("7. Tangent\n");
        printf("8. Arcsine\n");
        printf("9. Arccosine\n");
        printf("10. Arctangent\n");
        printf("11. Exponentiation\n");
        printf("12. Square root\n");
        printf("13. Cube root\n");
        printf("14. nth Root\n");
        printf("15. Factorial\n");
        printf("16. Absolute value\n");
        printf("17. Logarithm (base 10)\n");
        printf("18. Natural logarithm (base e)\n");
        printf("19. Custom base logarithm\n");
        printf("0. Exit\n");

        // Get user choice
        printf("Enter your choice: ");
        scanf("%d", &choice);
        // Perform the selected operation
        switch (choice) {
            case 0:
                printf("Exiting calculator. Goodbye!\n");
                return 0;
            case 1:
                printf("Enter two numbers: ");
                scanf("%lf %lf", &a, &b);
                result = add(a, b);
                printf("Result: %lf\n", result);
                break;
            case 2:
                printf("Enter two numbers: ");
                scanf("%lf %lf", &a, &b);
                result = subtract(a, b);
                printf("Result: %lf\n", result);
                break;
            case 3:
                printf("Enter two numbers: ");
                scanf("%lf %lf", &a, &b);
                result = multiply(a, b);
                printf("Result: %lf\n", result);
                break;
            case 4:
                printf("Enter two numbers: ");
                scanf("%lf %lf", &a, &b);
                if (b != 0) {
                    result = divide(a, b);
                    printf("Result: %lf\n", result);
                } else {
                    printf("Error: Division by zero.\n");
                }
                break;
            case 5:
                printf("Enter angle in degrees: ");
                scanf("%lf", &a);
                result = sine(a);
                printf("Result: %lf\n", result);
                break;
            case 6:
                printf("Enter angle in degrees: ");
                scanf("%lf", &a);
                result = cosine(a);
                printf("Result: %lf\n", result);
                break;
            case 7:
                printf("Enter angle in degrees: ");
                scanf("%lf", &a);
                result = tangent(a);
                printf("Result: %lf\n", result);
                break;
            case 8:
                printf("Enter value: ");
                scanf("%lf", &a);
                result = arcsine(a);
                printf("Result: %lf\n", result);
                break;
            case 9:
                printf("Enter value: ");
                scanf("%lf", &a);
                result = arccosine(a);
                printf("Result: %lf\n", result);
                break;
            case 10:
                printf("Enter value: ");
                scanf("%lf", &a);
                result = arctangent(a);
                printf("Result: %lf\n", result);
                break;
            case 11:
                printf("Enter base and exponent: ");
                scanf("%lf %lf", &a, &b);
                result = exponentiation(a, b);
                printf("Result: %lf\n", result);
                break;
            case 12:
                printf("Enter value: ");
                scanf("%lf", &a);
                result = squareRoot(a);
                printf("Result: %lf\n", result);
                break;
            case 13:
                printf("Enter value: ");
                scanf("%lf", &a);
                result = cubeRoot(a);
                printf("Result: %lf\n", result);
                break;
            case 14:
                printf("Enter value and root (n): ");
                scanf("%lf %lf", &a, &b);
                result = nthRoot(a, b);
                printf("Result: %lf\n", result);
                break;
            case 15:
                printf("Enter a number: ");
                scanf("%lf", &a);
                result = factorial(a);
                printf("Result: %lf\n", result);
                break;
            case 16:
                printf("Enter a number: ");
                scanf("%lf", &a);
                result = absoluteValue(a);
                printf("Result: %lf\n", result);
                break;
            case 17:
                printf("Enter a number: ");
                scanf("%lf", &a);
                result = logarithm(a);
                printf("Result: %lf\n", result);
                break;
            case 18:
                printf("Enter a number: ");
                scanf("%lf", &a);
                result = naturalLogarithm(a);
                printf("Result: %lf\n", result);
                break;
            case 19:
                printf("Enter base and value: ");
                scanf("%lf %lf", &a, &b);
                result = customBaseLogarithm(a, b);
                printf("Result: %lf\n", result);
                break;
            default:
                printf("Invalid choice. Please try again.\n");
                break;
        }
    }

    return 0;
}

// Function definitions
double add(double a, double b) {
    return a + b;
}
double subtract(double a, double b) {
    return a - b;
}
double multiply(double a, double b) {
    return a * b;
}
double divide(double a, double b) {
    return a / b;
}
double sine(double angle) {
    return sin(angle * M_PI / 180.0);
}
double cosine(double angle) {
    return cos(angle * M_PI / 180.0);
}
double tangent(double angle) {
    return tan(angle * M_PI / 180.0);
}
double arcsine(double value) {
    return asin(value) * 180.0 / M_PI;
}
double arccosine(double value) {
    return acos(value) * 180.0 / M_PI;
}
double arctangent(double value) {
    return atan(value) * 180.0 / M_PI;
}

double exponentiation(double base, double exponent) {
    return pow(base, exponent);
}
double squareRoot(double value) {
    return sqrt(value);
}
double cubeRoot(double value) {
    return cbrt(value);
}
double nthRoot(double value, double n) {
    return pow(value, 1.0 / n);
}
double factorial(double n) {
    if (n < 0) {
        return 0; // Error: Factorial of a negative number is undefined.
    } else if (n == 0 || n == 1) {
        return 1;
    } else {
        return n * factorial(n - 1);
    }
}
double absoluteValue(double value) {
    return fabs(value);
}
double logarithm(double value) {
    return log10(value);
}
double naturalLogarithm(double value) {
    return log(value);
}

double customBaseLogarithm(double base, double value) {
    return log(value) / log(base);
}

