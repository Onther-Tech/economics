# How to unravel fee token dilemma in layer 2

*Special thanks to Kevin.J, Darren.K, Nomad.I, Jake.J, Suah.K, Praveen.S, Jamie.J, and Theo.L for the productive feedback on the posting.*
<br/>
<br/>
## 0. Introduction
<br/>

Layer 2 is a collective term for a specific set of Ethereum scaling solutions without severely sacrificing security and decentralization. While layer 2 executes heavy computations off-chain, it relies on Ethereum for security and decentralization.
<br/>
<br/>

Tokamak Network has been striving to establish an on-demand layer 2 protocol. You can not only build your own layer 2 networks but freely communicate with other networks within Tokamak Network. Among various layer 2 technologies, optimistic roll-up, adopted by platforms like Optimism or Boba Network, will embody our mission. Being ‘optimistic’ implies that we assume the validity of transactions unless there is a challenge. If transactions get ‘rolled up,’ multiple transactions are collected into a batch and submitted to Ethereum at once. 

In the process, TON, the native token of Tokamak Network, must play a pivotal role in incentivizing users to act in an advantageous way for the protocol. In this context, diversifying the utilities of TON is crucial. Among possible utilities such as governance or staking, we will exclusively discuss the way to maximize the utility of TON as a fee token in this article.
<br/>
<br/>

## 1.  Trade-off around fee token utility
<br/>

### 1.1. Why TON to be a fee token?
<br/>

If TON is a fee token, users can pay transaction fees in TON.
<br/>
<br/>

Why is it so important?  First, fee token utility guarantees the baseline demand for TON.
No matter which applications or services people use on blockchains, making transactions is unavoidable. When you stake TON, it is a transaction. When you swap ETH for TON, it is a transaction as well. 

Adding TON to the list of fee tokens also improves UX by offering more options for users. They do not necessarily have to hold many ETH just for transaction fees. 
<br/>
<br/>

### 1.2. Fee token dilemma
<br/>

![fee token dilemma](https://github.com/Onther-Tech/economics/blob/main/fee_token_dilemma.png)
<br/>

Unfortunately, an extremely tricky issue has prevented many layer 2 protocols from allowing their tokens to be fee tokens: potential downward pressures on the token price from swapping TON for ETH to pay layer 1 fees.
<br/>
<br/>

The picture above shows how the ‘fee token dilemma’ arises. Layer 1 describes the underlying blockchain architecture responsible for the security and decentralization of layer 2 networks. In our discussion, Ethereum is layer 1. Sequencers are entities entitled to produce blocks in the layer 2 environment. 

Let’s look at the bright side first. When users make transactions, they purchase TON to pay transaction fees, boosting the price of TON.

However, you should also see the other side of the picture. Sequencers send the information on a bunch of layer 2 transactions to layer 1 for security. The problem is that the security or layer 1 fees incur, and sequencers must pay these fees in ETH. Consequently, despite taking transaction fees in TON, sequencers swap some TON for ETH to cover layer 1 costs. Of course, it would bring down the price of TON.
<br/>
<br/>

## 2. Similar protocols addressing fee token dilemma
<br/>

### 2.1. Optimism
<br/>

OP token, the native token of Optimism, is not for paying transaction fees within the network. Instead, it only performs governance functions.
<br/>

![Optimism Collective](https://github.com/Onther-Tech/economics/blob/main/optimism_collective.png)
<br/>

For example, Optimism Collective, together with Optimism Foundation, is responsible for governance in Optimism. In Token House, one of the two pillars supporting Optimism Collective, OP token holders can submit, deliberate, and vote on governance proposals, including protocol upgrades or inflation adjustments.
<br/>
<br/>

### 2.2. Boba Network
<br/>

Unlike Optimism, Boba Network has a dual-fee token system. Although ETH is a default fee token, users can also choose to pay transaction fees in the BOBA token. If BOBA is chosen as a fee token, users get a 25% discount.
<br/>
<br/>

However, Boba Network does not directly tackle the fee token dilemma. If necessary, BOBA gets swapped for ETH to cover layer 1 fees.

Instead, it tries to indirectly assuage the dilemma by combining governance with staking. If users want to participate in the decision-making process of Boba Network, they should stake BOBA. Additionally, a portion of transaction fees accrues to staked BOBA.

In other words, Boba network utilizes incentives so that more BOBA remains staked. Staked BOBA can partially offset selling pressures seen in the fee token dilemma.
<br/>
<br/>

## 3. Tokamak Network: proactive approach
<br/>

Tokamak Network wants TON to be a fee token. Plus, we directly deal with the fee token dilemma by using two tools at our disposal: MEV or Maximal Extractable Value and TON seigniorage distribution.
<br/>
<br/>

### 3.1. MEV(Maximal Extractable Value)
<br/>

MEV will remain intact in the long run. Instead of swapping TON from transaction fees for ETH, sequencers can utilize MEV profits to pay layer 1 fees.
<br/>
<br/>

#### 3.1.1. More inclusive definition of MEV
<br/>

- **Conventional definition of MEV**
    <br/>
    
    In technical terms, MEV refers to the maximum value extracted from block production in excess of the standard block reward and gas fees by including, excluding, and changing the order of transactions in a block.
    
    DEX arbitrage is one of the most well-known MEV examples. Let’s say two exchanges put a different price tag on the same token. Then, buying the token at a discount and immediately selling it at a premium generate profits. Of course, the selling transaction must be right after the buying transaction. If other transactions come in between these two transactions, arbitrage may not hold due to potential price volatility. In addition, the arbitrage transaction has to come before any other transaction involving the token. Otherwise, with the token price changed, the opportunity would be gone.
    
    Notably, MEV is not just for block producers. Searchers, a group of users specialized in spotting MEV opportunities with advanced algorithms or bots, can also benefit from MEV. In general, searchers should split the MEV benefits with block producers to include their transactions first in a block. For instance, in the case of arbitrage we just mentioned, even if a searcher finds the chance first, other searchers can snatch it by offering higher fees to block producers.
 <br/>

- **Redefinition of MEV**
  <br/>
  
    The definition of MEV above is primarily about taking profitable opportunities from a sea of transactions. However, we can also think about institutions to generate more value. More specifically, creating additional MEV is possible by designing policies that align the specific willingness to pay with corresponding needs.

    For example, if a sequencer gets compensated for putting transactions by a specific group of users first in a block, it can add to MEV, too. Users may also pay for inserting transactions at a particular time in a block. In other words, while users with a higher willingness to pay expend extra money for preferential treatment in processing transactions, users with a lower willingness to pay are content with basic services.

    Therefore, in this article, MEV refers to the maximum value, more than standard rewards, created by selling the rights to change the sequence of transactions in a block. It can be in the form of either fee competition or transaction policies. FYI, if block producers pursue MEV opportunities for themselves, it is the same as buying the rights for free.  
   <br/>
   <br/>
 
#### 3.1.2. MEV will not disappear
 <br/>
 
If MEV decreases significantly in the future, it cannot be a reliable source of income for sequencers to deal with layer 1 fees. In this sense, the sustainability of MEV is essential.

With the steadily increasing trend, MEV is unlikely to disappear thanks to centralized block production and complexity in Ethereum.
<br/>
<br/>

- **Present**
  <br/>
  <br/>
  
  ![cumulative extracted MEV](https://github.com/Onther-Tech/economics/blob/main/cumulative_mev.png)
  <br/>
  
  The graph above shows that the cumulative extracted MEV has increased significantly over the last two years. As of now, approximately 676 million USD   of MEV has been extracted.

  More importantly, this figure only considers the MEV from arbitrages and liquidations. Some lucrative MEV opportunities, including sandwich transactions, have been omitted. Plus, it has excluded CEX-DEX arbitrages in calculations due to the lack of information. On top of that, potential MEV chances generated by transaction policies, as we defined earlier, are off the table, too.

  Consequently, the actual MEV is likely to be much larger than the number measured by Flashbots.
  <br/>
  <br/>
  
- **Future**
  <br/>
  <br/>
  
  ![homogeneous](https://github.com/Onther-Tech/economics/blob/main/homogeneous_layer2.png)
  <br/>
  
  ![heterogeneous](https://github.com/Onther-Tech/economics/blob/main/heterogeneous_layer2.png)
  <br/>
  
  If the block production gets centralized, a small number of sequencers, if not only, handle transactions. Unlike decentralized sequencers, since there is less competition and uncertainties in becoming a block producer, it would be much easier to extract MEV.

  Then, how does block production get centralized? It is closely related to the future layer 2(roll-up) landscape proposed by Vitalik Buterin. The figure above illustrates the two possibilities discussed in his famous article ‘Endgame’: 1) a homogenous system where a small number of similar chains handle most of the Ethereum activities or 2) a heterogeneous system where multiple different chains cater to diverse needs. 

  Interestingly, both scenarios can lead to the same conclusion: centralized block production. In the case of a homogeneous world, the larger computational capacity for higher TPS would render the block production centralized. As for a heterogeneous ecosystem, potential cross-domain MEV may make centralized block production more likely.
  <br/>
  <br/>
  
  ![defi TVL](https://github.com/Onther-Tech/economics/blob/main/defi_tvl.png)
  <br/>
  <br/>
  
  The complicated nature of Ethereum can also feed MEV. For example, it is hard to reap profits from only sending or receiving tokens. However, it is a different story if you engage in diverse financial activities like trading spots or derivatives. Profitable MEV transactions such as arbitrages or liquidations will frequently pop up. Sequencers will benefit from either directly capitalizing on such opportunities or receiving higher gas fees from searchers.

  What demonstrates the complexity of Ethereum well is Defi. In the graph above, despite taking a hit from the recent crypto crash, Defi TVL has grown about 500% since September 2020. If you lengthen the time horizon a bit more, the current size of the Defi ecosystem is approximately 120 times larger than that in September 2019. As long as the crypto industry grows continuously in the long run, the Defi ecosystem will also expand, providing more MEV chances.
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

![heteregeneous homogeneous](https://github.com/Onther-Tech/economics/blob/main/tokamak_layer2_future.png)
<br/>

Tokamak Network expects a variety of layer 2 services to coexist, meeting diverse needs. While pursuing the same ideal of enhancing scalability, each layer 2 protocol will differentiate itself from others by specializing in certain areas. Some platforms may try to minimize slippage in swap transactions, whereas others can focus on offering a more comprehensive range of liquidity pools.
<br/>
<br/>

Consequently, layer 2 networks can exert monopoly power over users. Monopoly power exists because it will be hard to find the same functions targetting the specific necessity in many platforms. 

However, sequencers should not abuse monopoly power due to the competition based on scalability, the property all the layer 2 networks share. Suppose one protocol wields monopoly power to the point where its harms outweigh the benefits of customized functions. In that case, users will abandon the protocol and flock to competitors with comparable performances in scalability.
<br/>
<br/>

![userMEV](https://github.com/Onther-Tech/economics/blob/main/mev_users.png)
<br/>

The limited monopoly power affects the aggressiveness of sequencers in pursuing MEV chances.

Based on the figure above, at first, MEV is zero because there are no users. As the popularity of the layer 2 protocols grows, more people come to networks, which leads to more MEV opportunities. Interestingly, MEV increases very fast until it reaches roll-up fees. It is because sequencers can actively execute MEV transactions with monopoly power.

However, once MEV exceeds roll-up fees, the deceleration begins. Sequencers start to worry about whether MEV activity seriously erodes the common good. Crossing the ‘red line’ would mean users’ departure from protocols. The competition based on partial homogeneity works this time.
<br/>
<br/>

#### 3.1.4. Feasibility Test: numerical data
<br/>

We have reasoned that MEV will remain in place, and each layer 2 protocol will have a part of MEV. It is finally time to check whether the actual data on the following two items supports our argument: 1) layer 1 or roll-up fees and 2) estimated MEV a sequencer extracts.
<br/>

As for roll-up fees, we will refer to Boba Network for two reasons. First, Boba Network is an appropriate example of a relatively small protocol in a heterogeneous system. According to L2Beat, its current market share is approximately 0.59%. Plus, Boba Network is a good proxy for Tokamak Network. Both services utilize the optimistic roll-up technology. The size of networks, in terms of TVL, is quite similar, too.
<br/>

Regarding estimated MEV sequencer extracts, since the test is based on numerical data, we will consider only the quantifiable types of MEV.
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
 3. **daily roll-up fees:** 358,248*(10~30 gwei)*24 = 86 ~ 258 million gwei = **0.086 ~ 0.258 ETH**
<br/>

- **Estimated MEV a sequencer extracts**
    <br/>
    <br/>
    
    ![MEVeigenphi](https://github.com/Onther-Tech/economics/blob/main/mev_eigenphi.png)
    <br/>
    <br/>
    
    The numbers above show the size of MEV estimated by EigenPhi. Of course, it is for 30 days, so we have to modify it in daily terms:
    <br/>
    
    **(5.3M USD + 1.47M USD + 0.11M USD) / 30 = 230K USD**
    <br/>
    <br/>
    
    ![MEVsplitbyroles](https://github.com/Onther-Tech/economics/blob/main/mev_by_role.png)
    <br/>
    <br/>
    
    Unfortunately, MEV is not only for block producers or sequencers. Searchers can also capture MEV. If we only consider the share for sequencers:
    <br/>

    **230K USD * 0.357 = 82K USD**
    <br/>
    <br/>
    
    ![l2TVL](https://github.com/Onther-Tech/economics/blob/main/layer2_tvl.png)
    <br/>
    <br/>
    
    ![ethTVL](https://github.com/Onther-Tech/economics/blob/main/ethereum_tvl.png)
    <br/>
    <br/>
    
    Finally, we have to interpret this layer 1 number in the context of layer 2. Assuming MEV is generally proportional to the size of financial activities within networks, the following calculation holds:

    **82K USD * (4.71/31.9) = 12K USD**
    <br/>
    <br/>
    
- **Comparison**
    <br/>
    <br/>
    
    ![bobalocated](https://github.com/Onther-Tech/economics/blob/main/mev_users_boba.png)
    <br/>
    <br/>
    
    Boba Network now expends daily roll-up fees worth 0.086 ~ 0.258 ETH or 115 ~ 345 USD.
    
    The current market share of Boba Network is 0.59%. The estimated MEV a sequencer earns in Boba Network every day is 0.59% * 12K USD = 71 USD.
    
    Therefore, Boba Network is expected to cover 21%~62% of layer 1 fees with MEV.
    <br/>
    <br/>
    
    The result is consistent with our argument, given that Boba Network is an emergent platform with a growing user base. For example, according to ETHTPS.info, its TPS is 0.03, still not matching Ethereum.
    
    We also note that potential MEV opportunities created by transaction policies, as defined earlier, are not included in the data due to difficulties in obtaining credible data. Once they get attention, it will be much easier to cover layer 1 costs with MEV profits.
   <br/>
   <br/>
      
### 3.2. TON seigniorage
   <br/>
    
   The distribution of TON seigniorage will be proportional to 1) the amount of TON deposited in layer 2 ecosystems and 2) the amount of TON locked for layer 2 security.

   The first standard encourages sequencers to attract more users, consolidating the ground for generating more MEV opportunities.

   The second standard incentivizes sequencers to utilize MEV to pay layer 1 fees instead of swapping TON from transaction fees for ETH.
<br/>
<br/>

#### 3.2.1. Terminologies
<br/>

- **TON seigniorage**
    <br/>

    Seigniorage is the difference between the value of a currency and the cost of issuing that currency. Since the issuance cost of TON is practically zero, TON seigniorage is just the market value of TON. Therefore, distributing TON seigniorage is the same as printing and giving out a new TON.
<br/>

- **Deposit / lock / stake TON**
  <br/>
  
  ![depositvslock](https://github.com/Onther-Tech/economics/blob/main/deposit_lock_stake.png)
    <br/>

   Depositing TON implies putting TON into layer 2 networks to make transactions. 

   Deposited TON is open to various possibilities. For instance, users can hold deposited TON like cash for future transactions. They can also lock or stake TON for a specific purpose. Locked or staked TON loses the liquidity to perform the predetermined function. For example, TON locked for layer 2 security is only for maintaining the integrity of networks.
<br/>

#### 3.2.2. TON seigniorage distribution based on the amount of TON deposited
<br/>
<br/>

![depositedincentive](https://github.com/Onther-Tech/economics/blob/main/seigniorage_deposited.png)
<br/>
<br/>

As discussed in the previous sections, MEV mitigates the fee token dilemma by allowing extra income for sequencers to handle layer 1 costs. Of course, more MEV chances will arise only if more users join networks.

TON seigniorage based on the amount of TON deposited can facilitate such a process. Sequencers will strive to lure users because more users deposit more TON. Of course, it implies proportionately larger TON seigniorage for sequencers.
<br/>
<br/>

#### 3.2.3. TON seigniorage distribution based on the amount of TON locked
<br/>
<br/>

![lockedincentive](https://github.com/Onther-Tech/economics/blob/main/seigniorage_locked.png)
<br/>
<br/>

However, we have a problem. What if sequencers sell TON from transaction fees and seigniorage rewards to deal with layer 1 fees? It is at the discretion of sequencers to decide whether to 1) use MEV profits or 2) swap TON for ETH to pay layer 1 fees. Of course, the former option contributes to tackling the fee token dilemma. Unfortunately, we cannot force sequencers to choose a specific method.

TON seigniorage distribution proportional to the amount of TON locked can guide sequencers as we want. TON from transaction fees will be locked for seigniorage. Of course, MEV profits will cover layer 1 costs. If sequencers still stick to swapping TON for ETH, sacrificing the potential seigniorage revenue is inevitable.
<br/>
<br/>

#### 3.2.4. Game-theoretic interpretation
<br/>

We can illustrate how the behaviors of sequencers change with TON seigniorage distribution in a game-theoretic structure.
<br/>
<br/>

For this discussion, you first have to understand the payoff matrix. Payoff matrices show the benefits corresponding to specific actions by each entity. Notably, numbers in payoff matrices are in relative terms. For example, when the benefits of entity 1 and entity 2 are -2 and -1, respectively, absolute values of numbers do not matter. Instead, it just means that the loss of entity 1 is more than that of entity 2.

The payoff matrices below are not different. The first column and first row are the possible behaviors by sequencers 1 and 2, respectively. The payoff of two sequencers is denoted as (payoff of sequencer 1, payoff of sequencer 2).
<br/>
<br/>

![sellTONequil](https://github.com/Onther-Tech/economics/blob/main/payoff_default.png)
<br/>
<br/>

Without TON seigniorage distribution, the advantageous action for both sequencers is to swap TON for ETH, regardless of the decision by the counterpart. The reason is quite simple. You earn nothing for locking TON. Worse, if one sequencer locks TON and the other swaps TON for ETH, locked TON will suffer from declining prices due to selling pressures.

Therefore, both sequencers will sell TON from transaction fees to pay layer 1 fees and invest their assets, including MEV, in services offering higher returns.
<br/>
<br/>

![lockequil](https://github.com/Onther-Tech/economics/blob/main/payoff_seigniorage.png)
<br/>
<br/>

However, the whole narrative takes a 180-degree turn with TON seigniorage distribution. If you swap TON for ETH, it is the same as giving up rewards for locking TON. In other words, it will increase both the benefits of locking TON and the opportunity costs of swapping TON for ETH if we provide sufficient compensation for locked TON.

Consequently, with TON seigniorage distribution, both sequencers lock TON from transaction fees and cover layer 1 fees with their money, including MEV.
<br/>
<br/>

### 3.3. Tokamak Network: Freedom to choose
<br/>

It is finally time to incorporate all the ideas discussed into the concrete model. Within the Tokamak Network, each layer 2 protocol can establish tailored transaction fee policies. In this section, we will propose several possible combinations of institutions sequencers can introduce.
<br/>
<br/>

#### 3.3.1. Nascent protocols
<br/>

- **TON seigniorage distribution**
  <br/>
  <br/>
  
  ![nofees](https://github.com/Onther-Tech/economics/blob/main/zero_transaction_fees.png)
  <br/>
  <br/>
  
  While competing with other dominant incumbents, it will be hard to attract users as nascent followers. Thus, we can introduce zero transaction fees in the early phase of the protocol. One step further, each transaction may be rewarded with a certain amount of TON. In other words, sequencers are likely to invest their money in the early stage of protocols.
  <br/>
  <br/>
  
  Therefore, the incentive mechanism is necessary to ensure that sequencers get credit for their performances. Here comes the TON seigniorage distribution proportional to the amount of TON deposited. As sequencers convince users of their merits, more TON will be deposited to make transactions, leading to more TON seigniorage for sequencers.

  The TON seigniorage distribution proportional to the amount of TON locked can also work in that way. If sequencers lock a large amount of TON for seigniorage, they have big stakes to lose for their malicious behaviors. Users will interpret it as a sincere commitment to layer 2 security.
  <br/>
  <br/>
  
- **MEV**
    
  If TON incentives manage to bring more people into platforms, we should delve into concrete ways to extract MEV.
  <br/>
  <br/>
  
  ![paidservice](https://github.com/Onther-Tech/economics/blob/main/tiered_transaction_fees.png)
  <br/>
  <br/>
  
  For instance, we can implement the ‘paid service’ in processing transactions. In this case, the default transaction fees are zero. However, ‘paid users’ choose to pay fees and earn some benefits. Such benefits can be either prioritizing their transactions or sharing the MEV of a sequencer in the future. If possible, even paid users may be divided into multiple tiers.
    <br/>
    <br/>

  Establishing exchanges is also on the table. Potential arbitrage opportunities will add to MEV.
<br/>

#### 3.3.2. Mature protocols
<br/>

- **TON seigniorage distribution**
  <br/>
  
  ![noswap](https://github.com/Onther-Tech/economics/blob/main/ton_feetoken.png)
  <br/>
  <br/>
  
  Even with non-zero transaction fees, TON seigniorage performs similarly in mature protocols: encourage sequencers to maintain loyal users and capture new users.
  <br/>
  <br/>
  However, we must not miss one additional function: discourage sequencers from swapping TON for ETH. There is no way to force sequencers to use MEV to cover layer 1 fees. Despite making an adequate amount of MEV, they can still swap TON from transaction fees for ETH to pay layer 1 fees. TON seigniorage distribution based on the amount of TON locked raises the opportunity costs of such actions. If sequencers decide to sell TON from transaction fees, they give up potential benefits from TON seigniorage.
<br/>

- **MEV**
  <br/>
  
  Ideally, once they get mature, layer 2 services extract MEV enough to cover layer 1 fees. However, that might not be the case due to several factors, including the different layer 2 future landscape from our expectations.
  <br/>
  <br/>
  
  We can come up with alternatives to counter the shortfall. For example, sequencers may borrow money from users. Some collaterals can be attached to the loan to ensure redemption.

  Developing useful applications also helps sequencers alleviate the financial issue. P2P Lending/borrowing is the most common example. A lottery whose pool consists of users’ money is also possible. Commissions from these applications can contribute to making up for the insufficient MEV.
<br/>
<br/>

## 4. Implications
<br/>
<br/>

![structure](https://github.com/Onther-Tech/economics/blob/main/redefined_mev.png)
<br/>
<br/>

We can summarize the whole discussion with the diagram above.
<br/>
<br/>

In conclusion, implications of our model are as follows:
<br/>
<br/>

- **Improved UX**
  <br/>    
    
    Users can reduce their dependence on ETH to pay transaction fees because TON is also a fee token.
  <br/>
  <br/>
  
- **Centralized but censorship-resistant layer 2 block production**
  <br/>
  
  ![censorresistant](https://github.com/Onther-Tech/economics/blob/main/censorship_resistant.png)
  <br/>
  <br/>
  
  One of the most serious shortcomings of centralized block production is that transactions can be censored. However, in the future anticipated by Tokamak Network, such malicious behaviors can be restricted due to the competition among layer 2 protocols. The competition arises out of the homogeneity they share. If a specific layer 2 platform tries to manipulate the block creation at the expense of users’ benefits, they will abandon the network and migrate to other competitors.
  <br/>
  <br/>
  
- **Curtailed negative externalities of MEV**
  <br/>

  MEV has long been criticized for degrading UX. For this reason, leading layer 2 protocols have struggled to resolve the problem. For instance, Optimism aims at diverting MEV to common goods within the network through the MEV auction. On the other hand, Arbitrum tries to minimize MEV itself with decentralized sequencers. It has reportedly been exploring the Fair Sequencing Service by Chainlink.
   <br/>
   <br/>

  Our approach is more like the one taken by Optimism. While admitting the presence of MEV, Tokamak Network plans to alleviate the negative externalities of MEV by making it contribute to the fee token utility of TON.
  
  If MEV exceeds roll-up fees, the surplus can go to devoted users and developers, further diluting the side effects of MEV.
  
  It is also notable that we introduced a new type of MEV: value created by transaction policies. It is relatively resilient to the harms of MEV because every user can pay and earn benefits exactly as they want based on their willingness to pay.
<br/>
<br/>
  

## References
<br/>
<br/>

https://ethereum.org/en/developers/docs/mev/
</br>

https://vitalik.ca/general/2021/12/06/endgame.html
<br/>

https://research.paradigm.xyz/MEV
