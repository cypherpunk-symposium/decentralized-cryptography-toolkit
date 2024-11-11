## zero-knowledge 

<br>

### tl; dr

<br>

##### proofs

* **zero-knowledge proofs** represent **programs as circuits**, where a **prover** generates a proof from public and private inputs, and a **verifier** computes the output if the statement is correct (without any information regarding the private input).
* three fundamental characteristics define a zkp:
  * completeness (if a statement is true, then an honest verifier can be convinced by an honest prover that they possess knowledge about the correct input).
  * soundness (if a statement is false, then no dishonest prover can unilaterally convince an honest verifier that they have knowledge about the correct input).
  * zero-knowledge (if the state is true, then the verifier learns nothing more from the prover other than that).
* zk proofs use cases:
  * **private transactions**: blockchains such as zcash, with privacy-preserving txs.
  * **verifiable computations**: decentralized oracle networks, providing smart contracts with access to off-chain data.
  * **highly-scalable and secure l2s**: verifiable computations through methods such as zk-rollups, validiums, and volition by they use l1s as a settlement layer.
  * **decentralized identity and authentication**: zkps can underpin identity management systems to enable users to validate their identity.

<br>

<p align="center">
<img src="https://user-images.githubusercontent.com/1130416/234397705-090a0c7b-5d96-49f8-8eaa-183297e3fe37.png" width="60%" align="center" style="padding:1px;border:1px solid black;"/>

<br>

##### zk-rollups

<br>

* **zk-rollups** write transactions to ethereum as calldata, using compression techniques to reduce transaction data. while calldata is not stored as part of the evm's state, it persists on-chain as part of the chain's history logs.
* the zk-rollup's state, which includes l2 accounts and balances, is represented as a merkle tree.
* users in the zk-rollup sign transactions and submit them to l2 operators for processing and inclusion in the next batch. in some cases, the operator is a centralized entity (the sequencer), that executes transactions, aggregates them into batches, and submits to L1.
* the rollup contract won't automatically accept the proposed state commitment until the operator proves the new merkle root resulted from correct updates to the rollup’s state (this comes from validity proofs).
* goals:
 * lower gas fees (by tx baches and submitting minimal on-chain data)
 * higher throughput (fast tx speeds, reduced confirmation times, up to 100x)
 * fastter confirmation time (no need to wait for block confirmations on the base layer, finality on l2)
 * privacy (no info about the tx is leaked, concealing tx amounts and recipients)
 * proof generation costs can be high (reducing proof generation costs involves using more efficient proof systems or circuit designs or incentivizing provers).
 * high circuit complexity can affect zk-rollups' scalability and usability
 * compatibility issues (not fully compatible with existing smart contracts or tools)

<br>

----

### chapters

<br>

* **[zkEVMs](zkEVMs)**
* **[proofs](proofs)**
* **[machine learning](machine_learning)**

<br>

----

### cool resources

<br>

#### overview

* **[zk-learning mooc, by d. boneh et al.](https://zk-learning.org/)**
* **[course on modern zero knowledge cryptography](https://zkiap.com/)**
* **[pse's publications](https://mirror.xyz/privacy-scaling-explorations.eth)**
* **[zero knowledge podcast youtube](https://www.youtube.com/@zeroknowledgefm)**
* **[what are zk proofs, by ef](https://ethereum.org/en/zero-knowledge-proofs/)**
* **[the zk-ECDSA landscape, by pse](https://mirror.xyz/privacy-scaling-explorations.eth/djxf2g9VzUcss1e-gWIL2DSRD4stWggtTOcgsv1RlxY)**
* **[zero knowledge dapp from 0 to production, by v. plasencia](https://vivianblog.hashnode.dev/how-to-create-a-zero-knowledge-dapp-from-zero-to-production)**
* **[an evolution of models for zkps, by s. meiklejohn](https://youtube.com/watch?v=HO97kVMI3SE&t=2s)**
* **[a new era: safe deploys on zksync era](https://safe.mirror.xyz/yvnFJxFWrlHTXZFBLfQiKuPyW7zwa2TSurXz5Btl9Jk)**
* **[binius: highly efficient proofs over binary fields, by vub](https://vitalik.eth.limo/general/2024/04/29/binius.html)**
* **[possible futures of the ethereum protocol, part 4: the verge, by vub](https://vitalik.eth.limo/general/2024/10/23/futures4.html)**
* **the state of zk applications in ethereum, by andyguzman.eth: [1](https://mirror.xyz/andyguzman.eth/p4nNk7Rr-2i-uZDO_lTHJEWtNv3nYt2N2z3Cwly8RHc) and [2](https://mirror.xyz/andyguzman.eth/ZZRLBlx2KjlNnQ84v1doMKg_8QO-XRjYxFfT1Fm_ZDw)**
 * **[an incomplete guide to folding, by taiko labs](https://taiko.mirror.xyz/tk8LoE-rC2w0MJ4wCWwaJwbq8-Ih8DXnLUf7aJX1FbU)**
* **[zeroing into zkvms, by taiko labs](https://taiko.mirror.xyz/e_5GeGGFJIrOxqvXOfzY6HmWcRjCjRyG0NQF1zbNpNQ)**
* **[awesome zk list](https://github.com/ventali/awesome-zk)**

<br>

#### playgrounds

* **[zkrepl](https://zkrepl.dev/)**

<br>

#### coprocessors provers
* **[langrage network](https://www.lagrange.dev/)** (hyper-parallel zk coprocessing)
* **[brevis](https://brevis.network/)** (a smart zk coprocessor for blockchains)
* **[herodotus](https://herodotus.dev/)** (cryptographic integrity verification)

<br>

#### optimistic verifcation provers
* **[uma protocol](https://uma.xyz/)**
* **[accross protocol](https://github.com/across-protocol)**

<br>

#### zk-circuits provers
* **[succinct](https://github.com/succinctlabs/sp1-contract-call)**
