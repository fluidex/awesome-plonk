# Awesome PLONK [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

## Papers

+ [PLONK: Permutations over Lagrange-bases for Oecumenical Noninteractive arguments of Knowledge](https://eprint.iacr.org/2019/953.pdf)
    * slides:
        * [Simons Institute 2019](https://github.com/arielgabizon/Lectures/blob/master/PlonkSimonsCorrected.pdf)
        * [Stanford Blockchain Conference 2020](https://github.com/arielgabizon/Lectures/blob/master/StanfordJan2020UniversalUpdatable.pdf)
            - [transcripts](https://diyhpl.us/wiki/transcripts/stanford-blockchain-conference/2020/plonk/)
+ [Proposal: The Turbo-PLONK program syntax for specifying SNARK programs](https://docs.zkproof.org/pages/standards/accepted-workshop3/proposal-turbo_plonk.pdf)
    * Turbo-PLONK uses custom gates. Custom gates can make [Halo](https://eprint.iacr.org/2019/1021.pdf)-style Recursive Proof Composition efficient in PlonK.
        - [[BCMS20]](https://eprint.iacr.org/2020/499.pdf) further formalizes halo-style Recursive Proof Composition, and call it as an Accumulation scheme
+ [plookup: A simplified polynomial protocol for lookup tables](https://eprint.iacr.org/2020/315.pdf)
    * slides:
        * [plookup: speeding up SNARKs on non-friendly functions with lookup tables](https://github.com/arielgabizon/Lectures/blob/master/plookupzksummit2020.pdf)
        * [Plookup in action](https://github.com/arielgabizon/Lectures/blob/master/plookupinactionDystopia2020.pdf)
* [fflonK: a Fast-Fourier inspired verifier efficient version of PlonK](https://eprint.iacr.org/2021/1167.pdf)
   * extends KZG10 commitment scheme and allows for multiple polynomials to be represented by a single commitment
   * requiring 6 scalar multiplications and 2 bilinear pairings
   * verifier efficient
      * saves gas on Ethereum
      * at the cost of roughly tripling the prover time
+ [Public inputs in PlonK’s permutation argument](https://github.com/arielgabizon/plonk-addendum/blob/master/plonk-pubinputs.pdf)
+ [SHPLONK](https://eprint.iacr.org/2020/081.pdf)
+ [REDSHIFT: Transparent SNARKs from List Polynomial Commitment IOPs](https://eprint.iacr.org/2019/1400.pdf)
+ Reinforced Concrete: A new ZK friendly hash function. When Plookup is enabled, it can be up to 17x faster than Poseidon (50 cycles/byte), and only 7 times slower than Blake2.
    + [paper](https://drive.google.com/file/d/1MCIqD8XwKrHVBQPc26XjAmM9RyrLDpjw/view)
    + [website](https://www.rc-hash.info/)

## Forums
+ [PLONK Café](https://www.plonk.cafe/)

## Articles
+ [Understanding PLONK](https://vitalik.ca/general/2019/09/22/plonk.html) by Vitalik Buterin
+ [Plonk tutorial](https://github.com/barryWhiteHat/plonk_tutorial) by barryWhiteHat
+ metastate's plonk-by-hand series ([[1]](https://research.metastate.dev/plonk-by-hand-part-1/), [[2]](https://research.metastate.dev/plonk-by-hand-part-2-the-proof/) & [[3]](https://research.metastate.dev/plonk-by-hand-part-3-verification/))
    * [plonk-by-fingers](https://github.com/adria0/plonk-by-fingers) is a toy implementation in rust
* [On PLONK and plookup](https://research.metastate.dev/on-plonk-and-plookup/)
* [From AIRs to RAPs - how PLONK-style arithmetization works](https://hackmd.io/@aztec-network/plonk-arithmetiization-air)
+ [Multiset checks in PLONK and Plookup](https://hackmd.io/@XYwo0oEXTEGRpej1SQVMlg/ByFgSDA7D) by Ariel Gabizon
+ [Plonk and PLookup](https://hackmd.io/@7dpNYqjKQGeYC7wMlPxHtQ/BJpNmNW0L) by Dmitry Khovratovich
+ [PLONK custom gates design considerations](https://kobi.one/2021/05/20/plonk-custom-gates.html) by Kobi Gurkan
+ [Thoughts on Plookup implementation of Sha256 and Keccak](https://hackmd.io/xfgP5_uMTZyaEJJG4EJoRQ?view) by Konstantce
+ [Plonk and Poseidon](https://drive.google.com/file/d/1bZZvKMQHaZGA4L9eZhupQLyGINkkFG_b/view) (Plonk adaptation tailored to Poseidon) by Dmitry Khovratovich
+ [Non-native field arithmetic using custom gates](https://hackmd.io/@arielg/B13JoihA8)
+ [Fast recursive arguments based on Plonk and Halo](https://mirprotocol.org/blog/Fast-recursive-arguments-based-on-Plonk-and-Halo)
+ [Adding zero knowledge to Plonk-Halo](https://mirprotocol.org/blog/Adding-zero-knowledge-to-Plonk-Halo)
+ [UltraPLONK Arithmetization in Halo 2](https://zcash.github.io/halo2/concepts/arithmetization.html)
+ TurboPLONK benchmarks
   + https://medium.com/aztec-protocol/plonk-benchmarks-2-5x-faster-than-groth16-on-mimc-9e1009f96dfe
   + https://medium.com/aztec-protocol/plonk-benchmarks-ii-5x-faster-than-groth16-on-pedersen-hashes-ea5285353db0
+ AZTEC Ignition ([setup codes here](https://github.com/AztecProtocol/Setup), [verification codes here](https://github.com/AztecProtocol/ignition-verification))
    + [Ignition: Trusted Setup MPC Ceremony for PLONK](https://medium.com/aztec-protocol/aztec-announcing-our-ignition-ceremony-757850264cfe)
        * [How the Ceremony Works - Basic](https://medium.com/aztec-protocol/aztec-how-the-ceremony-works-5c23a54e2dd9)
        * [How the Ceremony Works - Advanced](https://medium.com/aztec-protocol/aztec-how-the-ceremony-works-9f021cf190d0)
    + [AZTEC CRS: The Biggest MPC Setup in History has Successfully Finished](https://medium.com/aztec-protocol/aztec-crs-the-biggest-mpc-setup-in-history-has-successfully-finished-74c6909cd0c4)

## Podcasts / Videos
+ [Zero Knowledge Episode 112: Dive into Plonk!](https://www.zeroknowledge.fm/112)
+ [ZK Study Club - Plonk with Zac Williamson](https://youtu.be/NqrVcDuQ8hM)
+ [Zac Williamson on PLONK and TurboPLONK at ZKSummit](https://youtu.be/ty-LZf0YCK0)
+ [zkSummit5: PLONK without FFTs - Justin Drake (EF)](https://www.youtube.com/watch?v=ffXgxvlCBvo&list=PLj80z0cJm8QFnY6VLVa84nr-21DNvjWH7&index=25)
+ [zkSummit: plookup: Speeding up the PLONK prover - Zac Williamson & Ariel Gabizon](https://youtu.be/Vdlc1CmRYRY) (with Turbo PLONK & Ultra PLONK benchmarks)
+ [ZK-LDN 0x04: On Marlin and PLONK](https://www.youtube.com/watch?v=gDpwBYHjcHA)
+ [Aztec: Plonk in Dystopian Times](https://www.youtube.com/watch?v=nz_VdPbCT64)
+ [Polynomial protocols for range proofs](https://www.youtube.com/watch?v=8n3c8fbi9Ac)
+ How does PLONK work? ([Part 1](https://www.cryptologie.net/article/529/how-does-the-general-purpose-zero-knowledge-proof-system-plonk-work/), [Part 2](https://www.cryptologie.net/article/530/how-does-plonk-work-part-2-an-overview/))

## Demo
+ dusk-network
    + [Zero-Knowledge: PLONK Demo - Dusk](https://dusk.network/news/zero-knowledge-plonk-demo)
    + [Zero-Knowledge: PLONK Demo 2 - Dusk](https://dusk.network/news/zero-knowledge-plonk-demo-2)

## Implementations
+ [Aztec's implementation in C++](https://github.com/AztecProtocol/barretenberg/tree/master/barretenberg/src/aztec/plonk)
+ [Matter Labs' implementation in Rust](https://github.com/matter-labs/bellman/tree/plonk_release/src/plonk)
+ [plonky: Recursive SNARKs based on Plonk and Halo](https://github.com/mir-protocol/plonky)
+ [dusk-plonk](https://github.com/dusk-network/plonk)
