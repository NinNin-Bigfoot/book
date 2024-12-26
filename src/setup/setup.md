# Setup Process

Why do we need to set up?
    - Because we need to ensure that the proof is generated correctly by the prover.


## This is type of setup 

![Setup](../asset/setup.png)


However, in this section, we will use Groth16 to process the trust setup.
It's important to note that this trust setup is specific to each circuit.

You need one setup per circuit.

Here is a code example of the trust setup process.

```rust


use ark_bn254::Bn254;
use ark_circom::CircomBuilder;
use ark_circom::CircomConfig;
use ark_groth16::Groth16;
use ark_snark::SNARK;

fn main() {

    let cfg = CircomConfig::<Bn254>::new("main.wasm", "main.r1cs").unwrap();

    let mut builder = CircomBuilder::new(cfg);
    builder.push_input("in", 7);

    // Create an empty instance for setting it up
    let circom = builder.setup();

    // this is random bit that use one time percircuit
    let mut rng = rand::thread_rng(); 👈
    let params =
        Groth16::<Bn254>::generate_random_parameters_with_reduction(circom, &mut rng).unwrap();


}

```