#!/bin/bash

# Exit on any error
set -e

# Directory for the project
REPO_DIR="code-jenga"
REPO_URL="https://github.com/yourusername/code-jenga.git" # Replace with your repository URL

# Create project directory
echo "Creating project directory: $REPO_DIR"
mkdir -p "$REPO_DIR"
cd "$REPO_DIR"

# Create README.md with all 12 Code Jenga challenges
echo "Creating README.md"
cat > README.md << 'EOF'
# 🎮 Code Jenga: The Ultimate Coding Showdown! 🚀

Welcome to **Code Jenga**, where coding meets strategy! Teams take turns pulling or tweaking a single "block" of code—**one line** or **one character/operator**—while keeping the program running and its output **unchanged**. One wrong move, and the tower **crashes**! 💥

## 🎯 Rules
- **Teams**: Take turns removing (✂) one line or tweaking (🔄) one character/operator (e.g., `+` to `-`, `i` to `j`).
- **Validation**: Code must **compile/run** without errors and produce the **exact same output** (content and format).
- **Failure**: A compilation error or altered output eliminates the team.
- **Victory**: The last team standing wins!
- **Tweak Clarification**: A tweak is a single character, operator, or logical unit (e.g., `.items()` to `.values()`).

Below are **12 thrilling challenges** in Python, Java, and C. Each includes the code, output, a safe move, and why it works. Get ready to test your coding precision! 🧠

---

## **1. Fibonacci Frenzy** 🧮
**Description**: Compute the 7th Fibonacci number iteratively. Can you pull a block without breaking the sequence?

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
```

**Output**:
```
The 7th Fibonacci number is 13
```

**Safe Move (🔄 Tweak)**: Change `for i in range(2, n + 1)` to `for _ in range(2, n + 1)`.

**Why It Works**: The loop variable `i` is unused in the loop body. Using `_` (a Python placeholder) keeps the calculation intact.

**Risks**: Removing `a = b` or tweaking `n + 1` to `n` disrupts the Fibonacci sequence.

---

## **2. Even Squares Explosion** 💣
**Description**: Sum the squares of even numbers. Can you simplify without changing the result?

```python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
squared_evens = [x**2 for x in numbers if x % 2 == 0]
summed = sum(squared_evens)
print(f"Sum of squares of even numbers: {summed}")
```

**Output**:
```
Sum of squares of even numbers: 220
```

**Safe Move (✂ Remove)**: Remove `summed = sum(squared_evens)` and change the print to `print(f"Sum of squares of even numbers: {sum(squared_evens)}")`.

**Why It Works**: The variable `summed` is only used in the print. Inlining the `sum` call preserves the output.

**Risks**: Removing `if x % 2 == 0` includes odd numbers’ squares, altering the result.

---

## **3. FizzBuzz Firestorm** 🔥
**Description**: Print numbers 1 to 15, with "Fizz" for multiples of 3, "Buzz" for 5, and "FizzBuzz" for both. Can you tweak without fizzling out?

```python
for i in range(1, 16):
    output = ""
    if i % 3 == 0:
        output += "Fizz"
    if i % 5 == 0:
        output += "Buzz"
    print(output if output else i)
```

**Output**:
```
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
```

**Safe Move (🔄 Tweak)**: Change `output += "Buzz"` to `output = output + "Buzz"`.

**Why It Works**: Both concatenation methods are equivalent, keeping the FizzBuzz logic intact.

**Risks**: Changing `if` to `elif` for the second condition breaks "FizzBuzz" for multiples of 15.

---

## **4. Dictionary Dash** 📊
**Description**: Compute the average of dictionary values. Can you pull a block without skewing the average?

```python
data = {'a': 10, 'b': 20, 'c': 30}
total = 0
for key, value in data.items():
    total += value
average = total / len(data)
print(f"The average value is {average}")
```

**Output**:
```
The average value is 20.0
```

**Safe Move (🔄 Tweak)**: Change `for key, value in data.items():` to `for value in data.values():`.

**Why It Works**: The `key` variable is unused. Using `data.values()` iterates directly over values, preserving the average.

**Risks**: Removing `total += value` breaks the sum calculation.

---

## **5. Inheritance Inferno** 🐶
**Description**: Use inheritance to make a dog bark. Can you remove a block without silencing it?

```java
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
```

**Output**:
```
Woof!
```

**Safe Move (✂ Remove)**: Remove the `@Override` annotation.

**Why It Works**: `@Override` is a compiler hint and doesn’t affect runtime behavior. The method still overrides correctly.

**Risks**: Removing `extends Animal` causes a compilation error.

---

## **6. Loop Lightning** ⚡
**Description**: Count iterations in nested loops. Can you tweak without losing count?

```java
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
```

**Output**:
```
Total iterations: 9
```

**Safe Move (🔄 Tweak)**: Change inner loop variable from `j` to `i`.

**Why It Works**: Shadowing the outer `i` doesn’t affect the inner loop’s independent iterations.

**Risks**: Changing `i < 3` to `i < 2` reduces the count to 4.

---

## **7. Array Avalanche** 🌊
**Description**: Find the largest element in a sorted array. Can you tweak without missing the max?

```java
import java.util.Arrays;

public class Main {
    public static void main(String[] args) {
        int[] numbers = {5, 2, 8, 1, 9};
        Arrays.sort(numbers);
        System.out.println("Largest element: " + numbers[numbers.length - 1]);
    }
}
```

**Output**:
```
Largest element: 9
```

**Safe Move (🔄 Tweak)**: Change `numbers.length - 1` to `4`.

**Why It Works**: The array has 5 elements, so index `4` accesses the last element (9) after sorting.

**Risks**: Changing the array size could cause an `ArrayIndexOutOfBoundsException`.

---

## **8. Ternary Tempest** 🌩
**Description**: Use a ternary operator for pass/fail. Can you add a block without failing?

```java
public class Main {
    public static void main(String[] args) {
        int score = 85;
        String result = (score >= 70) ? "Pass" : "Fail";
        System.out.println("Result: " + result);
    }
}
```

**Output**:
```
Result: Pass
```

**Safe Move (🔄 Tweak)**: Change `(score >= 70)` to `((score >= 70))`.

**Why It Works**: Extra parentheses don’t affect the ternary operator’s logic.

**Risks**: Changing `>=` to `<=` flips the result to `Fail`.

---

## **9. Pointer Pandemonium** 🖥
**Description**: Use pointers to print a value and address. Can you tweak without dereferencing disaster?

```c
#include <stdio.h>

int main() {
    int a = 5;
    int *ptr = &a;
    
    printf("Value of a: %d\n", a);
    printf("Value via pointer: %d\n", *ptr);
    printf("Address of a: %p\n", (void*)&a);
    
    return 0;
}
```

**Output**:
```
Value of a: 5
Value via pointer: 5
Address of a: <some address, e.g., 0x7fff5fbff83c>
```

**Safe Move (🔄 Tweak)**: Change `int a = 5` to `int a = 05`.

**Why It Works**: `05` is an octal literal but evaluates to `5` in decimal, preserving all output lines.

**Risks**: Removing `int *ptr = &a` breaks the pointer `printf`.

---

## **10. Macro Madness** 🛠
**Description**: Use a macro to square an expression. Can you tweak without squaring off?

```c
#include <stdio.h>
#define SQUARE(x) ((x) * (x))

int main() {
    int num = 5;
    int result = SQUARE(num + 1);
    printf("Square of %d + 1 is %d\n", num, result);
    return 0;
}
```

**Output**:
```
Square of 5 + 1 is 36
```

**Safe Move (🔄 Tweak)**: Change `#define SQUARE(x) ((x) * (x))` to `#define SQUARE(x) ( ( x ) * ( x ) )`.

**Why It Works**: Extra spaces and parentheses don’t affect the macro’s expansion.

**Risks**: Removing a parenthesis breaks the macro for expressions like `num + 1`.

---

## **11. Switch Showdown** 📜
**Description**: Print a grade message using a switch. Can you tweak without switching outcomes?

```c
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
```

**Output**:
```
Well done!
```

**Safe Move (🔄 Tweak)**: Change `case 'B':` to `case 66:`.

**Why It Works**: `'B'` has an ASCII value of `66`, so the case triggers the same block.

**Risks**: Removing `break` causes fall-through to the next case.

---

## **12. Loop Blitz** 🔄
**Description**: Combine conditionals and loops to print messages. Can you tweak without breaking the rhythm?

```c
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
```

**Output**:
```
i is less than 15
Hello 0
Hello 1
Hello 2
Hello 3
Hello 4
```

**Safe Move (🔄 Tweak)**: Change `i++` to `++i` in the for loop.

**Why It Works**: Pre-increment and post-increment are equivalent in the for loop’s increment step.

**Risks**: Removing `int i = 10` causes a compilation error.

---

## 🚀 Event Tips
- **Setup**: Use **Python 3.9+**, **Java 17**, and **GCC**. Test all programs beforehand.
- **Judging**: Run modified code and compare output using `diff` or manual inspection.
- **Time Limits**: 2 minutes per move for a fast-paced event.
- **Display**: Project code and output for all to see.
- **Validation**: Ensure code compiles and output matches exactly.

**Get ready to pull, tweak, and triumph!** May your code towers stand tall! 🏆
EOF

# Initialize Git repository
if [ ! -d ".git" ]; then
    echo "Initializing Git repository"
    git init
    git remote add origin "$REPO_URL"
else
    echo "Git repository already initialized"
fi

# Add and commit files
echo "Committing README.md to Git"
git add README.md
git commit -m "Add Code Jenga README with 12 challenges for club event"

# Push to GitHub
echo "Pushing to GitHub"
git push -u origin main || git push -u origin master

echo "Setup complete! README.md is committed to $REPO_URL"
echo "Check README.md in $REPO_DIR"
