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
  <br/>
  <br/>
  
  ![defi TVL](https://github.com/Onther-Tech/economics/blob/main/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202022-09-28%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%206.37.55.png)
  <br/>
  <br/>
  
  The complicated nature of Ethereum can also feed MEV. For example, it is hard to reap profits from only sending or receiving tokens. However, it is a different story if you engage in diverse financial activities like trading spots or derivatives. Lucrative MEV transactions such as arbitrages or liquidations will frequently arise. Sequencers will benefit from either directly capitalizing on such opportunities or receiving higher gas fees from searchers.

  What demonstrates the complexity of Ethereum well is Defi. In the graph above, despite taking a hit from the recent crypto crash, Defi TVL has grown about 500% since September 2020. If you lengthen the time horizon a bit more, the current size of the Defi ecosystem is approximately 120 times larger than that in September 2019. As long as the crypto industry grows continuously in the long run, the Defi ecosystem will also expand, offering more MEV chances.
  <br/>
  <br/>
  
#### 3.1.3. Layer 2 protocols take their own share of MEV
<br/>

From now on, we assume there exists only one sequencer in each layer 2 protocol based on the premise of centralized block production.
<br/>
<br/>

Even if MEV will not disappear as a whole, it does not guarantee a certain amount of MEV for individual layer 2 protocols. What if one or two dominant protocols take the whole pie? What if the competition among services is so fierce that the share for each platform is too small?

We believe each layer 2 protocol will retain MEV with monopoly power from the heterogeneous layer 2 environments. At the same time, the partial homogeneity all the layer 2 services share will put a cap on monopoly power and thus MEV they can extract.
<br/>
<br/>

![heteregeneous homogeneous](https://github.com/Onther-Tech/economics/blob/main/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202022-09-27%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%2012.52.34.png)
<br/>

Tokamak Network expects a variety of layer 2 services to coexist, meeting diverse needs.  Regarding block production, it will get centralized due to cross-domain MEV.

Since each protocol caters to specific needs, such as trading NFT or hedging risks with derivatives, layer 2 platforms can exert monopoly power over users. 

We should also note that users rarely go to other networks once they get used to a specific platform.
<br/>
<br/>

However, at the same time, all layer 2 protocols share some similarities in that they focus on scalability and rely on native token incentives.

It implies that the monopoly power mentioned above is not limitless due to some competition among layer 2 services.
<br/>
<br/>

![userMEV](https://github.com/Onther-Tech/economics/blob/main/%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202022-10-05%20%E1%84%8B%E1%85%A9%E1%84%8C%E1%85%A5%E1%86%AB%2012.41.30.png)
<br/>

The limited monopoly power affects the aggressiveness of sequencers in pursuing MEV chances.

Based on the figure above, at first, MEV is zero because there are no users. As the popularity of the layer 2 protocols grows, more people come to networks, which leads to more MEV opportunities. Interestingly, MEV increases very fast until it reaches roll-up fees. It is because sequencers can actively pursue MEV transactions with monopoly power.

However, once MEV exceeds roll-up fees, the deceleration begins. Sequencers start to worry about whether MEV activity seriously erodes the common goods. Crossing the ‘red-line’ would mean users’ departure from protocols. The competition based on partial homogeneity works this time.
<br/>
<br/>

**3.1.4. Numeric MEV modeling** 
<br/>
<br/>

We have reasoned that MEV will remain in place, and each layer 2 protocol will have a part of MEV. It is finally time to check whether the actual data supports our argument. 
<br/>
<br/>

While doing numeric modeling, we will refer to Boba Network for two reasons.

First, Boba Network is an appropriate example of a relatively small protocol in a heterogeneous system. According to L2Beat, its current market share is approximately 0.59% as of October 5th, KST.

Second, Boba Network is a good proxy for Tokamak Network. Both services utilize the optimistic roll-up technology. The size of networks, in terms of TVL, is quite similar, too.
<br/>
<br/>

- **Layer 1 fees (roll-up fees)**
  <br/>
  <br/>
  
  The transaction and state batches are submitted to Ethereum every hour in Boba Network. For the sake of simplicity, if we fix the number of transactions included in a batch as 34, the average during the recent 24 hours, the daily roll-up fees can be estimated as follows:
(As of October 5th, KST)
<br/>

<aside>
    💡 transaction & state batch examples
    
    [https://etherscan.io/tx/0xd8554666451837c2102b69d04b7da658fb063214c8ec826e057dffa441fb7653]                                (https://etherscan.io/tx/0xd8554666451837c2102b69d04b7da658fb063214c8ec826e057dffa441fb7653)

    [https://etherscan.io/tx/0x098bada6a80f025218fae21dcdd61bbed3854d18cc1c45c3f9cabb7875b9f48f](https://etherscan.io/tx/0x098bada6a80f025218fae21dcdd61bbed3854d18cc1c45c3f9cabb7875b9f48f)
<br/>
    
    [https://etherscan.io/tx/0x169f651767989fbca0e9268b378e7602a0c1cffc19fb8f3ed4779921c01c6ec3](https://etherscan.io/tx/0x169f651767989fbca0e9268b378e7602a0c1cffc19fb8f3ed4779921c01c6ec3)

    [https://etherscan.io/tx/0xbea9754d2c190912570c5fd03647c5262955208382405f779bd07dbc6d191184](https://etherscan.io/tx/0xbea9754d2c190912570c5fd03647c5262955208382405f779bd07dbc6d191184)
<br/>
    
    [https://etherscan.io/tx/0x3d3299a63dc144cbf041fba2af5e520fa0f0730b3cd0fa7dac80bfaa0474454f](https://etherscan.io/tx/0x3d3299a63dc144cbf041fba2af5e520fa0f0730b3cd0fa7dac80bfaa0474454f)

    [https://etherscan.io/tx/0x01e27250952e8c86ab6dba787f97ebaf313a82e6058fac8ef67e92d5adb464d1](https://etherscan.io/tx/0x01e27250952e8c86ab6dba787f97ebaf313a82e6058fac8ef67e92d5adb464d1)

</aside>

 1. average amount of gas required per transaction & state batch: 358,248
 2. gas price: 10~30 gwei (reflecting the recent downward trend in gas prices)
 3. **daily roll-up fees:** 358,248*(10~30 gwei)*24 = 86 ~258 million gwei = 0.086 ~ 0.258 ETH
<br/>

- **Estimated MEV a sequencer earns**
    <br/>
    <br/>
    
    According to Flashbots, as of October 5th, KST, the extracted MEV during the last 30 days is about 795K USD. Therefore, we can infer that MEV worth approximately 27K USD gets materialized daily.
    
    However, it is more like the lower bound for the actual MEV due to the omission of certain types of transactions, including CEX-DEX arbitrages and sandwich transactions. Moreover, it is the extracted MEV on Ethereum, not layer 2 networks.
    
    Therefore, adapting the original data for our modeling is crucial.
    </br>
    </br>
