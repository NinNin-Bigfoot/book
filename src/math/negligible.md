# Negligible function
Known as a cryptographic method to improve the security of our proofs.

Definition (Please visit this video first) 👉 <https://www.youtube.com/watch?v=l5A3oEG-XKk&list=PLAj2bGZ0eFtICkway8SJBrJBQ76VinWzB&index=2>

Imagine an attacker attempting to perform a brute-force attack with unbounded computational resources to find our proof in the field 𝔽.

So, what happened?

Brute force will not work effectively because finding the correct 'N' would take an extremely long time. This means that the attacker is effectively limited to polynomial time, whereas the proof verification can be accomplished in logarithmic time.

Then, the attacker would resort to a guessing method, often referred to as a poly-bounded adversary, to attempt to select the correct value.

This is where ***negligible functions come*** into play.

A polynomial-time algorithm has 'n' as a secret parameter. This means that if an attacker needs to find the correct value, they would be limited to polynomial time complexity. However, they might employ a method to randomly select potential values for 'n', which could potentially increase the time required for a successful attack.

what negligible function do ? 
 - significantly reduce the probability of finding the correct value within polynomial time.

 - Negligible functions define an upper bound on the probability of an event occurring within a reasonable timeframe, especially in the context of cryptography. For example, in the scenario where an attacker attempts to guess a secret parameter within polynomial time, a negligible function would define an upper bound on the probability of the attacker successfully finding the correct value.
 cuz it think about 1 / p(λ)

This is why the proof size depends on λ (the secret lambda parameter).

![Proof size](../asset/proof-size-time.png)