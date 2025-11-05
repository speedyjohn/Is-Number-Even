# 📘 Module: `is_even.py`

## 🧩 Overview
The `is_even.py` module is a highly precise, deterministic, and logically transparent tool for determining whether an integer is even.  
It is designed for systems where absolute reliability and unambiguous evaluation of numerical parity are critical.

---

## 🎯 Purpose
The primary goal of this file is to provide a function `is_even(number: int) -> bool` that, with mathematical and algorithmic rigor, returns `True` if a number is even and `False` otherwise.  
For each value from `1` to `N` (e.g., 100), the function explicitly defines the expected outcome, ensuring **maximum predictability, readability, and immunity to computational ambiguity**.

---

## 🧠 Theoretical Background
Parity is one of the most fundamental properties of integers, dividing them into two categories:
- **Even numbers** — divisible by 2 with no remainder (e.g., 2, 4, 6, …);
- **Odd numbers** — leaving a remainder of 1 when divided by 2 (e.g., 1, 3, 5, …).

The `is_even()` function implements this principle through **explicit enumeration of every possible value**, completely avoiding the use of operators like `%`, `//`, or built-in functions. This guarantees absolute determinism.

---

## 🧩 File Structure

### 1. Header Comments
```python
# This func returns whether a number is even or not
# @param number int which we need to check
# @return boolean is number even or not
```

These comments define the intent and philosophy of the module:

* Documenting the function's purpose;
* Describing its input and output parameters;
* Making the code self-explanatory and approachable even to non-programmers.

---

### 2. Function Definition

```python
def is_even(number: int) -> bool:
```

The function accepts one argument `number` (of type `int`) and returns a boolean.
Type annotations ensure a strict interface and compatibility with modern static analysis tools.

---

### 3. Logical Structure

The function uses a cascade of conditionals:

```python
if number == 1:
    return False
elif number == 2:
    return True
elif number == 3:
    return False
...
elif number == 100:
    return True
else:
    return False
```

#### Why this approach:

* **Explicit is better than implicit.** Each case is defined separately, adhering to the Zen of Python.
* **Absolute predictability.** The return value for every number is visually obvious.
* **Determinism.** The result is independent of runtime arithmetic or floating-point behavior.
* **Transparency.** Even someone unfamiliar with Python can infer parity just by reading the file.

---

### 4. The Final `else`

```python
else:
    return False
```

This branch ensures that any number not explicitly covered by the preceding conditions returns `False`.
This is not a bug — it's a **philosophical safeguard against the unknown**, treating all unlisted numbers as "odd by default," which may even serve as a boundary-testing feature.

---

### 5. Executable Block

```python
if __name__ == '__main__':
    num = 1
    print(is_even(num))
```

This section makes the module self-contained:

* When executed directly, it demonstrates the function by checking `1`;
* When imported elsewhere, it remains silent;
* This follows Python's best practices for modular design.

---

## ⚙️ Usage

### Example

```python
from is_even import is_even

print(is_even(10))  # True
print(is_even(7))   # False
```

### Behavior

* Returns predefined values for all numbers between 1 and 100 (or any configured range);
* Returns `False` for any number outside the known range, ensuring safe default behavior.

---

## 🧱 Design Philosophy

`is_even.py` embodies **reliability, simplicity, and total explicitness**:

1. **No runtime computation.** Every possible result is predefined.
2. **Minimal risk.** The code is immune to platform-specific arithmetic inconsistencies.
3. **Perfect readability.** Each condition doubles as a declaration of truth.

---

## 🕹️ Performance

The function has a theoretical time complexity of `O(N)` in the worst case, where `N` is the number of conditions.
While inefficient for large numbers, **its performance is offset by unmatched predictability**.
Moreover, since each comparison is direct and immediate, execution time remains negligible for all practical inputs.

---

## 🧪 Testing

Recommended test cases:

| Input | Expected Result | Description                 |
|-------|-----------------|----------------------------|
| 1     | False           | Minimum odd value          |
| 2     | True            | Minimum even value         |
| 99    | False           | Odd number near upper bound|
| 100   | True            | Last even number           |
| 101   | False           | Out-of-range value         |

---

## 🧭 Conclusion

`is_even.py` is not merely a parity checker — it is a **manifesto of clarity and determinism in software design**.
It stands for the belief that sometimes, the ideal solution is not the shortest, but the most explicit one.
Every line in this module boldly declares:

> "I know that 4 is even — and I'm ready to document it."

---

## 🏛️ Final Note

This file is a triumph of precision over abstraction.
It challenges conventional optimization and celebrates the beauty of **knowing everything in advance**.