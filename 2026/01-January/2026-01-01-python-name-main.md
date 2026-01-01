# 2026-01-01 TIL: Python's `if __name__ == '__main__'` Explained

## Category: Python / Fundamentals

### Video Reference

[![YouTube](https://img.shields.io/badge/YouTube-Video-red?style=flat-square&logo=youtube)](https://www.youtube.com/watch?v=KZpYtNtGxSU)

### Key Takeaways

The `if __name__ == '__main__':` idiom is one of Python's most important patterns for writing reusable, testable code.

#### 🤔 What is `__name__`?

`__name__` is a special built-in variable that Python sets automatically:

| Scenario                  | Value of `__name__`                   |
| ------------------------- | ------------------------------------- |
| Script run directly       | `'__main__'`                          |
| Script imported as module | The module's filename (without `.py`) |

#### 🔍 When does `__name__ == '__main__'`?

```python
# file: greetings.py

def say_hello(name):
    return f"Hello, {name}!"

print(f"__name__ is: {__name__}")

if __name__ == '__main__':
    # This block ONLY runs when the file is executed directly
    print(say_hello("World"))
```

**Running directly:**

```bash
$ python greetings.py
__name__ is: __main__
Hello, World!
```

**Importing as module:**

```python
# file: main.py
import greetings  # Output: __name__ is: greetings
# The if block does NOT execute!
```

#### 🧪 Primary Use Case: Testing Code

This pattern is perfect for including test code that won't run when the module is imported:

```python
# file: calculator.py

def add(a, b):
    return a + b

def multiply(a, b):
    return a * b

if __name__ == '__main__':
    # Quick tests - only run when executed directly
    print("Running tests...")
    assert add(2, 3) == 5, "Addition failed"
    assert multiply(4, 5) == 20, "Multiplication failed"
    print("All tests passed! ✅")
```

#### 📊 Visual Flow

```
┌─────────────────────────────────────────────────────────┐
│                  Python Execution Flow                   │
├─────────────────────────────────────────────────────────┤
│                                                          │
│   python script.py          import script               │
│         │                        │                       │
│         ▼                        ▼                       │
│   __name__ = '__main__'    __name__ = 'script'          │
│         │                        │                       │
│         ▼                        ▼                       │
│   if __name__ == '__main__':                            │
│         │                        │                       │
│      TRUE ✅                  FALSE ❌                   │
│         │                        │                       │
│   Code block runs         Code block skipped            │
│                                                          │
└─────────────────────────────────────────────────────────┘
```

### Code / Implementation

A practical example — a utility module with built-in demos:

```python
# file: string_utils.py
"""String utility functions with built-in demonstration."""

def reverse_string(s: str) -> str:
    """Reverse a string."""
    return s[::-1]

def is_palindrome(s: str) -> bool:
    """Check if a string is a palindrome (case-insensitive)."""
    cleaned = s.lower().replace(" ", "")
    return cleaned == cleaned[::-1]

def count_vowels(s: str) -> int:
    """Count vowels in a string."""
    return sum(1 for char in s.lower() if char in 'aeiou')


if __name__ == '__main__':
    # Demo mode - runs only when executed directly
    print("=== String Utils Demo ===\n")

    test_string = "Hello World"
    print(f"Original: {test_string}")
    print(f"Reversed: {reverse_string(test_string)}")
    print(f"Vowel count: {count_vowels(test_string)}")

    palindrome_test = "A man a plan a canal Panama"
    print(f"\n'{palindrome_test}'")
    print(f"Is palindrome: {is_palindrome(palindrome_test)}")
```

### Additional Resources

- [Python Docs: `__main__`](https://docs.python.org/3/library/__main__.html)
- [Real Python: if **name** == "**main**"](https://realpython.com/if-name-main-python/)
- [Original Video](https://www.youtube.com/watch?v=KZpYtNtGxSU)
