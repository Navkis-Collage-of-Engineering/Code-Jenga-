# 🎮 CODE JENGA: EXECUTABLE CHALLENGES 🎮
# Copy each challenge separately to test/play

# ================================================================================
# CHALLENGE 1: Fibonacci Frenzy 🧮
# ================================================================================
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

# ================================================================================
# CHALLENGE 2: Even Squares Explosion 💣
# ================================================================================
numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
squared_evens = [x**2 for x in numbers if x % 2 == 0]
summed = sum(squared_evens)
print(f"Sum of squares of even numbers: {summed}")

# ================================================================================
# CHALLENGE 3: FizzBuzz Firestorm 🔥
# ================================================================================
for i in range(1, 16):
    output = ""
    if i % 3 == 0:
        output += "Fizz"
    if i % 5 == 0:
        output += "Buzz"
    print(output if output else i)

# ================================================================================
# CHALLENGE 4: Dictionary Dash 📊
# ================================================================================
data = {"a": 10, "b": 20, "c": 30}
total = 0
for key, value in data.items():
    total += value
average = total / len(data)
print(f"The average value is {average}")

# ================================================================================
# CHALLENGE 5: Inheritance Inferno 🐶
# ================================================================================
class Animal:
    def makeSound(self):
        print("Some generic animal sound")

class Dog(Animal):
    def makeSound(self):
        print("Woof!")

myDog = Dog()
myDog.makeSound()

# ================================================================================
# CHALLENGE 6: Loop Lightning ⚡
# ================================================================================
count = 0
for i in range(3):
    for j in range(3):
        count += 1
print(f"Total iterations: {count}")

# ================================================================================
# CHALLENGE 7: Array Avalanche 🌊
# ================================================================================
numbers = [5, 2, 8, 1, 9]
numbers.sort()
print(f"Largest element: {numbers[-1]}")

# ================================================================================
# CHALLENGE 8: Ternary Tempest 🌩
# ================================================================================
score = 85
result = "Pass" if score >= 70 else "Fail"
print(f"Result: {result}")

# ================================================================================
# CHALLENGE 9: Pointer Pandemonium 🖥 (Python Simulation)
# ================================================================================
a = 5
ptr = id(a)
print(f"Value of a: {a}")
print(f"Address of a (simulated): {ptr}")

# ================================================================================
# CHALLENGE 10: Macro Madness 🛠 (Python Simulation)
# ================================================================================
def SQUARE(x):
    return x * x

num = 5
result = SQUARE(num + 1)
print(f"Square of {num} + 1 is {result}")

# ================================================================================
# CHALLENGE 11: Switch Showdown 📜 (Python Simulation)
# ================================================================================
grade = 'B'
switch = {
    'A': "Excellent!",
    'B': "Well done!",
    'C': "Good!"
}
print(switch.get(grade, "Invalid grade"))

# ================================================================================
# CHALLENGE 12: Loop Blitz 🔄
# ================================================================================
i = 10
if i < 15:
    print("i is less than 15")
else:
    print("i is greater than 15")

for i in range(5):
    print(f"Hello {i}")

# ================================================================================
# INSTRUCTIONS FOR ORGANIZERS:
# 1. Copy each challenge separately for teams to work on
# 2. Each challenge should run independently
# 3. Teams can test their moves by running the code
# 4. Make sure output matches exactly!
# ================================================================================
