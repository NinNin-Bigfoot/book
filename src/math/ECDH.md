# Ecliptic curve

Why you need to understand this ? 
 - zk-snark is working on field of big number in Ecliptic curve (BN254)

> p = 21888242871839275222246405745257275088548364400416034343698204186575808495617

cuz for security any input or withness will not show directly!. that why we used BN254 to optimize security 

this is a number of -1 in circom 

```math 
p = 21888242871839275222246405745257275088548364400416034343698204186575808495617.

# 1 - 2 = -1
(1 - 2) % p

# 21888242871839275222246405745257275088548364400416034343698204186575808495616

```
and remember this is for security 

but why modulo p ??
- to ensures that all values within the circuit stay within a specific range, making it more efficient to reason about and prove their validity in zk-SNARKs.


OK don't worry if you don't understand now.

ECDH have multiple ratio (method to create prairng )
    - Group Operation
    - Point Dobublig
    - Adding Vertical point
    - Scalar Multiplication 👈 I'll explain this.

let say we have
-   P is a point on curve 
-   k is a integer 𝕫
-   Q(P * k time) ----> this is our final destination. <br>  
>  Q = P+P+...+P } k times

OK pls take a look in this graph <br>
![EC Graph](../asset//ec.png) <br>

then look into this <br>
![EC Point](../asset/dot.png)

so if i ask you what parameter or what is the K value untill I get the red point ?????
- answer is mind blow up!! 🤯


Here is a Bench mark about each type of Paring friendly lib. 👉 <https://hackmd.io/@gnark/eccbench#BN254>
