# ECE2112---Programming_Assignment---2
Manalang, 2-ECE-C

## Overview
This experiment is about *Numerical Python (NumPy)*. The assignment demonstrates the use of Numpy to perform basic data manipulation and array operations. 

There are **2 problems** in this experiment:
1. **Normalization Problem** - Create a random 5x5 NumPy array and normalize it.
2. **Divisible by 3 Problem** - Create a 10x10 array of squares of the first 100 positive integers, extract numbers divisible by 3, and save them.

---

## Files
- `Assignment_2_Manalang_2-ECE_C.ipynb` - Jupyter Notebook containing the solution code.
- `X_normalized.npy` - Saved NumPy file containing the normalized 5x5 array.
- `div_by_3.npy` - Saved NumPy file containing all elements divisible by 3 from the 10x10 matrix.

---

## Code Explanation

### 1. Normalization Problem
- A random 5x5 array `X` is generated using `np.random.rand(5,5)`.
- Normalization is applied using the formula:

  ```
  Z = (X - mean) / std
  ```

  where `mean` is the average of all elements in array X and `std` is the standard deviation.
- The result is stored as `X_normalized.npy`.

### 2. Divisible by 3 Problem
- A 10x10 matrix `A` is created using:

  ```python
  A = np.arange(1, 101).reshape(10, 10) ** 2
  ```
  This generates integers from 1 to 100, reshapes them into a 10x10 matrix, and squares each element.
- To find elements divisible by 3:
  ```python
  x = A[A % 3 == 0]
  ```
  This checks every element of `A` and filters only those divisible by 3.
- The result is saved as `div_by_3.npy`.

---


## Notes
- `np.save()` is used to save arrays as `.npy` files.
- `np.load()` can be used to reload and verify saved files, e.g.:
  ```python
  arr = np.load("div_by_3.npy")
  print(arr)
  ```

---

## Conclusion and Reflection

Doing this experiment widened my knowledge in Python, especially in using Numpy for mathematical operations and array manipulation. I did not know that arrays can be used like this since I only knew a little bit of array in C++. I thought about whether similar codes for generating random numbers or arrays could be used as part of random number generators (RNG) in games like gacha games.

The experiment also helped me practice the use of functions more, which makes code more reusable and clean. I also learned how to save and load files with Numpy which gave me an idea that maybe i could load a pdf file into python and make a summary about it, like how we use AI

In addition, this activity trained me to pay closer attention to how arrays are structured and reshaped, and how conditions like boolean indexing can filter values in just a single line of code. It showed me that Python has shortcuts that are both powerful and easy to understand once practiced.

Overall, this experiment not only gave me technical skills but also inspired me to think creatively about coding. It opened my curiosity to explore how Python and Numpy can be applied in areas such as gaming, artificial intelligence, and data science.
