# Rank 1 Constrain Systems 

Now you circuit after compile and get ```file.r1cs``` file that mean 
the part that matrix come to play.

> this is definition of R1CS ***Az * Bz - Cz = 0*** or ***Az * Bz = Cz***

while A, B, C is a matrix of circuit 

and w is how to comput withness interm 
- > (1 || x || w)

and then do a element wise product (multiplier w to A, B, C index by index)

![Matrix definitiion](../asset/r1cs-matrix.png)

here's some code exmaple of this Aritmatic circuit to R1CS

```out = x * y + 2```

optimize for prevent r1cs larger than it needs to be.

```out - 2 = x * y```

```python
import numpy as np
import random

# Define the matrices
A = np.array([[0,0,1,0]])
B = np.array([[0,0,0,1]])
C = np.array([[-2,1,0,0]])

# pick random values to test the equation
x = random.randint(1,1000)
y = random.randint(1,1000)
out = x * y + 2# witness vector
w = np.array([1, out, x, y])

# check the equality
result = C.dot(w) == np.multiply(A.dot(w),B.dot(w))
assert result.all(), "result contains an inequality"
```

matrix size is depent on ***w***

but this is not done yet cuz it's lack of security go to next part to see how it more secure.