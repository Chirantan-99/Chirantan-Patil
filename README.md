Exception Handling Demo

This project demonstrates the core concepts of exception handling using the following keywords:

try

catch

finally

throw

throws

Exception handling is essential for building reliable applications, preventing unexpected crashes, and ensuring proper flow even when errors occur.

📘 Features Covered
✔ try Block

Used to enclose code that might throw an exception.

✔ catch Block

Used to handle specific or general exceptions thrown inside the try block.

✔ finally Block

Executes whether an exception occurs or not—commonly used for cleanup tasks like closing files or database connections.

✔ throw Keyword

Used to explicitly throw an exception from your code.

✔ throws Keyword

Used in method definitions to indicate that the method may throw certain exceptions, delegating handling to the calling code.

📂 Code Example
public class ExceptionDemo {

    // Method that declares an exception using 'throws'
    public static int divide(int a, int b) throws ArithmeticException {
        if (b == 0) {
            // Explicitly throwing an exception using 'throw'
            throw new ArithmeticException("Cannot divide by zero!");
        }
        return a / b;
    }

    public static void main(String[] args) {
        try {
            int result = divide(10, 0); // This will cause an exception
            System.out.println("Result: " + result);
        } 
        catch (ArithmeticException e) {
            System.out.println("Error occurred: " + e.getMessage());
        } 
        finally {
            System.out.println("Execution completed. Cleaning up...");
        }
    }
}

📝 Explanation
1. try Block

Encapsulates the risky code:

try {
    int result = divide(10, 0);
}

2. catch Block

Executes only when an exception occurs:

catch (ArithmeticException e) {
    System.out.println("Error occurred: " + e.getMessage());
}

3. finally Block

Runs regardless of whether an exception was thrown:

finally {
    System.out.println("Execution completed. Cleaning up...");
}

4. throw Keyword

Manually throwing a new exception:

throw new ArithmeticException("Cannot divide by zero!");

5. throws Keyword

Declares that the method may produce an exception:

public static int divide(int a, int b) throws ArithmeticException

🧪 How to Run

Clone or download this project.

Compile the Java file:

javac ExceptionDemo.java


Run the program:

java ExceptionDemo
