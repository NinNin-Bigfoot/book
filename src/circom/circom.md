# Circom

a HDL languages to write circuit

## how to wire circom is 
1. create variable for very intermedate wire 
2. wrire quation 

for example 

```circom 
pragma circom 2.0.0;

/*This circuit template checks that c is the multiplication of a and b.*/  

template Multiplier2 () {  

   // Declaration of signals.  
   signal input a;  
   signal input b;  
   signal output c;  

   // Constraints.  
   c <== a * b;  
}

```

![Circom](../asset/circom.png)
