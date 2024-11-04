## zkSync

<br>

### tl; dr

<br>

* layer-2 scaling solution for ethereum, aiming for scalability. 
* zkSync 2 is called Era, zkSync 1 is called light.
* uses "optimistic" transfers, which allow users to send and receive txs without waiting for conformation (reducing tx times, and allowing higher tx throughput).
* tvl: zkSync era has higher transfers of assets ($125M) than Polygon zkEVM ($2.57M) 
* sybil addresses: zkSync era has more potential sybil addresses based on the depositing addresses’ wallet age and usage on Ethereum/Layer 2 networks. 
* tx costs: ~$0.25-$2, high compared to optimistic rollups like arbitrum and Ootimism ($0.13 - $0.45)

<br>

----

### zksync era

* zksync era archtecture:
  * native account abstraction (any account on era can pay fees in any tokens or even transact with zero fees on protocols willing to subsidize usage)
  * powerful llvm compiler
  * data compression (publishing states diffs instead of tx inputs, enabling data compression, more frequent oracle updates, cheap privacy, seamless off-chain sotrage extension)
  * hyperscalability 


<br>

----

### cool resources

<br>

* **[zksync ecosystem](https://ecosystem.zksync.io/)**
* **[gm zkEVM, by zksync](https://blog.matter-labs.io/gm-zkevm-171b12a26b36)**
* **[dune board zksync vs. polygon zkEVM](https://dune.com/21shares_research/zkevm-comparison-zksync-era-vs-polygon-hermez)**
