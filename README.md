# ==============================
# 1. Fibonacci Frenzy 🧮
# Question: Compute the 7th Fibonacci number iteratively
# ==============================
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
# Expected Output: The 7th Fibonacci number is 13


# ==============================
# 2. Even Squares Explosion 💣
# Question: Sum the squares of even numbers
# ==============================
numbers = [1,2,3,4,5,6,7,8,9,10]
squared_evens = [x**2 for x in numbers if x % 2 == 0]
summed = sum(squared_evens)
print(f"Sum of squares of even numbers: {summed}")
# Expected Output: Sum of squares of even numbers: 220


# ==============================
# 3. FizzBuzz Firestorm 🔥
# Question: Print numbers 1 to 15 with "Fizz" for multiples of 3, "Buzz" for multiples of 5, and "FizzBuzz" for multiples of both
# ==============================
for i in range(1, 16):
    output = ""
    if i % 3 == 0:
        output += "Fizz"
    if i % 5 == 0:
        output += "Buzz"
    print(output if output else i)
# Expected Output:
# 1
# 2
# Fizz
# 4
# Buzz
# Fizz
# 7
# 8
# Fizz
# Buzz
# 11
# Fizz
# 13
# 14
# FizzBuzz


# ==============================
# 4. Dictionary Dash 📊
# Question: Compute the average of dictionary values
# ==============================
data = {"a": 10, "b": 20, "c": 30}
total = 0
for key, value in data.items():
    total += value
average = total / len(data)
print(f"The average value is {average}")
# Expected Output: The average value is 20.0


# ==============================
# 5. Inheritance Inferno 🐶
# Question: Use inheritance to make a dog bark
# ==============================
class Animal:
    def makeSound(self):
        print("Some generic animal sound")

class Dog(Animal):
    def makeSound(self):
        print("Woof!")

myDog = Dog()
myDog.makeSound()
# Expected Output: Woof!


# ==============================
# 6. Loop Lightning ⚡
# Question: Count iterations in nested loops
# ==============================
count = 0
for i in range(3):
    for j in range(3):
        count += 1
print(f"Total iterations: {count}")
# Expected Output: Total iterations: 9


# ==============================
# 7. Array Avalanche 🌊
# Question: Find the largest element in a sorted array
# ==============================
numbers = [5, 2, 8, 1, 9]
numbers.sort()
print(f"Largest element: {numbers[-1]}")
# Expected Output: Largest element: 9


# ==============================
# 8. Ternary Tempest 🌩
# Question: Use a ternary operator for pass/fail
# ==============================
score = 85
result = "Pass" if score >= 70 else "Fail"
print(f"Result: {result}")
# Expected Output: Result: Pass


# ==============================
# 9. Pointer Pandemonium 🖥
# Question: Use pointers to print a value and address (simulated in Python)
# ==============================
a = 5
ptr = id(a)
print(f"Value of a: {a}")
print(f"Address of a (simulated): {ptr}")
# Expected Output:
# Value of a: 5
# Address of a: <some address, varies each run>


# ==============================
# 10. Macro Madness 🛠
# Question: Use a macro to square an expression (simulated in Python)
# ==============================
def SQUARE(x):
    return x * x

num = 5
result = SQUARE(num + 1)
print(f"Square of {num} + 1 is {result}")
# Expected Output: Square of 5 + 1 is 36


# ==============================
# 11. Switch Showdown 📜
# Question: Print a grade message using a switch (simulated in Python)
# ==============================
grade = 'B'
switch = {
    'A': "Excellent!",
    'B': "Well done!",
    'C': "Good!"
}
print(switch.get(grade, "Invalid grade"))
# Expected Output: Well done!


# ==============================
# 12. Loop Blitz 🔄
# Question: Combine conditionals and loops to print messages
# ==============================
i = 10
if i < 15:
    print("i is less than 15")
else:
    print("i is greater than 15")

for i in range(5):
    print(f"Hello {i}")
# Expected Output:
# i is less than 15
# Hello 0
# Hello 1
# Hello 2
# Hello 3
# Hello 4
