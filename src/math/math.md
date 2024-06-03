# Basic Math for Zero-Knowledge

There is a lot of mathimatic using in Zero-knowlage technology like math in crypographic.

but in this section we gonna learn math for understand how to write circuit and how the circuit work with math.

There are 2 section of math that you should know before jump in code section

## Non-linear Equation

- why we need to know this ?
    - when we write circuit it's must be in term of Quadartic Equation (Non-linear) and this is the rules or constrain.
- why it's must be Quadartic Equation
    - imagine about if minimum of each computation is x ** 4
    computation time will blow up, complexity and take more time, this is why circom allow just x ** 2 is maximum cuz it all about efficiency proof.
#### linear vs non-linear
![Graph](../asset/linear.png)
## Matrix

#### Rank of matrix

- why we need to know this ?
    - after wire aritmetic circuit it's will be compress and comoutation in term of ***R1CS (Rank-1 constrain system)***, and it all about matrix 

- why rank-1 ? 
    - Rank of matrix is use for evelutate about how many equation that we gonna find
    - So Rank-1 constrain is the rules they will compute and process just 1 rank per matrix for efficiency time computaion, imagine have 10 rank in matrix, it gonnabe blow up
![Rank](../asset/rank.png)

#### solving equation problem with matrix
Trikc we can determine rank of matrix and then find solving equation by using gauss elimination method.
