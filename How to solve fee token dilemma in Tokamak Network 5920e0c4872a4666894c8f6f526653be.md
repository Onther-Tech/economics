# How to solve fee token dilemma in Tokamak Network

*Special thanks to Kevin.J, Darren.K, Nomad.I, Jake.J, Suah.K, Praveen.S, and Jamie for the productive feedback on the posting.*

## 0. Introduction

Layer 2 is a collective term for a specific set of Ethereum scaling solutions without severely sacrificing security and decentralization. While layer 2 executes heavy computations off-chain, it relies on layer 1 or Ethereum for security and decentralization.

Tokamak Network has been striving to establish an on-demand layer 2 protocol. More specifically, optimistic roll-up, adopted by platforms like Optimism or Boba Network, will be at the core of our service. Being ‘optimistic’ implies that we assume the validity of transactions unless there is a challenge. If transactions get ‘rolled-up,’ multiple transactions are collected into a batch and submitted to layer 1 at once. 

In the process, TON, the native token of Tokamak Network, must play a pivotal role in incentivizing users to act in an advantageous way for the protocol. In this context, diversifying the utilities of TON is crucial. 

Among possible utilities like governance or staking, we will exclusively discuss the way to maximize the utility of TON as a fee token in this paper.

## 1.  Trade-off around fee token utility

### **1.1. Why TON to be a fee token?**

 

If TON is a fee token, we can pay transaction fees in TON.

Why is it so important? No matter which applications or services people use on blockchains, making transactions is unavoidable. When you stake TON, it is a transaction. When you swap ETH for TON, it is a transaction as well. In other words, fee token utility guarantees the baseline demand for TON.

UX can be improved, too. Users do not necessarily have to hold many ETH just for transaction fees.

### **1.2. Fee token dilemma**

![**Example: fee token dilemma**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-09-26_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_6.16.39.png)

**Example: fee token dilemma**

Unfortunately, an extremely tricky issue has prevented many layer 2 protocols from allowing their tokens to be fee tokens: potential downward pressures on the token price.

The picture above shows how the ‘fee token dilemma’ arises. Layer 1 describes the underlying blockchain architecture responsible for the security and decentralization of layer 2 networks. Sequencers are entities entitled to produce blocks in the layer 2 environment. 

Let’s look at the bright side first. When users make transactions, they purchase TON to pay transaction fees, boosting the price of TON.

However, you should also see the other side of the picture. Sequencers send the information on a bunch of layer 2 transactions to layer 1 for security. The problem is that the security fees incur, and sequencers must pay these fees in ETH. Consequently, despite taking transaction fees in TON, sequencers swap some TON for ETH to pay layer 1 fees. Of course, it would bring down the price of TON.

## 2. Similar protocols addressing fee token dilemma

### 2.1. Optimism

OP token, the native token of Optimism, is not for paying transaction fees within the network. Instead, it only performs governance functions. 

![**Optimism Collective (Source: Optimism)**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-10-02_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_5.42.40.png)

**Optimism Collective (Source: Optimism)**

For example, Optimism Collective, together with Optimism Foundation, is responsible for governance in Optimism. In Token House, one of the two pillars supporting Optimism Collective, OP token holders can submit, deliberate, and vote on governance proposals, including protocol upgrades or inflation adjustment.

### 2.2. Boba Network

Unlike Optimism, Boba Network has a dual-fee token system. Although ETH is a default fee token, users can also choose to pay transaction fees in the BOBA token. If using BOBA as a fee token, users get a 25% discount.

However, Boba Network does not directly tackle the fee token dilemma. If necessary, BOBA gets swapped for ETH to cover layer 1 fees.

Instead, it tries to indirectly assuage the dilemma by combining governance with staking. If users want to participate in the decision-making process of Boba Network, they should stake BOBA. Additionally, a portion of transaction fees accrues to staked BOBA.

In other words, Boba network utilizes incentives so that more BOBA remains within the protocol.

## 3. Tokamak Network: proactive approach

Tokamak Network wants TON to be a fee token. Plus, we directly deal with the fee token dilemma by using two tools at our disposal: MEV or Maximal Extractable Value and TON seigniorage distribution.

### 3.1. MEV(Maximal Extractable Value)

The broader sense of MEV will remain intact in the long run. In addition, sequencers in each layer 2 protocol will manage to capture their share of MEV. It will help them cover layer 1 fees.

 

**3.1.1. Broader definition of MEV**

- **Conventional definition of MEV**
    
    
    In technical terms, MEV refers to the maximum value extracted from block production in excess of the standard block reward and gas fees by including, excluding, and changing the order of transactions in a block.
    
    DEX arbitrage is one of the most well-known MEV examples. Let’s say two exchanges put a different price tag on the same token. In this case, buying the token at a discount and immediately selling it at a premium generate profits.
    
    Notably, MEV is not just for block producers or sequencers. Searchers, a group of users specialized in spotting MEV opportunities with advanced algorithms or bots, can also benefit from MEV. Of course, a part of profits for searchers goes to sequencers in the form of higher gas fees. Searchers should split the MEV benefits to include their transactions first in a block.
    

- **Redefinition of MEV**

However, the definition of MEV above is primarily about on-chain transactions. We do believe that off-chain MEV chances also exist.

For example, if a sequencer gets compensated for putting transactions by a specific group of users first in a block, it can add to MEV, too. Users can also pay for inserting transactions at a certain point of time in a block.

Therefore, In this article, MEV refers to the maximum value derived from block production more than the standard block reward and gas fees. It can be by either directly changing the sequence of transactions or selling the rights to do such actions. In other words, MEV essentially comes from the discretion to construct blocks, either on-chain or off-chain.

**3.1.2. MEV will not disappear**

If MEV decreases significantly in the future, it cannot be a credible source of income for sequencers to deal with layer 1 fees. In this sense, the sustainability of MEV is essential.

With the steadily increasing trend, MEV is unlikely to disappear thanks to 1) centralized block production and 2) complexity in Ethereum.

- **Present**

![**Cumulative Extracted MEV(USD) (Source: Flashbots)**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-09-22_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_5.16.10.png)

**Cumulative Extracted MEV(USD) (Source: Flashbots)**

The graph above shows that the cumulative extracted MEV has increased significantly over the last two years. As of now, approximately 676 million USD of MEV has been extracted.

More importantly, this figure only considers the MEV from arbitrages and liquidations. Some lucrative MEV opportunities, including sandwich transactions, have been omitted. Plus, even in arbitrages, CEX-DEX arbitrages have not been counted due to the lack of information related to the CEX component. On top of that, potential off-chain MEV transactions are off the table, too.

Consequently, the actual MEV, as we defined earlier, is likely to be much larger than the number measured by Flashbots.

- **Future**
    
    
    ![**Homogeneous system**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-09-08_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_7.08.53.png)
    
    **Homogeneous system**
    
    ![**Heterogeneous system**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-09-27_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_12.51.15.png)
    
    **Heterogeneous system**
    
    If the block production gets centralized, a small number of sequencers, if not only, handle transactions. Unlike decentralized sequencers, since there is less competition and uncertainties in becoming a block producer, it would be much easier to pursue MEV.
    
    Then, how does block production get centralized? It is closely related to the future layer 2 landscape proposed by Vitalik Buterin. The figure above illustrates the two possibilities discussed in his famous article ‘Endgame’: 1) a homogenous system where a small number of similar chains handle most of the Ethereum activities or 2) a heterogeneous system where multiple different chains cater to diverse needs. 
    
    Interestingly, both scenarios can lead to the same conclusion: centralized block production. In the case of a homogeneous world, the larger computational capacity for higher TPS would render the block production centralized. As for a heterogeneous ecosystem, potential cross-domain MEV may make centralized block production more likely.
    
    ![**Defi TVL (Source: DefiLlama)**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-09-28_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_6.37.55.png)
    
    **Defi TVL (Source: DefiLlama)**
    
    The complicated nature of Ethereum can also feed MEV. For example, it is hard to reap profits from only sending or receiving tokens. However, it is a different story if you engage in diverse financial activities like trading spots or derivatives. Lucrative MEV transactions such as arbitrages or liquidations will frequently arise. Sequencers will benefit from either directly capitalizing on such opportunities or receiving higher gas fees from searchers.
    
    What demonstrates the complexity of Ethereum well is Defi. In the graph above, despite taking a hit from the recent crypto crash, Defi TVL has grown about 500% since September 2020. If you lengthen the time horizon a bit more, the current size of the Defi ecosystem is approximately 120 times larger than that in September 2019. As long as the crypto industry grows continuously in the long run, the Defi ecosystem will also expand, offering more MEV chances.
    

**3.1.3. Layer 2 protocols take their own share of MEV**

From now on, we assume there exists only one sequencer in each layer 2 protocol based on the premise of centralized block production.

Even if MEV will not disappear as a whole, it does not guarantee a certain amount of MEV for individual layer 2 protocols. What if one or two dominant protocols take the whole pie? What if the competition among services is so fierce that the share for each platform is too small?

We believe each layer 2 protocol will retain MEV with monopoly power from the heterogeneous layer 2 environments. At the same time, the partial homogeneity all the layer 2 services share will put a cap on monopoly power and thus MEV they can extract.

![**Heterogeneous system with some homogeneity**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-09-27_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_12.52.34.png)

**Heterogeneous system with some homogeneity**

Tokamak Network expects a variety of layer 2 services to coexist, meeting diverse needs.  Regarding block production, it will get centralized due to cross-domain MEV.

Since each protocol caters to specific needs, such as trading NFT or hedging risks with derivatives, layer 2 platforms can exert monopoly power over users. 

We should also note that users rarely go to other networks once they get used to a specific platform.

However, at the same time, all layer 2 protocols share some similarities in that they focus on scalability and rely on native token incentives.

It implies that the monopoly power mentioned above is not limitless due to some competition among layer 2 services.

![**Example: How far a sequencer can go in terms of pursuing MEV**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-10-05_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_12.41.30.png)

**Example: How far a sequencer can go in terms of pursuing MEV**

The limited monopoly power affects the aggressiveness of sequencers in pursuing MEV chances.

Based on the figure above, at first, MEV is zero because there are no users. As the popularity of the layer 2 protocols grows, more people come to networks, which leads to more MEV opportunities. Interestingly, MEV increases very fast until it reaches roll-up fees. It is because sequencers can actively pursue MEV transactions with monopoly power.

However, once MEV exceeds roll-up fees, the deceleration begins. Sequencers start to worry about whether MEV activity seriously erodes the common goods. Crossing the ‘red-line’ would mean users’ departure from protocols. The competition based on partial homogeneity works this time.

**3.1.4. Numeric MEV modeling** 

We have reasoned that MEV will remain in place, and each layer 2 protocol will have a part of MEV. It is finally time to check whether the actual data supports our argument. 

While doing numeric modeling, we will refer to Boba Network for two reasons.

First, Boba Network is an appropriate example of a relatively small protocol in a heterogeneous system. According to L2Beat, its current market share is approximately 0.59% as of October 5th, KST.

Second, Boba Network is a good proxy for Tokamak Network. Both services utilize the optimistic roll-up technology. The size of networks, in terms of TVL, is quite similar, too.

- **Layer 1 fees (roll-up fees)**

The transaction and state batches are submitted to Ethereum every hour in Boba Network. For the sake of simplicity, if we fix the number of transactions included in a batch as 34, the average during the recent 24 hours, the daily roll-up fees can be estimated as follows:
(As of October 5th, KST)

<aside>
💡 transaction & state batch examples

[https://etherscan.io/tx/0xd8554666451837c2102b69d04b7da658fb063214c8ec826e057dffa441fb7653](https://etherscan.io/tx/0xd8554666451837c2102b69d04b7da658fb063214c8ec826e057dffa441fb7653)

[https://etherscan.io/tx/0x098bada6a80f025218fae21dcdd61bbed3854d18cc1c45c3f9cabb7875b9f48f](https://etherscan.io/tx/0x098bada6a80f025218fae21dcdd61bbed3854d18cc1c45c3f9cabb7875b9f48f)

[https://etherscan.io/tx/0x169f651767989fbca0e9268b378e7602a0c1cffc19fb8f3ed4779921c01c6ec3](https://etherscan.io/tx/0x169f651767989fbca0e9268b378e7602a0c1cffc19fb8f3ed4779921c01c6ec3)

[https://etherscan.io/tx/0xbea9754d2c190912570c5fd03647c5262955208382405f779bd07dbc6d191184](https://etherscan.io/tx/0xbea9754d2c190912570c5fd03647c5262955208382405f779bd07dbc6d191184)

[https://etherscan.io/tx/0x3d3299a63dc144cbf041fba2af5e520fa0f0730b3cd0fa7dac80bfaa0474454f](https://etherscan.io/tx/0x3d3299a63dc144cbf041fba2af5e520fa0f0730b3cd0fa7dac80bfaa0474454f)

[https://etherscan.io/tx/0x01e27250952e8c86ab6dba787f97ebaf313a82e6058fac8ef67e92d5adb464d1](https://etherscan.io/tx/0x01e27250952e8c86ab6dba787f97ebaf313a82e6058fac8ef67e92d5adb464d1)

</aside>

- average amount of gas required per transaction & state batch: 358,248
- gas price: 10~30 gwei (reflecting the recent downward trend in gas prices)
- **daily roll-up fees:** 358,248*(10~30 gwei)*24 = 86 ~258 million gwei = 0.086 ~ 0.258 ETH

- **Estimated MEV a sequencer earns**
    
    
    According to Flashbots, as of October 5th, KST, the extracted MEV during the last 30 days is about 795K USD. Therefore, we can infer that MEV worth approximately 27K USD gets materialized daily.
    
    However, it is more like the lower bound for the actual MEV due to the omission of certain types of transactions, including CEX-DEX arbitrages and sandwich transactions. Moreover, it is the extracted MEV on Ethereum, not layer 2 networks.
    
    Therefore, adapting the original data for our modeling is crucial.
    
    ![**Cumulative Extracted MEV split by the type of transactions (Source: Flashbots)**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-09-26_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_12.01.14.png)
    
    **Cumulative Extracted MEV split by the type of transactions (Source: Flashbots)**
    
    ![**DEX to CEX Spot Trade Volume(%) (Source: The Block)**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-09-26_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_12.07.36.png)
    
    **DEX to CEX Spot Trade Volume(%) (Source: The Block)**
    
    First, the extracted MEV in the Flashbots Dashboard mostly comes from arbitrages. Considering liquidations are generally not more profitable than arbitrages, it is safe to assume all the extracted MEV comes from arbitrages.
    
    Plus, arbitrages in the Flashbots data are through swap transactions in DEX. Since swap transactions are equivalent to spot transactions, we can complement the extracted MEV by reflecting the spot transactions in CEX:
    
    27K USD + 27K USD / 0.1134 = 265K USD
    
    ![**Ethereum TVL as of October 5th, KST (Source: DefiLlama)**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-10-05_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_3.03.27.png)
    
    **Ethereum TVL as of October 5th, KST (Source: DefiLlama)**
    
    ![**Uniswap TVL as of October 5th, KST (Source: DefiLlama)**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-10-05_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_3.05.28.png)
    
    **Uniswap TVL as of October 5th, KST (Source: DefiLlama)**
    
    ![**Cumulative Sandwich Profits in Uniswap(USD) (Source: Dune)**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-10-04_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_3.39.41.png)
    
    **Cumulative Sandwich Profits in Uniswap(USD) (Source: Dune)**
    
    Sandwich transactions cannot be ignored, too. Given the TVL difference, the cumulative sandwich profits in Ethereum are estimated as follows:
    
    310,000 USD * 31.9 / 5.03 = 1.97M USD
    
    Of course, since the number is in annualized terms, we can further update the extracted MEV as follows:
    
    265K USD + 1.97M USD / 365 days = 270.4K USD
    
    ![**Extracted MEV Split by Role (Source: Flashbots)**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-10-04_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_4.20.50.png)
    
    **Extracted MEV Split by Role (Source: Flashbots)**
    
    Unfortunately, MEV is not only for block producers or sequencers. Searchers can also capture MEV. If we only consider the share for miners or sequencers:
    
    270.4K USD * 0.357 = 97K USD
    
    ![**Ethereum TVL as of October 5th, KST (Source: DefiLlama)**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-10-05_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_3.03.27%201.png)
    
    **Ethereum TVL as of October 5th, KST (Source: DefiLlama)**
    
    ![**Layer 2 TVL (Source: L2Beat)**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-10-05_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_3.11.14.png)
    
    **Layer 2 TVL (Source: L2Beat)**
    
    Finally, we have to interpret this layer 1 number in the context of layer 2. Assuming MEV is generally proportional to the size of financial activities within networks, the following calculation holds:
    
    97K USD * (4.71/31.9) = 14K USD
    
- **Conclusion**
    
    
    ![스크린샷 2022-10-05 오전 3.53.21.png](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-10-05_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_3.53.21.png)
    
    Boba Network now expends daily roll-up fees worth 0.086 ~ 0.258 ETH or 115 ~ 346 USD.
    
    The current market share of Boba Network is 0.59%. The estimated MEV a sequencer earns in Boba Network every day is 0.59% * 14K USD = 82.6 USD.
    
    Therefore, Boba Network is expected to cover 24%~72% of layer 1 fees with MEV.
    
    Considering the thin user base of Boba Network, the result of modeling is aligned with our argument. For example, according to ETHTPS.info, its TPS is 0.03, much inferior to Ethereum.
    

### 3.2. TON seigniorage

The distribution of TON seigniorage will be proportional to 1) the amount of TON deposited in layer 2 ecosystems and 2) the amount of TON locked for layer 2 security.

The first standard encourages sequencers to attract more users, consolidating the ground for generating more MEV opportunities.

The second standard incentivizes sequencers to utilize MEV to pay layer 1 fees instead of swapping TON from transaction fees for ETH.

**3.2.1. Terminologies**

- **TON seigniorage**

Seigniorage is the difference between the value of a currency and the cost of issuing that currency. Since the issuance cost of TON is practically zero, TON seigniorage is just the market value of TON. Therefore, distributing TON seigniorage is the same as printing and giving out a new TON.

- **Deposit / lock or stake TON**

![스크린샷 2022-10-05 오후 2.27.05.png](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-10-05_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_2.27.05.png)

Depositing TON implies putting TON into layer 2 networks to make transactions. 

Deposited TON is open to various possibilities. For instance, users can hold deposited TON like cash for future transactions. They can also lock or stake TON for a specific purpose. Notably, locked or staked TON loses the liquidity to perform the predetermined function.

**3.2.2. TON seigniorage distribution based on the amount of TON deposited**

![**Example: TON seigniorage proportional to the amount of TON deposited**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-09-22_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_3.20.49.png)

**Example: TON seigniorage proportional to the amount of TON deposited**

As discussed in the previous sections, MEV mitigates the fee token dilemma by allowing extra income for sequencers to handle layer 1 costs. Of course, more MEV chances will arise only if more users join networks.

TON seigniorage based on the amount of TON deposited can facilitate such a process. Sequencers will strive to lure users because more users deposit more TON, leading to a higher portion of TON seigniorage for sequencers.

**3.2.3. TON seigniorage distribution based on the amount of TON locked**

![**Example: TON seigniorage proportional to the amount of TON locked**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-10-05_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_4.15.46.png)

**Example: TON seigniorage proportional to the amount of TON locked**

However, we have a problem. What if people sell deposited TON all at once within layer 2? It is technically possible because deposited TON is open to all transactions, including selling.

The issue is also crucial to our scheme. When sequencers take transaction fees in TON, they must decide whether to 1) use MEV profits or 2) swap TON for ETH to pay layer 1 fees. Of course, the former option contributes to tackling the fee token dilemma.

TON seigniorage distribution proportional to the amount of TON locked can guide sequencers as we want. TON from transaction fees will be locked for seigniorage. Of course, MEV revenue will cover layer 1 costs. If sequencers still stick to swapping TON for ETH, sacrificing the potential seigniorage revenue is inevitable.

**3.2.4. Game-theoretic interpretation**

We can illustrate how the behaviors of sequencers change with TON seigniorage distribution in a game-theoretic structure.

For this discussion, you first have to understand the payoff matrix. Payoff matrices show the benefits corresponding to specific actions by each entity. Notably, numbers in payoff matrices are in relative terms. For example, when the benefits of entity 1 and entity 2 are -2 and -1, respectively, absolute values of numbers do not matter. Instead, it just means that the loss of entity 1 is more than that of entity 2.

The payoff matrices below are not different. The first column and first row are the possible behaviors by sequencers 1 and 2, respectively. The payoff of two sequencers is denoted as (payoff of sequencer 1, payoff of sequencer 2).

![**Example: payoff matrix without TON seigniorage distribution**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-09-29_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_2.26.37.png)

**Example: payoff matrix without TON seigniorage distribution**

Without TON seigniorage distribution, the advantageous action for both sequencers is to swap TON for ETH, regardless of the decision by the counterpart. The reason is quite simple. You earn nothing for locking TON. Worse, if one sequencer locks TON and the other swaps TON for ETH, locked TON will suffer from declining prices due to selling pressures.

Therefore, both sequencers will sell TON from transaction fees to pay layer 1 fees and invest their assets, including MEV, in services offering higher returns.

![**Example: payoff matrix with TON seigniorage distribution**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-09-29_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%258C%25E1%2585%25A5%25E1%2586%25AB_2.26.51.png)

**Example: payoff matrix with TON seigniorage distribution**

However, the whole narrative takes a 180-degree turn with TON seigniorage distribution. If you swap TON for ETH, it is the same as giving up rewards for locking TON. In other words, it will increase both the benefits of locking TON and the opportunity costs of swapping TON for ETH if we provide sufficient compensation for locked TON.

Consequently, with TON seigniorage distribution, both sequencers lock TON from transaction fees and cover layer 1 fees with their money, including MEV.

### 3.3. Tokamak Network: Freedom to choose

It is finally time to incorporate all the ideas discussed into the concrete model. Within the Tokamak Network, each layer 2 protocol can establish tailored transaction fee policies. In this section, we will propose several possible combinations of institutions sequencers can introduce.

**3.3.1. Nascent protocols**

- **TON seigniorage distribution**
    
    
    ![**Example: zero transaction fees**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-09-29_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_4.14.49.png)
    
    **Example: zero transaction fees**
    
    While competing with other dominant incumbents, it will be hard to attract users as nascent followers. Thus, we can introduce zero transaction fees in the early phase of the protocol. One step further, each transaction may be rewarded with a certain amount of TON.
    
    As you can see, sequencers are likely to invest their money in the early stage of protocols. Therefore, the incentive mechanism is necessary to ensure that sequencers get credit for their performances. Here comes the TON seigniorage distribution proportional to the amount of TON deposited. As sequencers convince users of their merits, more TON will be deposited to make transactions, leading to more TON seigniorage for sequencers.
    
    The TON seigniorage distribution proportional to the amount of TON locked can also work in that way. If sequencers lock a large amount of TON for seigniorage, they have big stakes to lose for their malicious behaviors. Users will interpret it as a sincere commitment to layer 2 security.
    
- **MEV**
    
    
    Now that TON incentives laid the ground for MEV by bringing more people into platforms, we should delve into concrete ways to extract MEV.
    
    ![**Example: two-tier transaction fees**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-09-29_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_9.07.41.png)
    
    **Example: two-tier transaction fees**
    
    For instance, we can implement the ‘paid service’ in processing transactions. In this case, the default transaction fees are zero. However, ‘paid users’ choose to pay fees and earn some benefits. Such benefits can be either prioritizing their transactions or sharing the MEV of a sequencer in the future. If possible, even paid users may be divided into multiple tiers.
    
    Establishing exchanges is also on the table. Potential arbitrage opportunities will add to MEV. Additionally, sequencers can also expect commissions from trading activities.
    

**3.3.2. Mature protocols**

- **TON seigniorage distribution**
    
    
    ![**Example: TON as a fee token**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-09-29_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_10.03.50.png)
    
    **Example: TON as a fee token**
    
    TON seigniorage performs a similar role in mature protocols: encourage sequencers to maintain loyal users and capture new users.
    
    However, we must not miss one additional function: discourage sequencers from swapping TON for ETH. There is no way to force sequencers to use MEV to cover security fees. Despite making an adequate amount of MEV, they can still swap TON from transaction fees for ETH to pay layer 1 fees. TON seigniorage distribution based on the amount of TON locked raises the opportunity costs of such actions. If sequencers decide to sell TON from transaction fees, they give up potential benefits from TON seigniorage.
    
- **MEV**

Ideally, once they get mature, layer 2 services extract MEV enough to cover layer 1 fees. However, that might not be the case due to several factors, including the different layer 2 future landscape from our expectations.

We can come up with alternatives to counter the shortfall. For example, sequencers may borrow money from users. Some collaterals can be attached to the loan to ensure redemption.

Developing useful applications also helps sequencers alleviate the financial issue. P2P Lending/borrowing is the most common example. A lottery whose pool consists of users’ money is also possible. Commissions from these applications can contribute to making up for the insufficient MEV.

## 4. Implications

![스크린샷 2022-10-05 오후 5.13.27.png](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-10-05_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_5.13.27.png)

We can summarize the whole discussion with the diagram above.

### 4.1. Implications

- **Improved UX**
    
    
    Users can reduce their dependence on ETH to pay transaction fees because TON is also a fee token.
    
- **Centralized but censorship-resistant block production**

![**Centralized but censorship-resistant block production**](How%20to%20solve%20fee%20token%20dilemma%20in%20Tokamak%20Network%205920e0c4872a4666894c8f6f526653be/%25E1%2584%2589%25E1%2585%25B3%25E1%2584%258F%25E1%2585%25B3%25E1%2584%2585%25E1%2585%25B5%25E1%2586%25AB%25E1%2584%2589%25E1%2585%25A3%25E1%2586%25BA_2022-09-08_%25E1%2584%258B%25E1%2585%25A9%25E1%2584%2592%25E1%2585%25AE_7.37.38.png)

**Centralized but censorship-resistant block production**

One of the most serious shortcomings of centralized block production is that transactions can be censored arbitrarily. However, in the future anticipated by Tokamak Network, such malicious behaviors can be restricted due to the competition among layer 2 protocols. The competition arises out of the homogeneity they share. If a specific layer 2 platform tries to manipulate the block creation at the expense of users’ benefits, they will abandon the network and migrate to other competitors.

- **Curtailed negative externalities of MEV**

MEV has long been criticized for degrading UX. For this reason, leading layer 2 protocols have struggled to resolve the problem. For instance, Optimism aims at diverting MEV to common goods within the network through the MEV auction. On the other hand, Arbitrum tries to minimize MEV itself with decentralized sequencers. It has reportedly been exploring the Fair Sequencing Service by Chainlink.

Our approach is more like the one taken by Optimism. While admitting the presence of MEV, Tokamak Network plans to alleviate the negative externalities of MEV by making it contribute to the fee token utility of TON.

github repo (mark down)에 올리고 같은 내용을 미디엄에 올림

디렉토리를 분류하면 다국어 버전 가능

미디엄 머리 쪽에 깃헙 레포 달아서 최신 버전 확인하게끔!

Thanks to… 꼭 집어넣기

Tokamak network repo에 들어가있는지 학인?

수정 반영하고 아카이브 걸기 (수정 못하게끔)

깃헙계정 만들어서 아이디 알려주기