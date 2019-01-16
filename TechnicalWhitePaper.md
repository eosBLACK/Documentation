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
