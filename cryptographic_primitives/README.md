## cryptographic primitives

<br>

### bls signatures

<br>

* used in the beacon chain to verify large numbers of signtures.
* invented by dan boneh, ben lynn, and hovav shacham.
* in optimistic rollups such as arbitrum and optimism, each tx must be accompanied by its own signature. these signatures are stored on l1 calldata, a read-only format that's commited as a part of a transaction rather than to (expensive) contract storage.
* storing txs and signatures as calldata is the cheapst method available for rollups to keep data on l1.
* the key property of bls signatures is that multiple signatures can be combined into one - so only one aggregate signature needs to be verified and stored on-chain (meaning less gas fees).

<br>

----

### shamir's secret sharing

<br>

* secret sharing algorithm to distribute private information among a group, and the secret cannot be revealed unless a quorum of the groups acts together to pool their knowledge.
* the secret is matematically divided into parts. if an attacker steals some shares, it's impossible for the attacker to reconstrcut the secret unless they have stolen a quorum number of shares.
* uses cases: password managers, encrypted emails, and crypto wallets.

<br>

---

### cool resources

<br>

#### cool courses

* **[number theory course by stanford (2023)](https://crypto.stanford.edu/pbc/notes/numbertheory/)**
* **[galois fields, part one (2020)](https://www.youtube.com/watch?v=yBVqk4YM2VY)**
  
<br>

#### cool papers

* **[bls multi-signatures with pub-key aggregation (2018)](https://crypto.stanford.edu/~dabo/pubs/papers/BLSmultisig.html)**
* **[ring confidential transactions (2015)](https://eprint.iacr.org/2015/1098.pdf)**
* **[intro to differential power analysis (2011)](https://link.springer.com/content/pdf/10.1007/s13389-011-0006-y.pdf)**
* **[pairing-friendly elliptic curves of prime order (2005)](https://eprint.iacr.org/2005/133.pdf)**

<br>

#### cool talks

* **[an introduction to cryptography, new and old, by atheartengineer et al. (2024)](https://www.youtube.com/watch?v=E6u3uQGP9J4)**
* **[programmable cryptography devcon panel, by barry and gang (2024)](https://www.youtube.com/watch?v=S6ixhGBnvKc)**
