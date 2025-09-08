# Code Jenga: 12 Programming Challenges 🚀

---

## 1. Fibonacci Frenzy 🧮

```python
# Question: Compute the 7th Fibonacci number iteratively.
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
