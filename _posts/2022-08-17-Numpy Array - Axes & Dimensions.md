---
title: "Numpy Array - Axes & Dimensions"
excerpt_separator: "<!--more-->"
categories:
  - Blog
tags:
  - Post Formats
  - readability
  - standard
---

When you first start working with Numpy arrays as I did couple of years ago with machine learning, it can be a little confusing. Machine learning libraries such as Scikit-learn requires input in a certain shape and size which can be pretty confusing and frustrating for beginners venturing into machine learning. If you just do a plain google search, Stackoverflow has over 5,000 queries regarding clarity with Numpy array dimensions. In this post, I try to cover the basic understanding of Numpy array with respect to its dimensions and shape and further understanding of multi-dimensional arrays. Let’s get started!

What is a Numpy Array?
Numpy (which stands for Numerical Python) arrays are fundamental building blocks of scientific computing in Python. They are similar to matrices, but they don’t have to be square. They can have any shape we like, and they can store values of any type, not just numbers. If you’ve used another programming language, then an array is a way to store a list of values of the same type. So, essentially, an array is a collection of data items of the same type. Numpy arrays go beyond that: they are flexible containers for data of any type and shape. Numpy is designed to take advantage of modern computer architectures, optimize memory usage, and be appropriate for a wide variety of applications. It’s optimized for efficient use with computer languages like Python, R, Julia, and more.

Working with Numpy Arrays
Numpy arrays are the fundamental data structure in the Numpy library, and they are the key to Numpy’s speed and efficiency. Numpy arrays are built on C-style arrays, which are simple lists of numbers, but they have been optimized to take advantage of modern hardware architectures. The data inside a Numpy array is organized as a series of contiguous elements, each with a specific data type and position number, with each element taking up the same amount of space. This means that when you are working with a large array, all of the elements are stored together in memory, which makes reading and writing from disk much faster.

Understanding Axis & Dimensions
You may find it a bit confusing, especially when you use axis when applying functions to multidimensional data. Whether you're manipulating data in Numpy, Pandas, TensorFlow, or another library, you'll encounter them often. The basic concepts covered here will be common to all these libraries.

What is the Axis?
Simply put, the axis is what represents the dimension of the data and for Numpy arrays it's used interchangeably, both having the same meaning. The dimension of an array is simply the no. of index position or combination of index positions you need to provide to access a single array element. Let's go through different examples to understand its core basic meaning. But before that, let's quickly have a look at how an array is indexed or stored in memory and how you can extract elements from an array.

![image-center]({{ site.url }}{{ site.baseurl }}/assets/images/Array Indexing.png){: .align-center}

The elements in an array are stored as index starting from 0 to n-1 where n is the no. of elements in an array. Numpy array is flexible in the sense that it also supports negative indexing starting from -1 (from the end of an array)to retrieve array contents from the end. To access an element of a 1-dimensional array you just need to specify a single index position like in the code below.

```
import numpy as np

Array1 = np.array([1,2,3,4,5,6,7,8])
# Element at index position 1
print("Array1 =",Array1)
print("-----------------------------")
print("Element at index position 1 is:", Array1[1]) 
# With negative indexing
print("Element at index position -7 is:", Array1[-7])  

Output:
Array1 = [1 2 3 4 5 6 7 8]
------------------------
Element at index position 1 is: 2
Element at index position -7 is: 2
```



COPY

COPY

COPY
import numpy as np

Array1 = np.array([1,2,3,4,5,6,7,8])
# Element at index position 1
print("Array1 =",Array1)
print("-----------------------------")
print("Element at index position 1 is:", Array1[1]) 
# With negative indexing
print("Element at index position -7 is:", Array1[-7])  

Output:
Array1 = [1 2 3 4 5 6 7 8]
------------------------
Element at index position 1 is: 2
Element at index position -7 is: 2
Zero-Dimensional Array
Scalar - Numpy array in zero-dimension is a scalar value. It is simply a single number. A scalar is just a number with no dimension or axis. (an analogy to scalar value in physics, which has only magnitude but no direction or dimension/axis in this case) 👀. Scalars, are the elements in an array. Each value in an array is a zero-dimension array.

```
import numpy as np
# create a 0-dimension array
a = np.array(2)
print("shape of numpy array a:", a.shape)   # returns an empty array
print("The datatype of a: ", type(a))
print("dimension of numpy array a:", a.ndim)
Output:
shape of numpy array a: ()
The datatype of a:  <class 'numpy.ndarray'>
dimension of numpy array a: 0
```

COPY

COPY

COPY

COPY
import numpy as np
# create a 0-dimension array
a = np.array(2)
print("shape of numpy array a:", a.shape)   # returns an empty array
print("The datatype of a: ", type(a))
print("dimension of numpy array a:", a.ndim)
Output:
shape of numpy array a: ()
The datatype of a:  <class 'numpy.ndarray'>
dimension of numpy array a: 0
Ok, so we just verified above, that a zero-dimension Numpy array is a scalar. You can also see that the datatype is a Numpy array. We will cover shape of an array later in the article. Once you understand the dimension concept, shape of an array would be a cakewalk. The array element here cannot be accessed via indexing. If you try to access the array element, Python will throw an index error as below 👇


COPY

COPY

COPY

COPY
# try to access the element of 0-dimensional array
a[0]
---------------------------------------------------------------------------
IndexError                                Traceback (most recent call last)
<ipython-input-29-6a1284577a36> in <module>
----> 1 a[0]

IndexError: too many indices for array: array is 0-dimensional, but 1 were indexed
1-Dimensional Array
Vector - A vector has an axis because it is one-dimensional. A vector is essentially a list of numbers representing a point in space. The list of numbers is a way of identifying that point in space. Let's create a single row and column vector and check it's dimension and shape using the ndim function and shape attribute of Numpy array.


COPY

COPY

COPY

COPY
# importing numpy
import numpy as np

# creating a 1-D list (Row Vector)
list1 = [10, 20, 30]

# creating a 1-D list (Column Vector)
list2 = [[10],
        [20],
        [30]]

# creating a vector1
# vector as row
vector1 = np.array(list1)

# creating a vector 2
# vector as column
vector2 = np.array(list2)

# Print row vector
print("Row Vector")
print(vector1)

print("----------------")

# Print column vector
print("Column Vector")
print(vector2)

Output:
Row Vector
[10 20 30]
----------------
Column Vector
[[10]
 [20]
 [30]]
Now, let's check arrays (vector1 and vector2) dimension and shape and notice this is where it gets interesting as well as a bit confusing 🤷‍♂️😎


COPY

COPY

COPY

COPY
print("Vector1 has dimension of:", vector1.ndim)
print("Vector1 has shape of:", vector1.shape)

print("--------------------------")

print("Vector2 has dimension of:", vector2.ndim)
print("Vector2 has shape of:", vector2.shape)

Output:
Vector1 has dimension of: 1
Vector1 has shape of: (3,)
--------------------------
Vector2 has dimension of: 2
Vector2 has shape of: (3, 1)
The row vector1 has a dimension of 1 and shape of 3 whereas column vector2 has dimension of 2 and shape of (3,1). (Note* Linear algebra makes a distinction between "row vectors" and "column vectors". There is no such distinction in NumPy)

2-Dimensional Array
Here, vector2 is a 2-dimensional array. We can also say it's a matrix with a collection of vectors and has a shape of (n,m), where 'n' is the number of vectors in it and 'm' is the number of elements in each vector. Here, it has 3 vectors with one element each and hence, its shape is (3,1). You can also visualize dimensions as axis=0 for rows and axis=1 for columns as we will see below.

For a 2-dimensional array we need to provide 2 index positions to extract the single element.


COPY

COPY

COPY

COPY
# Extracts the single element list
print(vector2[0])
# Extracts the single element with two index positions specified
print(vector2[0,0])

Output:
[10] 
10
image.png

The catch here is to understand the shape of an array. The shape of an array is the number of elements in each dimension. Hence, for a zero-dimensional array you will get an empty array as we saw earlier.

In the example above, vector2 being a nested list, you can see it as 3 vectors/rows along axis=0 and 1 element/column in second dimension or axis=1. Hence the shape (3,1).

3-Dimensional Array
Let's create a 3-dimensional array and have a look at its dimension and shape. You can also specify the dimension of the array using ndmin parameter while creating an array.


COPY

COPY

COPY

COPY
array3d = np.array([[[1, 2, 3], [4,5,6]], [[7,8,9], [10,11,12]]], ndmin=3)

print(array3d)
print("-------------------")
print('shape of array :', array3d.shape)

Output:
[[[ 1  2  3]
  [ 4  5  6]]

 [[ 7  8  9]
  [10 11 12]]]
-------------------
shape of array : (2, 2, 3)
Below is the visual representation of a 3-D array we created above.image.png

3-dimensional arrays are basically a collection of matrices in the shape of (m,n,p) where 'm' is the no. of matrices, 'n' is the no. of vectors in each matrix and 'p' is the no. of elements in each vector. Hence, the shape for above array is (2,2,3). You can also view the shape of 3-dimensional array as each matrix representing a plane and each plane with its vector and corresponding elements in those vectors.

Once you have this basic understanding of Numpy array dimensions and shape, it becomes a lot easier to visualize and understand the code when you are working with high dimensional data (i.e. arrays greater than 3-D) which is very common in machine learning practice. 👍

I started this article to cover array data manipulation tasks such as broadcasting, array slicing, reshaping and applying various functions on array, but realized the basic introduction is very important to understand further advanced operations with Numpy arrays and at the end the post got a bit lengthy 🤦‍♂️. I shall cover the array data manipulation in the upcoming post. Hope, you got a few takeaways from this post. 👍😊 Till next time stay safe, keep practicing and happy learning! 😊
