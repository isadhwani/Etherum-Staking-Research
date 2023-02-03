## Ethereum 
Ethereum is one of the most influential blockchains and has hundreds of currencies built off its network. Ethereum enables us to represent anything we own as a tradable, non-fungible token. After being deployed in 2015 with a proof of work validation system, Ethereum is finally transitioning to the faster and more environmentally friendly proof of stake. After years of delays, Ethereum's Goleri Testnet completed the merge on August 10, 2022. The full Ethereum merge is scheduled for September 19, 2022. 

### Proof of Work vs Proof of Stake
Proof of Work(PoW) has proven a successful validation method, but the advancement of Proof of Stake(PoS) offers the following advantages: 
#### Energy use
>The Ethereum Foundation estimates that the merge will cut energy consumption by around 99.6%. This enormous reduction comes primarily from no longer requiring mining.
#### Minting of new coins
> Because significantly less capital is invested in mining new coins, the protocol can give out fewer new coins. Miners no longer have to operate expensive machinery and instead use easily aquired hardware to run validation software.  Block rewards will be cut by an estimated [80%](https://time.com/nextadvisor/investing/cryptocurrency/ethereum-merge-price-this-week/)   
#### Dishonest nodes
> The Ethereum network is designed such that validators are always encouraged to act in the best interest of the network. The more ether you stake, the more risk you have of having your funds slashed. Because of the threat of slashing and rewarding honest nodes, it is substantially less feasible for mining "cartels" to hog the network and act selfishly. Here is an example of this in a PoW protocol [article](https://www.cs.cornell.edu/~ie53/publications/btcProcFC.pdf)
#### Centralization
> In a PoW system, the miners with the fastest hardware often have the best opportunity to mine new blocks, and therefore receive the lion's share of the rewards. In contrast, validators are selected with weighted randomness dependent on their stake. Due to the low hardware requirement and relativlty manageable 32 ETH minimum stake, participating in the validation process is far more feasible for individuals to join in. For those with more funds, your rewards are proportional to your invested stake. For example, $10 million worth of stake will give you exactly 10 times higher returns than $1 million of coins. 
#### 51% attack
> Because of the constant threat of being slashed, node participating in a 51% attack is at severe risk of losing all of their funds. No controlling attack can happen without at least 1/3 of all staked ether being destroyed

#### Problems with aBFT PoS 
Past Asynchronous Byzantine Fault Tolerance(aBFT) PoS implementations suffer from the "Nothing at Stake" problem, which occurs when a validator has to choose between two different chains. In a chain-based PoS, it is more economically viable for validators to split their votes in favor of making new chains. This occurs here because validators are rewarded whenever a new block is created, and splitting one's vote supports the creation of two new blocks on two chains. In PoW, creating two new blocks doubles the amount of computing power required, so this problem does not occur. 

The problem here is that without an attack, the network can no longer reach consensus and is now vulnerable to several different attacks. Eth 2.0 solves this problem in their Gasper algorithm, specifically the LMD Ghost forking algorithm. 

### Gasper
The Gasper protocol is a combination of the LMD Ghost Forking Algorithm and Casper block finalization and slashing algorithm. 

#### Forking
LMD Ghost stands for "Latest Message-Driven Greedy Heaviest Observed Subtree", and is an algorithm to help the network decide what to do in case of forking in the network. Forking means there are multiple latest blocks and the network is unsure of which one to choose. This occurs either with large network asynchronicity or a dishonest block proposal. Click [here](https://medium.com/@aditya.asgaonkar/bitwise-lmd-ghost-an-efficient-cbc-casper-fork-choice-rule-6db924e57d1f) for specifics on the LMD Ghost algorithm.
#### Finality
Finality in Ethereum is managed with set checkpoint blocks at the beginning of each epoch. If 2/3 of the total staked ether votes on a proposed checkpoint block, the checkpoint becomes `justified`. The process repeats until the next epoch, resulting in a new checkpoint block. Once this new checkpoint is voted on, the first block becomes officially `finalized`, and it would now require burning 1/3 of the total staked ether to revert to a previous checkpoint.  
#### Slashing
Slashing is defined mathematically in the Gasper [whitepaper](https://arxiv.org/pdf/2003.03052.pdf) in section three. In general, validators are slashed when they either split their vote, vote for the wrong checkpoint or act maliciously against the network. Slashing is flexible, in that any accountable problem can be adjusted for. 

### How to Stake Ethereum
Staking your ether is possible through running your node or validator, pooled staking, and centralized exchanges. 

#### Running a Node 
Running a node is the most low-level way to stake and requires 32 ETH, a dedicated machine, and a valid set of signing keys. Running your node allows you full control over your funds and staking setup. You will earn rewards directly from the protocol and strengthen the entire network. The rewards you earn depend on your stake in the network and the reliability of your hardware. 

#### Staking as a service
Delegating is the process of acquiring the required 32 ETH and letting a third party run the node for you. This requires you to trust a third party with acting honestly with your funds. 

#### Pooled Staking
You could also send you're stake to a Pool Staking service such as Rocket Pool, Lido and StakeWise. You will still earn staking rewarsds, but someone else will control you're funds and takes a cut of your rewards.

#### Rocketpool Node Operation
Our node is currently running Geth as an execution client and Prysm as a consensus client. Both were installed using docker and Rocketpools CLI. After syncing for over a week, both clients were ready to begin. We created a hot wallet with its private key stored on the VM so we can execute complicated ethereum transactions with Rocketpool's CLI, such as setting a withdrawl and voting address, registering the node, and combining funds to create a minipool. A minipool is Rocketpools alternative for the expensive 32 eth starting point for running a node. Rocketpool pools your eth with 16 of theirs, allowing us to run a node for only half the cost. We still earn full rewards on our 16 eth and can even deploy multiple minipools on our node

#### Liquid Staking
Liquid staking or live staking is the process of staking coins without locking them up. When you stake eth with a node, your 16 or 32 eth is locked until ethereum updates its protocol to allow for withdrawing eth. Liquid staking allows you to stake and withdraw when ever you want. With Rocketpool, you can swap eth for their native token, rpl and stake that with your node. Staking rpl gives comparable rewards to eth and can be withdrawn at any time. 

### Sources
- https://ethereum.org/en/developers/docs/consensus-mechanisms/pos/
- https://arxiv.org/pdf/2003.03052.pdf
- https://vitalik.ca/general/2017/12/31/pos_faq.html
- https://blog.ethereum.org/2016/05/09/on-settlement-finality
- https://ethereum.org/en/developers/docs/consensus-mechanisms/pos/gasper/#fork-choice
- https://arxiv.org/pdf/1710.09437.pdf
