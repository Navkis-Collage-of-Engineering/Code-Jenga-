#!/bin/bash
# =====================================================
# Code Jenga: 12 Programming Challenges 🚀
# All challenges in one shell script file
# Each challenge has question, code, and expected output
# =====================================================

# ---------------- Challenge 1 ----------------
echo "1. Fibonacci Frenzy 🧮"
echo "Question: Compute the 7th Fibonacci number iteratively."
echo
cat <<'PYTHON1'
def fibonacci(n):
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    else:
        a, b = 0, 1
        for i in range(2, n + 1):
            c = a + b
            a = b
            b = c
        return b

result = fibonacci(7)
print(f"The 7th Fibonacci number is {result}")
PYTHON1
echo
echo "Expected Output:"
echo "The 7th Fibonacci number is 13"
echo
# ---------------- Challenge 2 ----------------
echo "2. Even Squares Explosion 💣"
echo "Question: Sum the squares of even numbers."
echo
cat <<'PYTHON2'
numbers = [1,2,3,4,5,6,7,8,9,10]
squared_evens = [x**2 for x in numbers if x % 2 == 0]
summed = sum(squared_evens)
print(f"Sum of squares of even numbers: {summed}")
PYTHON2
echo
echo "Expected Output:"
echo "Sum of squares of even numbers: 220"
echo
# ---------------- Challenge 3 ----------------
echo "3. FizzBuzz Firestorm 🔥"
echo "Question: Print numbers 1 to 15 with 'Fizz' for multiples of 3, 'Buzz' for multiples of 5, 'FizzBuzz' for both."
echo
cat <<'PYTHON3'
for i in range(1, 16):
    output = ""
    if i % 3 == 0:
        output += "Fizz"
    if i % 5 == 0:
        output += "Buzz"
    print(output if output else i)
PYTHON3
echo
echo "Expected Output:"
echo "1
2
Fizz
4
Buzz
Fizz
7
8
Fizz
Buzz
11
Fizz
13
14
FizzBuzz"
echo
# ---------------- Challenge 4 ----------------
echo "4. Dictionary Dash 📊"
echo "Question: Compute the average of dictionary values."
echo
cat <<'PYTHON4'
data = {"a": 10, "b": 20, "c": 30}
total = 0
for key, value in data.items():
    total += value
average = total / len(data)
print(f"The average value is {average}")
PYTHON4
echo
echo "Expected Output:"
echo "The average value is 20.0"
echo
# ---------------- Challenge 5 ----------------
echo "5. Inheritance Inferno 🐶"
echo "Question: Use inheritance to make a dog bark."
echo
cat <<'JAVA5'
public class Main {
    public static void main(String[] args) {
        Animal myDog = new Dog();
        myDog.makeSound();
    }
}

class Animal {
    void makeSound() {
        System.out.println("Some generic animal sound");
    }
}

class Dog extends Animal {
    void makeSound() {
        System.out.println("Woof!");
    }
}
JAVA5
echo
echo "Expected Output:"
echo "Woof!"
echo
# ---------------- Challenge 6 ----------------
echo "6. Loop Lightning ⚡"
echo "Question: Count iterations in nested loops."
echo
cat <<'JAVA6'
public class Main {
    public static void main(String[] args) {
        int count = 0;
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                count++;
            }
        }
        System.out.println("Total iterations: " + count);
    }
}
JAVA6
echo
echo "Expected Output:"
echo "Total iterations: 9"
echo
# ---------------- Challenge 7 ----------------
echo "7. Array Avalanche 🌊"
echo "Question: Find the largest element in a sorted array."
echo
cat <<'JAVA7'
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        int[] numbers = {5, 2, 8, 1, 9};
        Arrays.sort(numbers);
        System.out.println("Largest element: " + numbers[numbers.length - 1]);
    }
}
JAVA7
echo
echo "Expected Output:"
echo "Largest element: 9"
echo
# ---------------- Challenge 8 ----------------
echo "8. Ternary Tempest 🌩"
echo "Question: Use a ternary operator for pass/fail."
echo
cat <<'JAVA8'
public class Main {
    public static void main(String[] args) {
        int score = 85;
        String result = (score >= 70) ? "Pass" : "Fail";
        System.out.println("Result: " + result);
    }
}
JAVA8
echo
echo "Expected Output:"
echo "Result: Pass"
echo
# ---------------- Challenge 9 ----------------
echo "9. Pointer Pandemonium 🖥"
echo "Question: Use pointers to print a value and address."
echo
cat <<'C9'
#include <stdio.h>

int main() {
    int a = 5;
    int *ptr = &a;
    
    printf("Value of a: %d\n", a);
    printf("Value via pointer: %d\n", *ptr);
    printf("Address of a: %p\n", (void*)&a);
    
    return 0;
}
C9
echo
echo "Expected Output:"
echo "Value of a: 5
Value via pointer: 5
Address of a: <some address, varies each run>"
echo
# ---------------- Challenge 10 ----------------
echo "10. Macro Madness 🛠"
echo "Question: Use a macro to square an expression."
echo
cat <<'C10'
#include <stdio.h>
#define SQUARE(x) ((x) * (x))

int main() {
    int num = 5;
    int result = SQUARE(num + 1);
    printf("Square of %d + 1 is %d\n", num, result);
    return 0;
}
C10
echo
echo "Expected Output:"
echo "Square of 5 + 1 is 36"
echo
# ---------------- Challenge 11 ----------------
echo "11. Switch Showdown 📜"
echo "Question: Print a grade message using a switch."
echo
cat <<'C11'
#include <stdio.h>

int main() {
    char grade = 'B';
    
    switch (grade) {
        case 'A':
            printf("Excellent!\n");
            break;
        case 'B':
            printf("Well done!\n");
            break;
        case 'C':
            printf("Good!\n");
            break;
        default:
            printf("Invalid grade\n");
    }
    
    return 0;
}
C11
echo
echo "Expected Output:"
echo "Well done!"
echo
# ---------------- Challenge 12 ----------------
echo "12. Loop Blitz 🔄"
echo "Question: Combine conditionals and loops to print messages."
echo
cat <<'C12'
#include <stdio.h>

int main() {
    int i = 10;
    
    if (i < 15) {
        printf("i is less than 15\n");
    } else {
        printf("i is greater than 15\n");
    }
    
    for (i = 0; i < 5; i++) {
        printf("Hello %d\n", i);
    }
    
    return 0;
}
C12
echo
echo "Expected Output:"
echo "i is less than 15
Hello 0
Hello 1
Hello 2
Hello 3
Hello 4"
echo
