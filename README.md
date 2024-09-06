# Experiment-2


# Normalization: y

import numpy as np

X = np.random.rand(5,5)

mean = X.mean()

std = X.std()


normalized = (X - mean) /std


np.save('X_normalized.npy', normalized)

print("Variables: \n", X)

print("\nNormalized: \n", np.load('X_normalized.npy'))

Variables: 

 [[0.38320141 0.78434572 0.59212546 0.96534703 0.800955  ]
 [0.51033724 0.48351184 0.76107414 0.41013179 0.20691759]
 [0.76115595 0.29960103 0.81853596 0.8391078  0.5963912 ]
 [0.73388616 0.81499738 0.74551187 0.76282574 0.18518   ]
 [0.59225675 0.03675963 0.06485202 0.21719796 0.07226402]]

Normalized:

 [[-0.5555759   0.88844275  0.19649814  1.54000197  0.94823198]
 [-0.09791888 -0.19448355  0.80467091 -0.4586333  -1.19015332]
 [ 0.80496543 -0.85651623  1.01151901  1.08557246  0.21185374]
 [ 0.70680102  0.99878103  0.74865067  0.81097623 -1.26840319]
 [ 0.19697078 -1.80267921 -1.70155366 -1.15314656 -1.67487232]]


# Divisible by 3 Problem:

import numpy as np


n = np.arange(1, 101)

s = n ** 2


a = s.reshape(10, 10)


divisible_by_3 = s[s % 3 == 0]


np.save('div_by_3.npy', divisible_by_3)

print("10x10 array: \n", a) 

print("\nNumbers Divisible by 3: \n", np.load('div_by_3.npy'))

10x10 array: 

 [[    1     4     9    16    25    36    49    64    81   100]
 [  121   144   169   196   225   256   289   324   361   400]
 [  441   484   529   576   625   676   729   784   841   900]
 [  961  1024  1089  1156  1225  1296  1369  1444  1521  1600]
 [ 1681  1764  1849  1936  2025  2116  2209  2304  2401  2500]
 [ 2601  2704  2809  2916  3025  3136  3249  3364  3481  3600]
 [ 3721  3844  3969  4096  4225  4356  4489  4624  4761  4900]
 [ 5041  5184  5329  5476  5625  5776  5929  6084  6241  6400]
 [ 6561  6724  6889  7056  7225  7396  7569  7744  7921  8100]
 [ 8281  8464  8649  8836  9025  9216  9409  9604  9801 10000]]

Numbers Divisible by 3: 

 [   9   36   81  144  225  324  441  576  729  900 1089 1296 1521 1764
 2025 2304 2601 2916 3249 3600 3969 4356 4761 5184 5625 6084 6561 7056
 7569 8100 8649 9216 9801]
 
