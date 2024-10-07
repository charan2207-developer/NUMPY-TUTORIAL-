# NUMPY-TUTORIAL-
this is Numpy tutorial for the begginers which is done by me 
Here's a detailed overview of the NumPy code snippets you provided, formatted for your GitHub README. You can modify it as needed.

---

% NumPy Code Snippets

This document contains various code snippets demonstrating the usage of the NumPy library in Python for numerical computing. Each section highlights a specific functionality or feature of NumPy.

%% 1. Array Creation

%%% 1.1 Creating a Simple Array
```python
import numpy as np
a = np.array([1, 2, 3])
r = np.asarray(a, dtype="str")
print(r)
```
%Output:%
```
['1' '2' '3']
```
- Converts an array of integers to strings.

%%% 1.2 From Buffer
```python
s = b"helloooooooooooooooooooo"
z = np.frombuffer(s, dtype="int")
print(z)
```
%Output:%
```
[8029759184975979880 8029759185026510703 8029759185026510703]
```
- Creates a NumPy array from a buffer of bytes.

%%% 1.3 From Iterable
```python
s = [1, 2, 3, 4, 5]
z = np.fromiter(s, dtype=int)
print(z)
```
%Output:%
```
[1 2 3 4 5]
```
- Generates an array from an iterable.

%% 2. Array Generation

%%% 2.1 Using `arange`
```python
a = np.arange(0, 10, 2)
print(a)
```
%Output:%
```
[0 2 4 6 8]
```
- Creates an array with a specified range and step.

%%% 2.2 Using `linspace`
```python
a = np.linspace(0, 10, 3, endpoint=False, retstep=True, dtype=int)
print(a)
```
%Output:%
```
(array([0, 3, 6]), 3.3333333333333335)
```
- Generates linearly spaced values between two numbers.

%%% 2.3 Using `logspace`
```python
a = np.logspace(10, 10000, num=4, base=10)
print(a)
```
%Output:%
```
[1.e+10    inf    inf    inf]
```
- Creates an array with numbers spaced evenly on a logarithmic scale.

%% 3. Array Initialization

%%% 3.1 Creating Zeros Array
```python
x = np.zeros((2, 3), dtype=int)
print(x)
```
%Output:%
```
[[0 0 0]
 [0 0 0]]
```
- Initializes a 2D array filled with zeros.

%%% 3.2 Creating Full Array
```python
x = np.full((2, 3), 5, dtype=float)
print(x)
```
%Output:%
```
[[5. 5. 5.]
 [5. 5. 5.]]
```
- Creates a 2D array filled with a specified constant value.

%%% 3.3 Identity Matrix
```python
x = np.eye(3, dtype=int)
print(x)
```
%Output:%
```
[[1 0 0]
 [0 1 0]
 [0 0 1]]
```
- Generates a 2D identity matrix.

%% 4. Array Properties

%%% 4.1 Shape of an Array
```python
x = np.array([[1, 2, 3], [4, 5, 6]])
print(np.shape(x))
```
%Output:%
```
(2, 3)
```
- Retrieves the shape of an array.

%%% 4.2 Reshaping an Array
```python
x = np.array([[1, 2, 3], [4, 5, 6]])
print(np.reshape(x, (3, 2)))
```
%Output:%
```
[[1 2]
 [3 4]
 [5 6]]
```
- Changes the shape of an array without changing its data.

%% 5. Indexing and Slicing

%%% 5.1 Accessing Elements
```python
x = np.array([[1, 2, 3], [4, 5, 6]])
print(x[0, 2])
```
%Output:%
```
3
```
- Accesses a specific element in a multi-dimensional array.

%%% 5.2 Slicing Arrays
```python
x = np.array([[1, 2, 3], [4, 5, 6]])
print(x[0:2, 1])
```
%Output:%
```
[2 5]
```
- Slices parts of the array based on specified indices.

%%% 5.3 Advanced Slicing
```python
x = np.array([1, 2, 3, 4, 5, 6])
print(x[::2])
```
%Output:%
```
[1 3 5]
```
- Uses slicing to select every second element.

%% 6. Array Copying and Views

%%% 6.1 Copying Arrays
```python
x = np.array([1, 2, 3, 4, 5])
y = x.copy()
y[0] = 4
print(x)
print(y)
```
%Output:%
```
[1 2 3 4 5]
[4 2 3 4 5]
```
- Demonstrates creating a copy of an array that does not affect the original.

%%% 6.2 Array Views
```python
x = np.array([1, 2, 3, 4, 5])
y = x.view()
y[0] = 4
print(x)
print(y)
```
%Output:%
```
[4 2 3 4 5]
[4 2 3 4 5]
```
- Shows that views reference the same data as the original array.

%% 7. Array Concatenation and Stacking

%%% 7.1 Concatenation
```python
x = np.arange(0, 4).reshape(2, 2)
y = np.arange(0, 4).reshape(2, 2)
z = np.concatenate((x, y), axis=1)
print(z)
```
%Output:%
```
[[0 1 0 1]
 [2 3 2 3]]
```
- Combines arrays along a specified axis.

%%% 7.2 Stacking
```python
z = np.stack((x, y), axis=1)
print(z)
```
%Output:%
```
[[[0 1]
  [0 1]]

 [[2 3]
  [2 3]]]
```
- Stacks arrays along a new axis.

%% 8. Array Splitting

%%% 8.1 Splitting Arrays
```python
a = np.arange(10)
print(a, "\n")
b = np.array_split(a, 3)
print(b, "\n")
```
%Output:%
```
[0 1 2 3 4 5 6 7 8 9] 

[array([0, 1, 2, 3]), array([4, 5, 6]), array([7, 8, 9])] 
```
- Splits an array into multiple sub-arrays.

%% 9. Searching in Arrays

%%% 9.1 Finding Indices
```python
a = np.arange(10)
print(a)
x = np.where(a == 5)
print(x)
```
%Output:%
```
[0 1 2 3 4 5 6 7 8 9]
(array([5]),)
```
- Locates the index of a specific value in an array.

%% 10. Array Operations

%%% 10.1 Basic Operations
```python
import numpy as np
a = np.arange(1, 7).reshape(2, 3)
b = np.arange(7, 13).reshape(2, 3)
print(a, "\n")
print(b, "\n")
z = np.add(a, b)
print(z, "\n")
z = np.subtract(b, a)
print(z, "\n")
```
%Output:%
```
[[1 2 3]
 [4 5 6]] 

[[ 7  8  9]
 [10 11 12]] 

[[ 8 10 12]
 [14 16 18]] 

[[6 6 6]
 [6 6 6]] 
```
- Demonstrates element-wise arithmetic operations between arrays.

---

Feel free to add any additional sections or modify the explanations as needed!
