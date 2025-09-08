#!/bin/bash
# =====================================================
# Code Jenga: 12 Programming Challenges 🚀
# All challenges in ONE file with question, code, and expected output
# =====================================================

echo "================ Challenge 1: Fibonacci Frenzy 🧮 ================"
echo "Question: Compute the 7th Fibonacci number iteratively."
echo
echo "Code:"
echo 'def fibonacci(n):
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
print(f"The 7th Fibonacci number is {result}")'
echo
echo "Expected Output:"
echo "The 7th Fibonacci number is 13"
echo

echo "================ Challenge 2: Even Squares Explosion 💣 ================"
echo "Question: Sum the squares of even numbers."
echo
echo "Code:"
echo 'numbers = [1,2,3,4,5,6,7,8,9,10]
squared_evens = [x**2 for x in numbers if x % 2 == 0]
summed = sum(squared_evens)
print(f"Sum of squares of even numbers: {summed}")'
echo
echo "Expected Output:"
echo "Sum of squares of even numbers: 220"
echo

echo "================ Challenge 3: FizzBuzz Firestorm 🔥 ================"
echo "Question: Print numbers 1 to 15 with Fizz/Buzz rules."
echo
echo "Code:"
echo 'for i in range(1, 16):
    output = ""
    if i % 3 == 0:
        output += "Fizz"
    if i % 5 == 0:
        output += "Buzz"
    print(output if output else i)'
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

echo "================ Challenge 4: Dictionary Dash 📊 ================"
echo "Question: Compute the average of dictionary values."
echo
echo "Code:"
echo 'data = {"a": 10, "b": 20, "c": 30}
total = 0
for key, value in data.items():
    total += value
average = total / len(data)
print(f"The average value is {average}")'
echo
echo "Expected Output:"
echo "The average value is 20.0"
echo

echo "================ Challenge 5: Inheritance Inferno 🐶 ================"
echo "Question: Use inheritance to make a dog bark."
echo
echo "Code:"
echo 'public class Main {
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
}'
echo
echo "Expected Output:"
echo "Woof!"
echo

echo "================ Challenge 6: Loop Lightning ⚡ ================"
echo "Question: Count iterations in nested loops."
echo
echo "Code:"
echo 'public class Main {
    public static void main(String[] args) {
        int count = 0;
        for (int i = 0; i < 3; i++) {
            for (int j = 0; j < 3; j++) {
                count++;
            }
        }
        System.out.println("Total iterations: " + count);
    }
}'
echo
echo "Expected Output:"
echo "Total iterations: 9"
echo

echo "================ Challenge 7: Array Avalanche 🌊 ================"
echo "Question: Find the largest element in a sorted array."
echo
echo "Code:"
echo 'import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        int[] numbers = {5, 2, 8, 1, 9};
        Arrays.sort(numbers);
        System.out.println("Largest element: " + numbers[numbers.length - 1]);
    }
}'
echo
echo "Expected Output:"
echo "Largest element: 9"
echo

echo "================ Challenge 8: Ternary Tempest 🌩 ================"
echo "Question: Use a ternary operator for pass/fail."
echo
echo "Code:"
echo 'public class Main {
    public static void main(String[] args) {
        int score = 85;
        String result = (score >= 70) ? "Pass" : "Fail";
        System.out.println("Result: " + result);
    }
}'
echo
echo "Expected Output:"
echo "Result: Pass"
echo

echo "================ Challenge 9: Pointer Pandemonium 🖥 ================"
echo "Question: Use pointers to print a value and address."
echo
echo "Code:"
echo '#include <stdio.h>

int main() {
    int a = 5;
    int *ptr = &a;
    
    printf("Value of a: %d\n", a);
    printf("Value via pointer: %d\n", *ptr);
    printf("Address of a: %p\n", (void*)&a);
    
    return 0;
}'
echo
echo "Expected Output:"
echo "Value of a: 5
Value via pointer: 5
Address of a: <some address, varies each run>"
echo

echo "================ Challenge 10: Macro Madness 🛠 ================"
echo "Question: Use a macro to square an expression."
echo
echo "Code:"
echo '#include <stdio.h>
#define SQUARE(x) ((x) * (x))

int main() {
    int num = 5;
    int result = SQUARE(num + 1);
    printf("Square of %d + 1 is %d\n", num, result);
    return 0;
}'
echo
echo "Expected Output:"
echo "Square of 5 + 1 is 36"
echo

echo "================ Challenge 11: Switch Showdown 📜 ================"
echo "Question: Print a grade message using a switch."
echo
echo "Code:"
echo '#include <stdio.h>

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
}'
echo
echo "Expected Output:"
echo "Well done!"
echo

echo "================ Challenge 12: Loop Blitz 🔄 ================"
echo "Question: Combine conditionals and loops to print messages."
echo
echo "Code:"
echo '#include <stdio.h>

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
}'
echo
echo "Expected Output:"
echo "i is less than 15
Hello 0
Hello 1
Hello 2
Hello 3
Hello 4"
echo
