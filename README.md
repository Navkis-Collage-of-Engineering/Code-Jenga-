#!/bin/bash

# 🎮 Code Jenga: The Ultimate Coding Showdown! 🚀
# Welcome to Code Jenga, where teams manipulate code like a Jenga tower!
# Teams take turns removing one line (✂) or tweaking one character/operator (🔄).
# The code must compile/run and produce the exact same output.
# One wrong move, and the team is out! Last team standing wins!

# **1. Fibonacci Frenzy** 🧮
# Description: Compute the 7th Fibonacci number iteratively. 
# Can you pull a block without breaking the sequence?
: '
Code:
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

Expected Output:
The 7th Fibonacci number is 13

Safe Move (🔄 Tweak):
Change `for i in range(2, n + 1)` to `for _ in range(2, n + 1)`.
'

# **2. Even Squares Explosion** 💣
# Description: Sum the squares of even numbers. 
# Can you simplify without changing the result?
: '
Code:
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
squared_evens = [x**2 for x in numbers if x % 2 == 0]
summed = sum(squared_evens)
print(f"Sum of squares of even numbers: {summed}")

Expected Output:
Sum of squares of even numbers: 220

Safe Move (✂ Remove):
Remove `summed = sum(squared_evens)` and change the print to `print(f"Sum of squares of even numbers: {sum(squared_evens)}")`.
'

# **3. FizzBuzz Firestorm** 🔥
# Description: Print numbers 1 to 15 with fizzing rules. 
# Can you tweak without fizzling out?
: '
Code:
for i in range(1, 16):
    output = ""
    if i % 3 == 0:
        output += "Fizz"
    if i % 5 == 0:
        output += "Buzz"
    print(output if output else i)

Expected Output:
1
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
FizzBuzz

Safe Move (🔄 Tweak):
Change `output += "Buzz"` to `output = output + "Buzz"`.
'

# **4. Dictionary Dash** 📊
# Description: Compute the average of dictionary values. 
# Can you pull a block without skewing the average?
: '
Code:
data = {"a": 10, "b": 20, "c": 30}
total = 0
for key, value in data.items():
    total += value
average = total / len(data)
print(f"The average value is {average}")

Expected Output:
The average value is 20.0

Safe Move (🔄 Tweak):
Change `for key, value in data.items():` to `for value in data.values():`.
'

# **5. Inheritance Inferno** 🐶
# Description: Use inheritance to make a dog bark. 
# Can you remove a block without silencing it?
: '
Code:
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
    @Override
    void makeSound() {
        System.out.println("Woof!");
    }
}

Expected Output:
Woof!

Safe Move (✂ Remove):
Remove the `@Override` annotation.
'

# **6. Loop Lightning** ⚡
# Description: Count iterations in nested loops. 
# Can you tweak without losing count?
: '
Code:
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

Expected Output:
Total iterations: 9

Safe Move (🔄 Tweak):
Change inner loop variable from `j` to `i`.
'

# **7. Array Avalanche** 🌊
# Description: Find the largest element in a sorted array. 
# Can you tweak without missing the max?
: '
Code:
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        int[] numbers = {5, 2, 8, 1, 9};
        Arrays.sort(numbers);
        System.out.println("Largest element: " + numbers[numbers.length - 1]);
    }
}

Expected Output:
Largest element: 9

Safe Move (🔄 Tweak):
Change `numbers.length - 1` to `4`.
'

# **8. Ternary Tempest** 🌩
# Description: Use a ternary operator for pass/fail. 
# Can you add a block without failing?
: '
Code:
public class Main {
    public static void main(String[] args) {
        int score = 85;
        String result = (score >= 70) ? "Pass" : "Fail";
        System.out.println("Result: " + result);
    }
}

Expected Output:
Result: Pass

Safe Move (🔄 Tweak):
Change `(score >= 70)` to `((score >= 70))`.
'

# **9. Pointer Pandemonium** 🖥
# Description: Use pointers to print a value and address. 
# Can you tweak without dereferencing disaster?
: '
Code:
#include <stdio.h>

int main() {
    int a = 5;
    int *ptr = &a;
    
    printf("Value of a: %d\n", a);
    printf("Value via pointer: %d\n", *ptr);
    printf("Address of a: %p\n", (void*)&a);
    
    return 0;
}

Expected Output:
Value of a: 5
Value via pointer: 5
Address of a: <some address, e.g., 0x7fff5fbff83c>

Safe Move (🔄 Tweak):
Change `int a = 5` to `int a = 05`.
'

# **10. Macro Madness** 🛠
# Description: Use a macro to square an expression. 
# Can you tweak without squaring off?
: '
Code:
#include <stdio.h>
#define SQUARE(x) ((x) * (x))

int main() {
    int num = 5;
    int result = SQUARE(num + 1);
    printf("Square of %d + 1 is %d\n", num, result);
    return 0;
}

Expected Output:
Square of 5 + 1 is 36

Safe Move (🔄 Tweak):
Change `#define SQUARE(x) ((x) * (x))` to `#define SQUARE(x) ( ( x ) * ( x ) )`.
'

# **11. Switch Showdown** 📜
# Description: Print a grade message using a switch. 
# Can you tweak without switching outcomes?
: '
Code:
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

Expected Output:
Well done!

Safe Move (🔄 Tweak):
Change `case 'B':` to `case 66:`.
'

# **12. Loop Blitz** 🔄
# Description: Combine conditionals and loops to print messages. 
# Can you tweak without breaking the rhythm?
: '
Code:
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

Expected Output:
i is less than 15
Hello 0
Hello 1
Hello 2
Hello 3
Hello 4

Safe Move (🔄 Tweak):
Change `i++` to `++i` in the for loop.
'
