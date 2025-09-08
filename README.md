# Code Jenga: Executable Challenge Shells 🎮


**Note**: For Challenge 9, the memory address in the output varies between runs due to dynamic memory allocation.

---

 1: Fibonacci Frenzy 🧮
**🔥 Question**: Compute the 7th Fibonacci number iteratively.

```python
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
textThe 7th Fibonacci number is 13



2: Even Squares Explosion 💣
🔥 Question: Sum the squares of even numbers.

numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
squared_evens = [x**2 for x in numbers if x % 2 == 0]
summed = sum(squared_evens)
print(f"Sum of squares of even numbers: {summed}")
Expected Output:
Sum of squares of even numbers: 220



3: FizzBuzz Firestorm 🔥
🔥 Question: Print numbers 1 to 15 with "Fizz" for multiples of 3, "Buzz" for multiples of 5, and "FizzBuzz" for multiples of both.
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



4: Dictionary Dash 📊
🔥 Question: Compute the average of dictionary values.
data = {"a": 10, "b": 20, "c": 30}
total = 0
for key, value in data.items():
    total += value
average = total / len(data)
print(f"The average value is {average}")
Expected Output:
textThe average value is 20.0



5: Inheritance Inferno 🐶
🔥 Question: Use inheritance to make a dog bark.
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




 6: Loop Lightning ⚡
🔥 Question: Count iterations in nested loops.
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




 7: Array Avalanche 🌊
🔥 Question: Find the largest element in a sorted array.
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



 8: Ternary Tempest 🌩
🔥 Question: Use a ternary operator for pass/fail.
public class Main {
    public static void main(String[] args) {
        int score = 85;
        String result = (score >= 70) ? "Pass" : "Fail";
        System.out.println("Result: " + result);
    }
}
Expected Output:
Result: Pass



 9: Pointer Pandemonium 🖥
🔥 Question: Use pointers to print a value and address.
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
Note: The memory address varies between runs due to dynamic memory allocation.





10: Macro Madness 🛠
🔥 Question: Use a macro to square an expression.
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




 11: Switch Showdown 📜
🔥 Question: Print a grade message using a switch.
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



 12: Loop Blitz 🔄
🔥 Question: Combine conditionals and loops to print messages.
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
