# Task-05-Roll--24070103-
### Post Lab Exercise Breakdown for GitHub README

Here is a breakdown of how the Java programs for the listed problems should be structured and implemented, including their explanations for your GitHub README file.

---

# **Post Lab Exercises - Java Programs**

## **1. Fahrenheit to Celsius Converter**

### **Problem:**
Write a Java program to convert temperature from Fahrenheit to Celsius.

### **Test Data:**
Input: 212  
Expected Output:  
```
212.0 degree Fahrenheit is equal to 100.0 in Celsius
```

### **Solution:**
This program reads the temperature in Fahrenheit and then uses the formula to convert it to Celsius. The formula is:
```
Celsius = (Fahrenheit - 32) * 5/9
```

### **Code:**
```java
import java.util.Scanner;

public class FahrenheitToCelsius {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Input a degree in Fahrenheit: ");
        double fahrenheit = scanner.nextDouble();
        
        double celsius = (fahrenheit - 32) * 5 / 9;
        
        System.out.println(fahrenheit + " degree Fahrenheit is equal to " + celsius + " in Celsius");
    }
}
```

---

## **2. Leap Year Check**

### **Problem:**
Write a program to test whether a year is a leap year or not.

### **Solution:**
A leap year is divisible by 4, except for years divisible by 100, unless they are also divisible by 400.

### **Code:**
```java
import java.util.Scanner;

public class LeapYear {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a year: ");
        int year = scanner.nextInt();
        
        if ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0)) {
            System.out.println(year + " is a leap year.");
        } else {
            System.out.println(year + " is not a leap year.");
        }
    }
}
```

---

## **3. Evaluate the Series `1^2 + 3^2 + 5^2 + ...` Up to n Terms**

### **Problem:**
Write a program to evaluate the following series:  
`1 + 32 + 52 + ...` up to `n` terms.

### **Solution:**
The series increases by 20 at each step:  
1, 3^2, 5^2, 7^2, ...

### **Code:**
```java
public class SERIES1 {

    public static int sumOfSquares(int n) {
        int sum = 0;

        // Iterate over the first n odd numbers
        for (int i = 1; i <= n; i++) {
            int oddNumber = 2 * i - 1;  // Generate the i-th odd number
            sum += oddNumber * oddNumber;  // Add its square to the sum
        }

        return sum;
    }

    public static void main(String[] args) {
        int n = 5;  // Change this value to calculate for different n
        int result = sumOfSquares(n);
        System.out.println("The sum of squares of the first " + n + " odd numbers is: " + result);
    }
}


## **4. Evaluate the Series `1 - 2 + 3 - 4 + ...` Up to n Terms**

### **Problem:**
Write a program to evaluate the following series:  
`1 - 2 + 3 - 4 + ...` up to `n` terms.

### **Solution:**
The terms alternate between positive and negative numbers. 

### **Code:**
```java
import java.util.Scanner;

public class AlternatingSeriesSum {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the number of terms: ");
        int n = scanner.nextInt();
        
        int sum = 0;
        for (int i = 1; i <= n; i++) {
            if (i % 2 == 0) {
                sum -= i;  // Subtract even terms
            } else {
                sum += i;  // Add odd terms
            }
        }
        
        System.out.println("Sum of the series is: " + sum);
    }
}
```

---

## **5. Find the Factorial of a Number**

### **Problem:**
Write a program to find the factorial of a number.

### **Solution:**
The factorial of a number `n` is the product of all positive integers from `1` to `n`. For example, `5! = 5 * 4 * 3 * 2 * 1`.

### **Code:**
```java
import java.util.Scanner;

public class Factorial {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter a number: ");
        int number = scanner.nextInt();
        
        long factorial = 1;
        for (int i = 1; i <= number; i++) {
            factorial *= i;
        }
        
        System.out.println("Factorial of " + number + " is: " + factorial);
    }
}
```

---

## **6. Find the Power of a Number**

### **Problem:**
Write a program to find the power for a given base and exponent.

### **Solution:**
Use the formula:  
`power = base ^ exponent` (base raised to the power of exponent).

### **Code:**
```java
import java.util.Scanner;

public class Power {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter base: ");
        int base = scanner.nextInt();
        System.out.print("Enter exponent: ");
        int exponent = scanner.nextInt();
        
        long result = 1;
        for (int i = 1; i <= exponent; i++) {
            result *= base;
        }
        
        System.out.println(base + " raised to the power of " + exponent + " is: " + result);
    }
}
```

---

## **7. Find the Bangla Season Based on the Month**

### **Problem:**
Write a program to find the Bangla season from a given month using `if/switch`.

### **Solution:**
The months are categorized into seasons in the Bangla calendar. For example, months from January to March may be considered `Winter`, and so on.

### **Code:**
```java
import java.util.Scanner;

public class BanglaSeason {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter month number (1-12): ");
        int month = scanner.nextInt();
        
        String season;
        switch (month) {
            case 1: case 2: case 3: season = "Winter"; break;
            case 4: case 5: season = "Spring"; break;
            case 6: case 7: season = "Summer"; break;
            case 8: case 9: season = "Rainy"; break;
            case 10: case 11: season = "Autumn"; break;
            case 12: season = "Winter"; break;
            default: season = "Invalid month"; break;
        }
        
        System.out.println("The Bangla season for month " + month + " is: " + season);
    }
}
```

---

## **8. Find the Largest Number in an Array**

### **Problem:**
Write a program to find the largest number in a list of numbers (array).

### **Solution:**
The program will iterate through the array and find the maximum value.

### **Code:**
```java
import java.util.Scanner;

public class LargestNumber {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the number of elements: ");
        int n = scanner.nextInt();
        
        int[] numbers = new int[n];
        System.out.println("Enter the numbers:");
        for (int i = 0; i < n; i++) {
            numbers[i] = scanner.nextInt();
        }
        
        int largest = numbers[0];
        for (int i = 1; i < n; i++) {
            if (numbers[i] > largest) {
                largest = numbers[i];
            }
        }
        
        System.out.println("The largest number is: " + largest);
    }
}
```

---

## **9. Sort Numbers in Ascending Order**

### **Problem:**
Write a program to sort numbers in ascending order.

### **Solution:**
We will use a simple sorting algorithm like Bubble Sort or Arrays.sort.

### **Code:**
```java
import java.util.Scanner;
import java.util.Arrays;

public class SortNumbers {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.print("Enter the number of elements: ");
        int n = scanner.nextInt();
        
        int[] numbers = new int[n];
        System.out.println("Enter the numbers:");
        for (int i = 0; i < n; i++) {
            numbers[i] = scanner.nextInt();
        }
        
        Arrays.sort(numbers);
        
        System.out.println("Sorted numbers in ascending order: ");
        for (int number : numbers) {
            System.out.print(number + " ");
        }
    }
}
```

---

### Conclusion:
These Java programs cover a variety of basic concepts such as loops, conditional statements, and array manipulation. You can copy these examples to your own repository and customize them as per your requirements.


