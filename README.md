# calculator
EXPLANATION:                                                                                                                                                                                                   This Java program is a simple console-based calculator that performs basic arithmetic operations such as addition, subtraction, multiplication, and division. It uses the Scanner class to take user input from the console. The user is first prompted to enter two numbers and then choose an operator (+, -, *, or /). Based on the selected operator, the program uses a switch statement to determine which mathematical operation to perform. The result of the operation is then displayed on the screen. The program also includes a basic error check to prevent division by zero, which would otherwise cause a runtime error. Overall, this calculator program demonstrates the use of variables, user input, conditional logic, and basic control flow in Java.
CODE:
import java.util.Scanner;

public class Calculator {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
        double num1, num2, result;
        char operator;

        System.out.print("Enter first number: ");
        num1 = input.nextDouble();

        System.out.print("Enter an operator (+, -, *, /): ");
        operator = input.next().charAt(0);

        System.out.print("Enter second number: ");
        num2 = input.nextDouble();

        switch (operator) {
            case '+':
                result = num1 + num2;
                System.out.println("Result: " + result);
                break;

            case '-':
                result = num1 - num2;
                System.out.println("Result: " + result);
                break;

            case '*':
                result = num1 * num2;
                System.out.println("Result: " + result);
                break;

            case '/':
                if (num2 != 0) {
                    result = num1 / num2;
                    System.out.println("Result: " + result);
                } else {
                    System.out.println("Error: Division by zero!");
                }
                break;

            default:
                System.out.println("Invalid operator!");
                break;
        }

        input.close();
    }
}
