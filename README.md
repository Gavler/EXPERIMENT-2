# Experiment-2


# Normalization:
Normalization is one of the most basic preprocessing techniques in
data analytics. This involves centering and scaling process. Centering means subtracting the data from the
mean and scaling means dividing with its standard deviation. Mathematically, normalization can be
expressed as:

 ![image](https://github.com/user-attachments/assets/691efe30-e11b-42f3-87e1-84a0a4a705b7)

In Python, element-wise mean and element-wise standard deviation can be obtained by using .mean() and
.std() calls.

In this problem, create a random 5 x 5 ndarray and store it to variable X. Normalize X. Save your normalized
ndarray as X_normalized.npy.
- Since this is an array, we use numpy and call it out.
 
		import numpy as np
- np.rando.rand used to create a random 5 by 5 float variable between 0 and 1.

		X = np.random.rand(5,5)
- To get the standard deviation of the problem, we call the mean and std of x, and then we set up the equation.

		mean = X.mean()
		std = X.std()

		normalized = (X - mean) /std
- The computed x is then saved as an X_normalized.npy file and can be called at any time.

		np.save('X_normalized.npy', normalized)
- Then, we print out the code to get the output.

		print("Variables: \n", X)
		print("\nNormalized: \n", np.load('X_normalized.npy'))


# OUTPUT

 Variables: 

> [[0.38320141 0.78434572 0.59212546 0.96534703 0.800955  ]
 [0.51033724 0.48351184 0.76107414 0.41013179 0.20691759]
 [0.76115595 0.29960103 0.81853596 0.8391078  0.5963912 ]
 [0.73388616 0.81499738 0.74551187 0.76282574 0.18518   ]
 [0.59225675 0.03675963 0.06485202 0.21719796 0.07226402]]

Normalized:

> [[-0.5555759   0.88844275  0.19649814  1.54000197  0.94823198]
 [-0.09791888 -0.19448355  0.80467091 -0.4586333  -1.19015332]
 [ 0.80496543 -0.85651623  1.01151901  1.08557246  0.21185374]
 [ 0.70680102  0.99878103  0.74865067  0.81097623 -1.26840319]
 [ 0.19697078 -1.80267921 -1.70155366 -1.15314656 -1.67487232]]



# Divisible by 3 Problem:
Create the following 10 x 10 ndarray:

![image](https://github.com/user-attachments/assets/e9cc4534-f2c9-4459-8750-4d711ee51c90)


Which are the squares of the first 100 positive integers.
From this ndarray, determine all the elements that are divisible by 3. Save the result as div_by_3.npy.
- Same as the previous problem it also an array so we call numpy as np

		import numpy as np
- We need the first 100 square integers, so we use this equation.

		n = np.arange(1, 101)** 2

- Then, we arrange values in a 10x10 array. 

		a = n.reshape(10, 10)
  
- We need the values that are divisible by 3 in the array so we use this equation.
 
		divisible_by_3 = n[n % 3 == 0]

- We arrange the values to make it clean and use -1 to automatically compute how many items in three rows are needed.
		
		b = divisible_by_3.reshape(3,-1)

- Save the result as div_by_3.npy file.

		np.save('div_by_3.npy', b)
- We print out the code to get the output.
	
		print("10x10 array: \n", a)
  		print("\nNumbers Divisible by 3: \n", np.load('div_by_3.npy'))

# OUTPUT

 10x10 array of Square integers: 

> [[    1     4     9    16    25    36    49    64    81   100]
>
> [  121   144   169   196   225   256   289   324   361   400]
>
> [  441   484   529   576   625   676   729   784   841   900]
>
> [  961  1024  1089  1156  1225  1296  1369  1444  1521  1600]
>
>  [ 1681  1764  1849  1936  2025  2116  2209  2304  2401  2500]
>
> [ 2601  2704  2809  2916  3025  3136  3249  3364  3481  3600]
>
> [ 3721  3844  3969  4096  4225  4356  4489  4624  4761  4900]
>
> [ 5041  5184  5329  5476  5625  5776  5929  6084  6241  6400]
>
> [ 6561  6724  6889  7056  7225  7396  7569  7744  7921  8100]
>
> [ 8281  8464  8649  8836  9025  9216  9409  9604  9801 10000]]
 

 Numbers Divisible by 3: 

>  [[   9   36   81  144  225  324  441  576  729  900 1089]
>
> [1296 1521 1764 2025 2304 2601 2916 3249 3600 3969 4356]
>
> [4761 5184 5625 6084 6561 7056 7569 8100 8649 9216 9801]]


# Change log
- 0.1 added the .ipynb file.

- 0.2 added a README file.

- 0.3 edited the README file.

- 0.4 revised the .ipynb file; added the files included within the code.

 
