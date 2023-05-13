#include <stdio.h>
#include <math.h>

int main() {
   int choice;
   double num, result;

   printf("Welcome to the Scientific Calculator\n");
   printf("Select an operation to perform:\n");
   printf("1. Square Root\n");
   printf("2. Exponential\n");
   printf("3. Natural Logarithm (base e)\n");
   printf("4. Logarithm (base 10)\n");
   printf("5. Sine\n");
   printf("6. Cosine\n");
   printf("7. Tangent\n");
   printf("8. Quit\n");

   do {
      printf("\nEnter your choice: ");
      scanf("%d", &choice);

      switch(choice) {
         case 1:
            printf("Enter a number: ");
            scanf("%lf", &num);
            result = sqrt(num);
            printf("Square root of %.2lf is %.2lf\n", num, result);
            break;

         case 2:
            printf("Enter a number: ");
            scanf("%lf", &num);
            result = exp(num);
            printf("Exponential of %.2lf is %.2lf\n", num, result);
            break;

         case 3:
            printf("Enter a number: ");
            scanf("%lf", &num);
            result = log(num);
            printf("Natural logarithm of %.2lf is %.2lf\n", num, result);
            break;

         case 4:
            printf("Enter a number: ");
            scanf("%lf", &num);
            result = log10(num);
            printf("Logarithm (base 10) of %.2lf is %.2lf\n", num, result);
            break;

         case 5:
            printf("Enter a number (in radians): ");
            scanf("%lf", &num);
            result = sin(num);
            printf("Sine of %.2lf is %.2lf\n", num, result);
            break;

         case 6:
            printf("Enter a number (in radians): ");
            scanf("%lf", &num);
            result = cos(num);
            printf("Cosine of %.2lf is %.2lf\n", num, result);
            break;

         case 7:
            printf("Enter a number (in radians): ");
            scanf("%lf", &num);
            result = tan(num);
            printf("Tangent of %.2lf is %.2lf\n", num, result);
            break;

         case 8:
            printf("Thank you for using the calculator\n");
            break;

         default:
            printf("Invalid choice. Please try again.\n");
            break;
      }
   } while (choice != 8);

   return 0;
}
