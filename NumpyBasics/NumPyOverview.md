

```python
import numpy as np
```


```python
l = [1,2,3]
```


```python
np.array(l)
```




    array([1, 2, 3])



Note here that `np.array` actually converts the list to an array


```python
arr = np.array(l)
```


```python
np.arange(0, 10)
```




    array([0, 1, 2, 3, 4, 5, 6, 7, 8, 9])




```python
np.arange(0,10,2)
```




    array([0, 2, 4, 6, 8])



The `np.arange()` function is actually similar to the range function in python


```python
np.zeros(5)
```




    array([0., 0., 0., 0., 0.])




```python
np.zeros((3,5))
```




    array([[0., 0., 0., 0., 0.],
           [0., 0., 0., 0., 0.],
           [0., 0., 0., 0., 0.]])



Note that it has a decimal point indicating that these are infact floating point values inside the array that we got


```python
np.ones(4)
```




    array([1., 1., 1., 1.])




```python
np.ones((3,4))
```




    array([[1., 1., 1., 1.],
           [1., 1., 1., 1.],
           [1., 1., 1., 1.]])




```python
np.linspace(0, 11, 10)
```




    array([ 0.        ,  1.22222222,  2.44444444,  3.66666667,  4.88888889,
            6.11111111,  7.33333333,  8.55555556,  9.77777778, 11.        ])




```python
np.linspace(0,11,11)
```




    array([ 0. ,  1.1,  2.2,  3.3,  4.4,  5.5,  6.6,  7.7,  8.8,  9.9, 11. ])




```python
np.linspace(0,11)
```




    array([ 0.        ,  0.2244898 ,  0.44897959,  0.67346939,  0.89795918,
            1.12244898,  1.34693878,  1.57142857,  1.79591837,  2.02040816,
            2.24489796,  2.46938776,  2.69387755,  2.91836735,  3.14285714,
            3.36734694,  3.59183673,  3.81632653,  4.04081633,  4.26530612,
            4.48979592,  4.71428571,  4.93877551,  5.16326531,  5.3877551 ,
            5.6122449 ,  5.83673469,  6.06122449,  6.28571429,  6.51020408,
            6.73469388,  6.95918367,  7.18367347,  7.40816327,  7.63265306,
            7.85714286,  8.08163265,  8.30612245,  8.53061224,  8.75510204,
            8.97959184,  9.20408163,  9.42857143,  9.65306122,  9.87755102,
           10.10204082, 10.32653061, 10.55102041, 10.7755102 , 11.        ])



The way the `np.linspace` function works is that we specify a start point, an end point and the number of points we want linearly spaced. So in the first case we had 0 to 11 and 11 points we wanted linearly spaced.


```python
np.linspace(0,11,5000)
```




    array([0.00000000e+00, 2.20044009e-03, 4.40088018e-03, ...,
           1.09955991e+01, 1.09977996e+01, 1.10000000e+01])




```python
np.random.randint(0,10)
```




    9




```python
np.random.randint(0,10,(3,3))
```




    array([[0, 1, 5],
           [2, 3, 2],
           [3, 9, 5]])




```python
np.random.seed(101)
np.random.randint(0,100,10)
```




    array([95, 11, 81, 70, 63, 87, 75,  9, 77, 40])



If i want to make sure that I am getting back the same set of random integers every time I need to make sure to fix the seed.


```python
np.random.seed(101)
arr = np.random.randint(0,100,10)
```


```python
arr
```




    array([95, 11, 81, 70, 63, 87, 75,  9, 77, 40])




```python
arr.max()
```




    95




```python
arr.min()
```




    9




```python
arr.mean()
```




    60.8




```python
arr.argmax()
```




    0



`argmax` returns the index location of the max value in the array

Similarly for `argmin`


```python
arr.reshape(2,5)
```




    array([[95, 11, 81, 70, 63],
           [87, 75,  9, 77, 40]])



Basically the `reshape` function is simply used for reshaping the array


```python
mat = np.arange(0,100).reshape(10,10)
```


```python
mat
```




    array([[ 0,  1,  2,  3,  4,  5,  6,  7,  8,  9],
           [10, 11, 12, 13, 14, 15, 16, 17, 18, 19],
           [20, 21, 22, 23, 24, 25, 26, 27, 28, 29],
           [30, 31, 32, 33, 34, 35, 36, 37, 38, 39],
           [40, 41, 42, 43, 44, 45, 46, 47, 48, 49],
           [50, 51, 52, 53, 54, 55, 56, 57, 58, 59],
           [60, 61, 62, 63, 64, 65, 66, 67, 68, 69],
           [70, 71, 72, 73, 74, 75, 76, 77, 78, 79],
           [80, 81, 82, 83, 84, 85, 86, 87, 88, 89],
           [90, 91, 92, 93, 94, 95, 96, 97, 98, 99]])




```python
mat[0,1]

```




    1




```python
mat[0,5]
```




    5




```python
mat[:,0]
```




    array([ 0, 10, 20, 30, 40, 50, 60, 70, 80, 90])




```python
mat[5,:]
```




    array([50, 51, 52, 53, 54, 55, 56, 57, 58, 59])




```python
mat[0:3,0:3]
```




    array([[ 0,  1,  2],
           [10, 11, 12],
           [20, 21, 22]])



### Masking

Boolean masking


```python
mat > 50
```




    array([[False, False, False, False, False, False, False, False, False,
            False],
           [False, False, False, False, False, False, False, False, False,
            False],
           [False, False, False, False, False, False, False, False, False,
            False],
           [False, False, False, False, False, False, False, False, False,
            False],
           [False, False, False, False, False, False, False, False, False,
            False],
           [False,  True,  True,  True,  True,  True,  True,  True,  True,
             True],
           [ True,  True,  True,  True,  True,  True,  True,  True,  True,
             True],
           [ True,  True,  True,  True,  True,  True,  True,  True,  True,
             True],
           [ True,  True,  True,  True,  True,  True,  True,  True,  True,
             True],
           [ True,  True,  True,  True,  True,  True,  True,  True,  True,
             True]])



Here we end up getting a boolean n-d array of all values that we greater than 50


```python
mat[mat>50]
```




    array([51, 52, 53, 54, 55, 56, 57, 58, 59, 60, 61, 62, 63, 64, 65, 66, 67,
           68, 69, 70, 71, 72, 73, 74, 75, 76, 77, 78, 79, 80, 81, 82, 83, 84,
           85, 86, 87, 88, 89, 90, 91, 92, 93, 94, 95, 96, 97, 98, 99])


