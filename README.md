🎮 CODE JENGA: EXECUTABLE CHALLENGES 🎮
🔥 CHALLENGE 1: Fibonacci Frenzy 🧮
python
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
Output:

text
The 7th Fibonacci number is 13
🔥 CHALLENGE 2: Even Squares Explosion 💣
python
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
squared_evens = [x**2 for x in numbers if x % 2 == 0]
summed = sum(squared_evens)
print(f"Sum of squares of even numbers: {summed}")
Output:

text
Sum of squares of even numbers: 220
🔥 CHALLENGE 3: FizzBuzz Firestorm 🔥
python
for i in range(1, 16):
    output = ""
    if i % 3 == 0:
        output += "Fizz"
    if i % 5 == 0:
        output += "Buzz"
    print(output if output else i)
Output:

text
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
🔥 CHALLENGE 4: Dictionary Dash 📊
python
data = {"a": 10, "b": 20, "c": 30}
total = 0
for key, value in data.items():
    total += value
average = total / len(data)
print(f"The average value is {average}")
Output:

text
The average value is 20.0
🔥 CHALLENGE 5: Inheritance Inferno 🐶
python
class Animal:
    def makeSound(self):
        print("Some generic animal sound")

class Dog(Animal):
    def makeSound(self):
        print("Woof!")

myDog = Dog()
myDog.makeSound()
Output:

text
Woof!
🔥 CHALLENGE 6: Loop Lightning ⚡
python
count = 0
for i in range(3):
    for j in range(3):
        count += 1
print(f"Total iterations: {count}")
Output:

text
Total iterations: 9
🔥 CHALLENGE 7: Array Avalanche 🌊
python
numbers = [5, 2, 8, 1, 9]
numbers.sort()
print(f"Largest element: {numbers[-1]}")
Output:

text
Largest element: 9
🔥 CHALLENGE 8: Ternary Tempest 🌩
python
score = 85
result = "Pass" if score >= 70 else "Fail"
print(f"Result: {result}")
Output:

text
Result: Pass
🔥 CHALLENGE 9: Pointer Pandemonium 🖥 (Python Simulation)
python
a = 5
ptr = id(a)
print(f"Value of a: {a}")
print(f"Address of a (simulated): {ptr}")
Output:

text
Value of a: 5
Address of a (simulated): [Memory address will vary each run]
🔥 CHALLENGE 10: Macro Madness 🛠 (Python Simulation)
python
def SQUARE(x):
    return x * x

num = 5
result = SQUARE(num + 1)
print(f"Square of {num} + 1 is {result}")
Output:

text
Square of 5 + 1 is 36
🔥 CHALLENGE 11: Switch Showdown 📜 (Python Simulation)
python
grade = 'B'
switch = {
    'A': "Excellent!",
    'B': "Well done!",
    'C': "Good!"
}
print(switch.get(grade, "Invalid grade"))
Output:

text
Well done!
🔥 CHALLENGE 12: Loop Blitz 🔄
python
i = 10
if i < 15:
    print("i is less than 15")
else:
    print("i is greater than 15")

for i in range(5):
    print(f"Hello {i}")
Output:

text
i is less than 15
Hello 0
Hello 1
Hello 2
Hello 3
Hello 4
