# How to solve fee token dilemma in Tokamak Network

*Special thanks to Kevin.J, Darren.K, Nomad.I, Jake.J, Suah.K, Praveen.S, and Jamie for the productive feedback on the posting.*
<br/>
<br/>
## 0. Introduction
<br/>

Layer 2 is a collective term for a specific set of Ethereum scaling solutions without severely sacrificing security and decentralization. While layer 2 executes heavy computations off-chain, it relies on layer 1 or Ethereum for security and decentralization.
<br/>
<br/>

Tokamak Network has been striving to establish an on-demand layer 2 protocol. More specifically, optimistic roll-up, adopted by platforms like Optimism or Boba Network, will be at the core of our service. Being ‘optimistic’ implies that we assume the validity of transactions unless there is a challenge. If transactions get ‘rolled-up,’ multiple transactions are collected into a batch and submitted to layer 1 at once. 

In the process, TON, the native token of Tokamak Network, must play a pivotal role in incentivizing users to act in an advantageous way for the protocol. In this context, diversifying the utilities of TON is crucial. 

Among possible utilities like governance or staking, we will exclusively discuss the way to maximize the utility of TON as a fee token in this paper.
<br/>
<br/>

## 1.  Trade-off around fee token utility
<br/>

### 1.1. Why TON to be a fee token?
<br/>

If TON is a fee token, we can pay transaction fees in TON.
<br/>
<br/>

Why is it so important? No matter which applications or services people use on blockchains, making transactions is unavoidable. When you stake TON, it is a transaction. When you swap ETH for TON, it is a transaction as well. In other words, fee token utility guarantees the baseline demand for TON.

UX can be improved, too. Users do not necessarily have to hold many ETH just for transaction fees.
<br/>
<br/>

### 1.2. Fee token dilemma
<br/>

![fee token dilemma](https://github.com/Onther-Tech/economics/blob/main/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202022-09-26%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%206.16.39.png)
<br/>

Unfortunately, an extremely tricky issue has prevented many layer 2 protocols from allowing their tokens to be fee tokens: potential downward pressures on the token price.
<br/>
<br/>

The picture above shows how the ‘fee token dilemma’ arises. Layer 1 describes the underlying blockchain architecture responsible for the security and decentralization of layer 2 networks. Sequencers are entities entitled to produce blocks in the layer 2 environment. 

Let’s look at the bright side first. When users make transactions, they purchase TON to pay transaction fees, boosting the price of TON.

However, you should also see the other side of the picture. Sequencers send the information on a bunch of layer 2 transactions to layer 1 for security. The problem is that the security fees incur, and sequencers must pay these fees in ETH. Consequently, despite taking transaction fees in TON, sequencers swap some TON for ETH to pay layer 1 fees. Of course, it would bring down the price of TON.
<br/>
<br/>

## 2. Similar protocols addressing fee token dilemma
<br/>

### 2.1. Optimism
<br/>

OP token, the native token of Optimism, is not for paying transaction fees within the network. Instead, it only performs governance functions.
<br/>

![Optimism Collective](https://github.com/Onther-Tech/economics/blob/main/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202022-10-02%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%205.42.40.png)
<br/>

For example, Optimism Collective, together with Optimism Foundation, is responsible for governance in Optimism. In Token House, one of the two pillars supporting Optimism Collective, OP token holders can submit, deliberate, and vote on governance proposals, including protocol upgrades or inflation adjustment.
<br/>
<br/>

### 2.2. Boba Network
<br/>

Unlike Optimism, Boba Network has a dual-fee token system. Although ETH is a default fee token, users can also choose to pay transaction fees in the BOBA token. If using BOBA as a fee token, users get a 25% discount.
<br/>
<br/>

However, Boba Network does not directly tackle the fee token dilemma. If necessary, BOBA gets swapped for ETH to cover layer 1 fees.

Instead, it tries to indirectly assuage the dilemma by combining governance with staking. If users want to participate in the decision-making process of Boba Network, they should stake BOBA. Additionally, a portion of transaction fees accrues to staked BOBA.

In other words, Boba network utilizes incentives so that more BOBA remains within the protocol.
<br/>
<br/>

## 3. Tokamak Network: proactive approach
<br/>

Tokamak Network wants TON to be a fee token. Plus, we directly deal with the fee token dilemma by using two tools at our disposal: MEV or Maximal Extractable Value and TON seigniorage distribution.
<br/>

### 3.1. MEV(Maximal Extractable Value)
<br/>

The broader sense of MEV will remain intact in the long run. In addition, sequencers in each layer 2 protocol will manage to capture their share of MEV. It will help them cover layer 1 fees.
<br/>
<br/>

#### 3.1.1. Broader definition of MEV
<br/>

- **Conventional definition of MEV**
    <br/>
    
    In technical terms, MEV refers to the maximum value extracted from block production in excess of the standard block reward and gas fees by including, excluding, and changing the order of transactions in a block.
    
    DEX arbitrage is one of the most well-known MEV examples. Let’s say two exchanges put a different price tag on the same token. In this case, buying the token at a discount and immediately selling it at a premium generate profits.
    
    Notably, MEV is not just for block producers or sequencers. Searchers, a group of users specialized in spotting MEV opportunities with advanced algorithms or bots, can also benefit from MEV. Of course, a part of profits for searchers goes to sequencers in the form of higher gas fees. Searchers should split the MEV benefits to include their transactions first in a block.
 <br/>

- **Redefinition of MEV**
  <br/>
  
  However, the definition of MEV above is primarily about on-chain transactions. We do believe that off-chain MEV chances also exist.

  For example, if a sequencer gets compensated for putting transactions by a specific group of users first in a block, it can add to MEV, too. Users can   also pay for inserting transactions at a certain point of time in a block.

  Therefore, In this article, MEV refers to the maximum value derived from block production more than the standard block reward and gas fees. It can be   by either directly changing the sequence of transactions or selling the rights to do such actions. In other words, MEV essentially comes from the       discretion to construct blocks, either on-chain or off-chain.
 <br/>
 
#### 3.1.2. MEV will not disappear
 <br/>
 
If MEV decreases significantly in the future, it cannot be a credible source of income for sequencers to deal with layer 1 fees. In this sense, the sustainability of MEV is essential.

With the steadily increasing trend, MEV is unlikely to disappear thanks to 1) centralized block production and 2) complexity in Ethereum.
<br/>
<br/>

- **Present**
  <br/>
  <br/>
  
  ![cumulative extracted MEV](https://github.com/Onther-Tech/economics/blob/main/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202022-09-22%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%205.16.10.png)
  <br/>
  
  The graph above shows that the cumulative extracted MEV has increased significantly over the last two years. As of now, approximately 676 million USD   of MEV has been extracted.

  More importantly, this figure only considers the MEV from arbitrages and liquidations. Some lucrative MEV opportunities, including sandwich             transactions, have been omitted. Plus, even in arbitrages, CEX-DEX arbitrages have not been counted due to the lack of information related to the CEX   component. On top of that, potential off-chain MEV transactions are off the table, too.

  Consequently, the actual MEV, as we defined earlier, is likely to be much larger than the number measured by Flashbots.
  <br/>
  <br/>
  
- **Future**
  <br/>
  <br/>
  
  ![homogeneous](https://github.com/Onther-Tech/economics/blob/main/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202022-09-08%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%207.08.53.png)
  <br/>
  
  ![heterogeneous](https://github.com/Onther-Tech/economics/blob/main/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202022-09-27%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%2012.51.15.png)
  <br/>
  
  If the block production gets centralized, a small number of sequencers, if not only, handle transactions. Unlike decentralized sequencers, since there is less competition and uncertainties in becoming a block producer, it would be much easier to pursue MEV.

  Then, how does block production get centralized? It is closely related to the future layer 2 landscape proposed by Vitalik Buterin. The figure above illustrates the two possibilities discussed in his famous article ‘Endgame’: 1) a homogenous system where a small number of similar chains handle most of the Ethereum activities or 2) a heterogeneous system where multiple different chains cater to diverse needs. 

  Interestingly, both scenarios can lead to the same conclusion: centralized block production. In the case of a homogeneous world, the larger computational capacity for higher TPS would render the block production centralized. As for a heterogeneous ecosystem, potential cross-domain MEV may make centralized block production more likely.
