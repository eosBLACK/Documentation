# eosBLACK Technical Whitepaper

## 01 Disclaimer

&nbsp;&nbsp;&nbsp;&nbsp;This documentation and other documentations may be modified or changed due to additional information at any time without notice. The sole purpose of this material is to provide information, and its contents may be changed in the future.

This whitepaper was written to provide information on an ongoing project, and it does not assure any content about future business activities. The technical details and realization) process mentioned in this whitepaper may be changed according to actual business environment and may not be accurate. eosBLACK project progress details will be shared on GitHub at each phase to the extent where such information does not contain sensitive information.

The information described in this whitepaper is currently under development and is being continuously updated.

The complete version of eosBLACK may have significant differences with the network stipulated in this whitepaper. EOSBLACK PTE. LTD. does not make assurance about any plans or future forecasts/prospects, and no details in this documentation shall be deemed to be a promise or an indication about the future.
<br>
<br>

***

## 02 Account

&nbsp;&nbsp;&nbsp;&nbsp;Unlike EOS Mainnet, BLACK Mainnet does not impose account creation costs to the network user. Users can create new accounts using various DApps, and the resources required for creating an account shall temporarily be delegated to user account through the system.

EOS Mainnet accounts which possess BLACK tokens are succeeded as is to BLACK Mainnet, and the minimum resources required for maintaining the account shall be provided with BLACK tokens owned by the account.

<pre>eosBLACK plans to issue accounts that can access BLACK Mainnet based on an EOS snapshot at the point of converting to Mainnet.</pre>

### 2.1 Free Trials

#### 2.1.1 Lending Staked Tokens<sup id="a1">[1](#f1)</sup> with No fees

&nbsp;&nbsp;&nbsp;&nbsp;The cost for creating EOSIO network accounts is an entry barrier in developing DApps for securing users. For example, if the cost for creating an account is KRW 2,000<sup id="a2">[2](#f2)</sup>, a total of KRW 2 billion is required for creating a million accounts. eosBLACK minimizes user’s costs by providing the resources required for account creation, as well as 3Kbytes of RAM, free of charge.

The CPU and NET Bandwidth that have been delegated upon creating an account are provided free of charge for 30 days, and are retrieved to the system afterwards through the Refund process. The retrieved resources are again used for creating new accounts.

<pre>A user cannot execute any transaction if there is no computing power. Therefore, the DApp account serves as the Parent Account and runs transactions required for creating a new account.</pre>

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/account1.png" width=80% height=80% /></p>
<h5><p align="center">Figure 1. Leasing Bandwidth Resources for Creating Account</p></h5><br>

<br>The computing resources provided to new users are as follows:

<h5><p align="center">Table 1. Resources for Free Account</p></h5>
<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/account2.png" width=70% height=70% /></p>
<h6><p align="center">* CPU and NET Bandwidth quantity can be changed according to extent of the use of resources.</p></h6>
<br>

#### 2.1.2 Refund Process

&nbsp;&nbsp;&nbsp;&nbsp;Users can maintain their accounts without adding additional resources for 30 days from the date of joining. If no additional stake is made during this period, use of account will be discontinued.

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/account3.png" width=80% height=80% /></p>
<h5><p align="center">Figure 2. Refund Process</p></h5>
<br>

#### 2.1.3 Solutions for creation of malicious accounts

##### 2.1.3.1 By Invitation Only

&nbsp;&nbsp;&nbsp;&nbsp;In order to prevent system shutdown and account ownership issues followed by competitive network or creation of infinite number of accounts by hackers, we are considering a network membership method where existing users invite new users. A healthy network is not created by meaningless masses. Even if they are a minority, an increase in the number of Active Users can enhance the potential for growth of the network.


##### 2.1.3.2 Email Verification

&nbsp;&nbsp;&nbsp;&nbsp;Whereas the account creation method using an Invitation Code limits access by users to a certain extent, the Email Verification method allows anyone to access the network while preventing indiscriminate account creation. Provided that there is no economic benefit from account creation, a new email account must be registered every time in order to create a new account, preventing the issue of automatic account creation.

### 2.2 Account Type

&nbsp;&nbsp;&nbsp;&nbsp;Based on the stake quantity, eosBLACK accounts are largely divided into Token Holders and Stakeholders.

<strong><pre><p align="center">Token Holder < Minimum Stake  ≤ Stakeholder</p></pre></strong>

Stakeholder are then classified into Participants, Supporters, POs, and Representatives. A participant is a member who stakes the minimum tokens (determined by the Representative) and has the right to vote and right to receive rewards for voting.

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/account4.png" width=80% height=80% /></p>
<h5><p align="center">Figure 3. User Classification</p></h5><br>
<br>

Supporters, Project Owners<sup id="a3">[3](#f3)</sup>, and Representative Candidates can obtain their qualifications by registering in the system. To enhance the reliability of network members, eosBLACK requires staking period as collateral. As authority increases there are increases in the minimum stake quantity and Refund Duration<sup id="a4">[4](#f4)</sup>.

<h5><p align="center">Table 2. Examples of minimum stake quantity and Refund Duration according to account type</p></h5>
<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/account5.png" width=70% height=70% /></p>
<h6><p align="center">* Minimum stake quantity and Refund Duration may be changed to optimal values according to agreement by representatives.</p></h6>
<h6><p align="center">* Vesting Option realized during Lock-in Period</p></h6>

<br>

The minimum stake quantity and Refund Duration according to account type can be changed by agreement of Active Representatives. The parameter value that is newly proposed by a certain representative is open for voting by representatives for 36 hours. Agreement by ⅔+1 leads to a Notice Period, after which the change will be reflected in the system.

If some representatives do not exercise their voting right before the deadline, leading to a shortfall in the number of votes required for the decision, the rights for decision making will be transferred to the next Inactive Representatives in order.

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/account6.png" width=80% height=70% /></p>
<h5><p align="center">Figure 4.  Representative's Proposal Approval Procedure</p></h5>

<br>

<pre>If a representative does not exercise his/her voting right, their penalty score increases. If the same event occurs 3 consecutive times, he/she will be excluded from producing blocks for 7 days.</pre>

<br>

><b id="f1"><sup>1</sup></b> Staked token in the system for computing source lending. [↩](#a1)<br>
<b id="f2"><sup>2</sup></b> Cost for new account creation in eoshub https://eoshub.io/account/create?locale=ko [↩](#a2)<br>
<b id="f3"><sup>3</sup></b> Abbreviation for a Project Owner, a DApp developer. [↩](#a3)<br>
<b id="f4"><sup>4</sup></b> Refund duration refers to the necessary time needed for the resources staked at the system return to the account. [↩](#a4)<br>

<br>

***

## 03 Resources

### 3.1 Plan for restricting RAM speculation: Limiting Active RAM Usage

&nbsp;&nbsp;&nbsp;&nbsp;The eosBLACK system automatically retrieves Active RAM<sup id="a5">[5](#f5)</sup> in order to prevent irregular increases in RAM price following RAM Squatting. At this time, the RAM refund cost is based on the price at the point of purchase, and a 1% transaction fee will be imposed as a penalty for irregular RAM purchase. The retrieval rate of Active RAM is 90% of the unused RAM, and the trigger is buyram/buyrambytes action and the usage rate below 50% of RAM acquired by such action.

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/resources1.PNG" width=80% height=70% /></p>
<h5><p align="center">Figure 5. Solving RAM Speculation in BLACK</p></h5><br>

While EOS Mainnet announced that it will supply 1KB of additional RAM per block to stabilize RAM price<sup id="a6">[6](#f6)</sup>, this appears to be an inefficient plan in that it increase RAM resources in a uniform manner regardless of RAM demand in the actual network.

<strong><pre><p align="center">[1 kbyte/block] x [2 block/sec] x [60 sec/min] x [60 min/hr] x [24hr/day] = 172,800 kbyte</p></pre></strong>

### 3.2 CPU price stabilization: ① Dualize the use of staking

&nbsp;&nbsp;&nbsp;&nbsp;To enhance the efficiency of resource utilization, eosBLACK plans to separate staking for using CPU and Net Bandwidth resource and staking for voting. In fact, a significant amount of resources is used for voting, but they are not being used as network resources. Since eosBLACK provides incentives for voting unlike EOS Mainnet, it seems likely that there will be more token holders who voluntarily participate in voting regardless of resource allocation.

### 3.3 CPU price stabilization: ② Selective DApp acceptance via community

&nbsp;&nbsp;&nbsp;&nbsp;The price and availability of CPU resources are becoming problematic along with exponential an increase in Inline Action from Contracts such as pokereosgame-resolvebet and betdiceadmin-reveal2<sup id="a7">[7](#f7)</sup>. While Daniel Larimer said in Medium that unnecessary CPU consumption can be reduced through code optimization on the Application level, this does not seem to be a good solution because there is no good means to force code optimization on individual network participants. Also, circumstances of cross-trading producing malicious large-scale transactions were identified for the purpose of DApp promotion. As eosBLACK selects the DApps to be operated on the chain through its community members, it can fundamentally block DApps that produces meaningless transactions, which leads to the prevention of consequent increases in CPU price.

<br>

><b id="f5"><sup>5</sup></b> Unused RAM [↩](#a5)<br>
<b id="f6"><sup>6</sup></b> Unlimited RAM Supply Model [↩](#a6)<br>
<b id="f7"><sup>7</sup></b> Action Summary http://eos.dapptools.info/#/actions-summary-24-hours [↩](#a7)<br>

<br>
<br>

***

## 04 Voting

### 4.1 Representative Voting: Stake-Weighted Approval Votes
&nbsp;&nbsp;&nbsp;&nbsp;Stakeholders can exercise Voting Power<sup id="a8">[8](#f8)</sup> in proportion to the quantity of BLACK that they possess. Just like in EOS Mainnet, they can vote at most 30 times per account, and Refund is available as well. While the voting power in BLACK Mainnet is largely similar to that of EOS Mainnet, the principle of equal allocation of voting power according to the number of accounts that exercise voting power and Contribute Time<sup id="a9">[9](#f9)</sup> will apply.

#### 4.1.1 Calculation of Voting Power
##### 4.1.1.1 Contribute Time
&nbsp;&nbsp;&nbsp;&nbsp;To reflect network loyalty into voting power, eosBLACK reflects Contribute Time as follows when calculating voting power.

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/voting1.PNG" width=80% height=80% /></p>
<br>

Voting power increases by 10%<sup id="a10">[10](#f10)</sup> every day, based on stake that has not been converted into voting power. For example, an account which staked 1,000 BLACK for 20 days has about twice the voting power that an account which staked 5,000 BLACK for a day does.

<br>

<h5><p align="center">Table 3. Comparison of Voting Power for a particular day according to stake quantity and period</p></h5>
<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/voting2.PNG" width=70% height=70% /></p>

<br>

Voting power calculated in ‘Day’ units is aggregated as time goes by. Its details are as follows.

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/voting3.PNG" width=80% height=80% /></p>
<h5><p align="center">Figure 6. Voting Power(10% Upgraded from Staked Tokens per Day)</p></h5><br>

##### 4.1.1.2 Equal allocation of voting power according to the number of accounts that exercise voting power

&nbsp;&nbsp;&nbsp;&nbsp;In order to enhance network integrity and reduce the possibility of collusion, which may occur by accounts with a high number of BLACK advocating a few Representatives, eosBLACK applies equal allocation of voting power according to the number of accounts that participate in voting when calculating voting power. This is calculated as follows.

<br>

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/voting4.PNG" width=80% height=80% /></p>

<br>

### 4.2 Voting for Project Selection (Voting Projects of This Phase)
&nbsp;&nbsp;&nbsp;&nbsp;Based on its budget collected through base funds and inflation, etc., eosBLACK supports projects for developing promising DApps (that will lead the eosBLACK ecosystem). We use the following methods in order to reflect the opinions of more members and to prevent specific projects from receiving preferential treatment.

#### 4.2.1 Voting for projects: Proof of Mixed
&nbsp;&nbsp;&nbsp;&nbsp;eosBLACK uses mixed proof in the process of selecting projects in order to eliminate practical limitations of DPoS –collusion or illegitimate collective actions by a few, etc. Mixed proof here means that PoA (Proof of Approval) and PoS (Proof of Stake) are applied sequentially in the decision-making process.

Projects that are registered in the Proposal Pool are sent to Representative Voting after receiving Stakeholder Approval for a certain period. Project listed at this point are selected within the scope of the available budget based on the approval results of Public Voting.  

Representatives must participate in the voting for selecting projects within a designated period. If a quorum for resolution is not met within the deadline, the right to vote shall be given to the next Inactive Representative(s) in order.

Voting becomes effective with approval by ⅔+1 (⅔ Supermajority). Selected projects receive human/physical support according to each roadmap.

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/voting5.PNG" width=80% height=80% /></p>
<h5><p align="center">Figure 7. Project Voting</p></h5><br>

#### 4.2.2 Score(aka Range) Voting
&nbsp;&nbsp;&nbsp;&nbsp;To not stop at a simple Approval, although it is a part of Approval voting, the ranking of projects is determined by giving scores to each project to further specify members’ Measure of Value. The Scores that are aggregated during the presentation period can affect the order of project exposure. Once the presentation period ends, projects are selected based on PoA, and if there is a tie, the scores will be taken into consideration. These scores may be used as indicators for the decision-making process during Representative voting. If two projects have the same number of Approval votes and same scores, the project with a lower budget will be selected, from the perspective of cost-to-performance ratio.

<h5><p align="center">Table 4. Aka Range Voting</p></h5>
<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/voting6.PNG" width=70% height=70% /></p>

<br>

><b id="f8"><sup>8</sup></b> Voting Power is directly proportionate to the amount of staked token the account has. [↩](#a8)<br>
<b id="f9"><sup>9</sup></b> The total duration of maintaining the account. Considered as ‘User’s Loyalty’. [↩](#a9)<br>
<b id="f10"><sup>10</sup></b> 10% of the figure can change according to the consensus of the Representatives. [↩](#a10)<br>

<br>
<br>

***

## 05 Entities
### 5.1 Representatives

&nbsp;&nbsp;&nbsp;&nbsp;The representatives who are the top 21 winners of the public voting (Stake-Weighted Approval Votes) produce a new block every round using a ⅔ +1 consensus algorithm. The representatives hold the right to modify all network parameters.

The representatives consist of 21 active representatives (Producing Nodes) and 30 pre-representatives (non-producing nodes). To compensate for design defects in the EOS network, where only 21 nodes are used for block validation, the representatives can increase the number of representative nodes (Master Node, Producing Node) up to 51 through an agreement.

Representatives participating in the block production are selected through a round-robin-schedule<sup id="a11">[11](#f11)</sup> for each round.

In order to become a candidate representative, BLACK must be staked by a specified amount. The BLACK locked up in the voting system in this process is tied to the system for a certain period of time and refunded upon withdrawal request.

#### 5.1.1 DPoS(Delegated Proof-of-Stake) + BFT(Byzantine Fault Tolerance)

&nbsp;&nbsp;&nbsp;&nbsp;The Proof of Work (POW) and Proof of Stake (POS) consensus mechanisms are inept for quickly handling high-level transaction demands. The DPOS+BFT aggregation mechanism has already been proven by Steem and Bitshares as a solution that satisfies both user experience and distributed systems. Using this mechanism, thousands of transactions can be processed per second without the need of a side chain or sharding mechanism.

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/entities1.PNG" width=80% height=80% /></p>
<h5><p align="center">Figure 8. Block Producer</p></h5><br>

#### 5.1.2 Hardware Requirements

-  Minimum 8 core CPU
-  At least 32 GB of RAM
-  Static IP with a 100Mbps internet connection speed
-  SSD Storage

#### 5.1.3 Disqualification

&nbsp;&nbsp;&nbsp;&nbsp;A representative may lose his/her qualifications in any of the following ways:

-  Withdrawal of participant support: participants can withdraw their votes and vote for other candidates or representatives.
-  Representative dismissal agreed on through a vote: when it is determined that a representative has caused serious damage to the maintenance of the ecosystem, the representatives may vote to remove the representative. When the number consenting to the dismissal of the representative by the representatives, including pre-representatives but excluding the representative subjected to the vote, is not less than ⅔+1 of the voters.
- Minimum staking quantity condition not met: the representatives must maintain at least <sup id="a12">[12](#f12)</sup> stakes during the term. The representative status shall be lost when the staking amount falls below the minimum.

### 5.2 Supporters (Co-workers)
#### 5.2.1 Eligibility

&nbsp;&nbsp;&nbsp;&nbsp;Any BLACK token holder can acquire supporter status through staking and registration.

Once the supporter registration is completed, the supporter is automatically registered in the Supporter's Pool.

Supporters can participate in, and receive rewards for, the DApp projects developed in the Crypto Factory. This is similar to the Work Proposal on EOS Mainnet. Supporters can earn higher rewards through continuous project participation and reputation management. The Supporters’ participation is managed and rewarded through smart contracts.

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/entities2.PNG" width=80% height=80% /></p>
<h5><p align="center">Figure 9. Supporter’s Role</p></h5><br>

The token holders must register the following when registering as supporters.

<br>

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/entities3_en.PNG" width=80% height=80% /></p>

<br>

### 5.3 Advisory Board
#### 5.3.1 Composition of the Advisory Board

&nbsp;&nbsp;&nbsp;&nbsp;Members of the advisory board are elected through public voting and are guaranteed a one-year term to ensure the continuity of their work, except in the case of a serious moral hazard.

- Members can be reappointed
- A certain amount of BLACK may be charged for candidacy

If a member of advisory board fails to fulfill the principles of good faith during their term in office and becomes disqualified by representative voting, a new advisory board candidate will be appointed based on the advisory board voting approval rate for the year. If the candidate accepts the advisory board proposal, he/she will act as a member of the advisory board for the remainder of the term.

Unlike representative voting, where it is appropriated each round, a vote cannot be withdrawn once the year’s voting period ends.

<pre>The amount rewarded for advisory board activities, which is a type of supporter reward, is determined by the Representatives.</pre>

#### 5.3.2 Key roles of the Advisory Board

- Project budget decision-making
- Project proposal review
- Business parameter proposal

<br>

><b id="f11"><sup>11</sup></b> A way in which all the steps proceed in sequence and the first step gets the opportunity again at the end of the last sequence. [↩](#a11)<br>
<b id="f12"><sup>12</sup></b> The minimum quantity can be changed upon agreement of the representatives but shall be based on "Table 2. Minimum number of stakes and withdrawal period according to account type". [↩](#a12)<br>

<br>
<br>

***
## 06 Incentives

&nbsp;&nbsp;&nbsp;&nbsp;eosBLACK supports new ideas and projects to expand the value and utilization of the ecosystem and provides incentives for members of the ecosystem to participate directly in the process of innovation. The incentives can be categorized into:

-  rewards for block production required for network node maintenance; 
-  rewards for supporter activity required for network growth; and 
-  rewards for voting activities that can enhance the value of decentralization

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/incentives1.PNG" width=80% height=80% /></p>
<h5><p align="center">Figure 10. Incentives</p></h5><br>

### 6.1 Block Producer Rewards
#### 6.1.1 Weighted Round Robin (WRR) Discipline

&nbsp;&nbsp;&nbsp;&nbsp;Round-robin load balancing is a method of "sequentially" allocating client requests across the server group, whereas Weighted Round Robin load balancing is a method of assigning client requests to each representative node based on specific criteria (weight).

By using the "weight” attribute, the block production request is allocated to the node in proportion to the weight, and the rewards for block production between representatives are adjusted so that the representatives can maintain and manage the nodes more responsibly.

For example, if a cluster has two nodes and the administrator has assigned a weight of 100 to node A and a weight of 400 to node B, 20 out of 100 requests are sent to node A and 80 to node B. The Weighted Round Robin (WRR) approach is applied to the nodes that have received a penalty as a mechanism to preempt problems.

### 6.2 Supporter Ranking Rewards

&nbsp;&nbsp;&nbsp;&nbsp;eosBLACK uses the following criteria to provide incentives for supporters that drive the growth of the community.

#### 6.2.1 Activity Rewards

&nbsp;&nbsp;&nbsp;&nbsp;Supporters are scored based on new followers, post recommendations, etc. This score (50%) is added to the approval rating on the supporter ranking system (50%) and the resulting score becomes the basis for incentive allocation. Rewards are calculated on a weekly basis and payment criteria are also adjusted on a weekly basis. Rewards are paid upon claim.


<br>

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/incentives2_en.PNG" width=80% height=80% /></p>

<br>

#### 6.2.2 Approval Rating Rewards

&nbsp;&nbsp;&nbsp;&nbsp;The supporter ranking reward is calculated based on the votes proportion, and the formula is as follows:

<strong><pre><p align="center">Supporter Rewards = Total Weekly Reward x (last_supporter_vote_weight / Total last_vote_weight)</p></pre></strong>

Values below the 1% Qualifying Threshold are not subject to the reward. The vote calculation follows the same method of representative voting. Each account can vote for up to 10 accounts.

### 6.3 Contribution-Based Airdrop: Voting Rewards

<strong><pre><p align="center">Voting Rewards = Total Air Drop Quantity x (last_vote_weight ÷ Total last_vote_weight)</p></pre></strong>

&nbsp;&nbsp;&nbsp;&nbsp;The votes subject to voting rewards are representative voting and project voting. To receive an airdrop, one must participate in both types of voting.

POs must be airdrop according to the project token allocation plan. 80% of the amount will be paid to all voters and the remaining 20% will be paid to the members who voted for the project, based on their shares.

<br>

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/incentives3.PNG" width=80% height=80% /></p>
<h5><p align="center">Figure 11. Voting Rewards</p></h5><br>

<br>

#### 6.3.1 DApp Token Payment Method: Skyhook

&nbsp;&nbsp;&nbsp;&nbsp;The tokens issued by the Crypto Factory are paid via the Skyhook method. Unless there is a claim from the receiver within the due date, the tokens paid will be returned in full, unlike in the case of Airgrab. In addition, Receivers must provide a small amount of RAM resources (approximately 240 bytes) to store new token information.

<br>

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/incentives4.PNG" width=80% height=80% /></p>
<h5><p align="center">Figure 12. Airdrop: Skyhook</p></h5><br>

<br>
<br>

***

## 07 Project

&nbsp;&nbsp;&nbsp;&nbsp;eosBLACK's project is a community-driven project because the value created by eosBLACK is incorporated into the project through the members of the community. Proposals submitted to eosBLACK are expressed as projects through “on-chain governance”. As the project support budget is set for each Phase, the PO must improve the completeness of the proposal content and examine the Business Model (BM) closely to gain greater support from the members.

&nbsp;&nbsp;&nbsp;&nbsp;In order to prevent excessive project registration, the PO must pay a certain fee when registering the project.

<br>
<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/project1_en.PNG" width=80% height=80% /></p>
<br>

### 7.1 Proposal Presentation

&nbsp;&nbsp;&nbsp;&nbsp;The voting process by the members for a project owner’s proposal is as follows:

<br>
<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/project2.PNG" width=80% height=80% /></p>
<h5><p align="center">Figure 13. Proposal Presentation</p></h5><br>
<br>

&nbsp;&nbsp;&nbsp;&nbsp;When a project owner submits a proposal, the information is encrypted and stored in a block chain. The proposal goes through a presentation period instead of being reviewed and censored by a centralized organization. This is the period in which the proposal is presented to a large number of members before the referendum.

&nbsp;&nbsp;&nbsp;&nbsp;The referendum period is one week long and the proposal can be updated until the referendum commences. At the end of the voting period, part of the proposal will be presented to representative voting.

In the case of a referendum, more than 15% of all members must participate in the vote for a proposal to be selected, and a proposal with the highest score (on a 5 point-scale) will be selected within the budget. Once the proposal is approved in representative voting, the development work can commence according to the road map. The project owner(PO) must provide the output in accordance with the road map, within the deadline, and may change the budget on a sub-project basis. Agreements related to budget execution are made by the representative group.

<br>
<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/project3.PNG" width=80% height=80% /></p>
<h5><p align="center">Figure 14. Examples of Proposal Presentation</p></h5><br>
<br>

&nbsp;&nbsp;&nbsp;&nbsp;The number of up/down votes may be displayed on the UI to sort the data, but they do not affect the voting results.

&nbsp;&nbsp;&nbsp;&nbsp;Even if a proposal is rejected because of low votes, it can still compete in a later phase upon PO’s decision.

### 7.1.1 Voting Status Disclosure Method

&nbsp;&nbsp;&nbsp;&nbsp;If the voting status is released before the ballot is over, it may boost the concentration of votes on proposals which already have a high vote count. This is similar to the “Keynesian beauty contest” in which many invest based on the projection of majority vote. The PLCR (Partial Lock Commit / Reveal) voting method<sup id="a13">[13](#f13)</sup> prevents an unspecified number of votes from being cast in a meaningless direction by preventing the votes from being disclosed to the chain during the ballot period.

## 7.2 Proposal Presentation Ordering

&nbsp;&nbsp;&nbsp;&nbsp;As previously noted, the scores obtained through score voting can affect the order of project exposure. The order of project display is a factor that greatly influences the outcome of the approval rating of proposals. As such, the display shall be determined based on an algorithm, and not through human curation.

## 7.3 Project classification by size

&nbsp;&nbsp;&nbsp;&nbsp;Projects are categorized according to the following budget criteria:

<br>
<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/project4.PNG" width=80% height=80% /></p>
<br>

## 7.4 Types of rewards as the project progresses

&nbsp;&nbsp;&nbsp;&nbsp;Project support rewards for network members are determined based on the following criteria:

<br>
<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/project5_en.PNG" width=80% height=80% /></p>
<br>

## 7.5 Intellectual Property Protection: Code Privacy

&nbsp;&nbsp;&nbsp;&nbsp;Project Owners can hold intellectual property rights of smart contracts deployed in the network.


## 7.6 Application Requirement of eosBLACK: Mature & Budding

Project Owners must register sufficient development and funding plans at the time of project registration and after project selection, periodically updating the project progress to inform participants.

-	The submitted documents must be complete and accurate.
-	It must follow professional and compliance requirements without any policy risk
-	The project must be capable of actual technical support and aim at practical applications. 
-	The project must have a team that works organically and manages/maintains the community. 
-	eosBLACK Advisory Board's asset evaluation criteria must be met
-	Must provide project information, including white papers, periodic development, and progress reports, in an accurate and timely manner.
-	Other explicit requirements for Crypto Factory project listings
-	Recommended by professional investment institutes.<br>
  Must provide at least 10% of total tokens or at least 20% of tokens in circulation.*

<br>

<b id="f13"><sup>13</sup></b> Partial-Lock Commit-Reveal Voting  https://github.com/ConsenSys/PLCRVoting [↩](#a13)<br>
