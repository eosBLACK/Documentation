# eosBLACK Technical Whitepaper

## 01 Disclaimer

&nbsp;&nbsp;&nbsp;&nbsp;본 문서 및 기타 문서는 변경 또는 추가 정보에 대한 통지없이 언제든지 수정하거나 변경될 수 있습니다. 이 자료는 정보 제공만을 목적으로 하며 향후 그 내용이 변경될 수 있습니다.

본 백서는 현재 진행 중인 프로젝트에 대한 정보를 제공하기 위해 작성된 것이며, 향후에 비즈니스 활동에 대해서는 그 어떤 내용도 보장하지 않습니다. 이 백서에서 언급한 기술적 세부 사항과 구현 프로세스는 실제 비즈니스 환경에 따라 변경될 수 있으며 정확하지 않을 수 있습니다. eosBLACK 프로젝트와 관련된  진행 사항은 민감하지 않는 범위 내에서 단계별로 GitHub에 공유될 것입니다.

본 백서에 기술된 내용은 현재 개발중이며 지속적으로 업데이트 되고 있습니다.

eosBLACK이 완성될 경우, 본 백서에 명시된 네트워크와는 상당 수준 차이가 날 수 있습니다. EOSBLACK PTE. LTD.는 모든 계획, 향후 예상이나 전망과 관련해 어떠한 보증도 하지 않으며, 본 문서의 어떠한 내용도 미래에 대한 약속이나 표시로 간주되지 않습니다.
<br>
<br>

***

## 02 Account

&nbsp;&nbsp;&nbsp;&nbsp;EOS Mainnet과 달리 BLACK Mainnet은 네트워크 사용자에게 계정 생성 비용을 부과하지 않습니다. 사용자는 다양한 DApp을 통해 신규 계정을 생성할 수 있으며, 계정 생성에 필요한 자원은 시스템을 통해 한시적으로 사용자 계정에 위임됩니다.

BLACK 토큰을 보유한 EOS Mainnet의 계정은 BLACK Mainnet에 그대로 승계되며 계정 유지에 필요한 최소 자원은 해당 계정이 보유한 BLACK 토큰으로 충당합니다.

<pre>eosBLACK은 Mainnet 전환 시점의 EOS 스냅샷을 바탕으로 BLACK Mainnet에 접근할 수 있는 계정을 발급할 예정입니다.</pre>

### 2.1 Free Trials

#### 2.1.1 Lending Staked Tokens<sup id="a1">[1](#f1)</sup> with No fees

&nbsp;&nbsp;&nbsp;&nbsp;EOSIO 네트워크 계정 생성 비용은 사용자 확보 측면에서 DApp 개발의 진입 장벽으로 평가됩니다. 일례로 계정당 생성 비용이 2,000원<sup id="a2">[2](#f2)</sup>일 때 100만 계정 생성 시 20억 원의 비용이 소요됩니다. eosBLACK은 계정 생성에 필요한 자원 뿐만 아니라 3 Kbytes의 RAM을 무료로 제공함으로써 사용자 부담을 극소화시킵니다.

신규 계정 생성 시 위임된 CPU와 NET Bandwidth는 30일간 무료로 제공되며, 이후 철회(Refund) 과정을 거쳐 시스템으로 회수됩니다. 이렇게 회수된 자원은 다시 신규 계정 생성에 활용됩니다.

<pre>컴퓨팅 자원이 없을 경우 사용자는 그 어떤 트랜잭션도 실행할 수 없습니다.<br>그렇기 때문에 DApp 계정이 부모 계정(Parent Account)의 역할을 하게 되며 신규 계정 생성에 필요한 트랜잭션을 실행합니다.</pre>

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/account1.png" width=80% height=80% /></p>
<h5><p align="center">Figure 1. Leasing Bandwidth Resources for Creating Account</p></h5><br>

<br>신규 사용자에게 제공되는 컴퓨팅 자원은 다음과 같습니다. 플랫폼의 모든 기능이 구현되기 전까지는 eosBLACK 개발사에 의해 비즈니스 파라미터가 결정될 수 있습니다.

<h5><p align="center">Table 1. Resources for Free Account</p></h5>
<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/account2.png" width=70% height=70% /></p>
<h6><p align="center">* CPU와 NET Bandwidth 수량은 자원 사용 정도에 따라 변경될 수 있음.</p></h6>
<br>

#### 2.1.2 Refund Process

&nbsp;&nbsp;&nbsp;&nbsp;사용자는 가입일 기준 30일 동안 추가 자원 투입없이 계정을 유지할 수 있습니다. 만약 이 기간 동안 추가 스테이크를 하지 않으면 계정 사용이 중지됩니다.
<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/account3.png" width=80% height=80% /></p>
<h5><p align="center">Figure 2. Refund Process</p></h5>
<br>

#### 2.1.3 악의적 계정 생성에 대한 해결 방안

##### 2.1.3.1 By Invitation Only

&nbsp;&nbsp;&nbsp;&nbsp;경쟁 네트워크 혹은 해커에 의한 무한 계정 생성에 따른 시스템 마비 및 계정 점유 이슈를 예방하기 위해 기존 사용자가 신규 사용자를 초대하는 네트워크 가입 방식을 고려합니다. 건강한 네트워크는  무의미한 다수가 만드는 것이 아닙니다. 비록 소수일지라도 활성 사용자(Active User)가 증가하면 네트워크의 성장잠재력도 커집니다.


##### 2.1.3.2 Email Verification

&nbsp;&nbsp;&nbsp;&nbsp;Invitation Code에 따른 계정 생성 방법이 다소 사용자의 접근을 제한한다면 Email Verification은 무분별한 계정 생성을 막을 수 있으면서 누구나 네트워크에 접근할 수 있게 합니다. 계정 생성에 따른 경제적 이득이 없다는 전제 하에, 신규 계정 생성을 위해 매번 새로운 메일 계정을 등록해야 하기 때문에 자동 계정 생성 이슈를 방지할 수 있습니다.

### 2.2 Account Type

&nbsp;&nbsp;&nbsp;&nbsp;eosBLACK 계정은 스테이크 수량을 기준으로 크게 토큰 홀더(Token Holder)와 스테이크홀더(Stakeholder)로 나뉩니다.

<strong><pre><p align="center">Token Holder < Minimum Stake  ≤ Stakeholder</p></pre></strong>

스테이크홀더는 다시 참여자, 서포터, PO, 대표자로 구분됩니다. 참여자는 (대표자가 정한) 최소 토큰을 스테이크한 구성원으로 투표권과 투표보상의 권리를 갖습니다.

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/account4.png" width=80% height=80% /></p>
<h5><p align="center">Figure 3. User Classification</p></h5><br>
<br>

서포터, Project Owner<sup id="a3">[3](#f3)</sup>, 대표자 후보는 시스템 등록을 통해 해당 자격을 얻을 수 있습니다.  eosBLACK은 네트워크 구성원의 신뢰도를 높이기 위해 담보(collateral) 개념의 스테이킹 기간을 요구하며 권한이 늘어날수록 최소 스테이크 수량과 철회 기간(Refund Duration)<sup id="a4">[4](#f4)</sup>은 늘어납니다.


<h5><p align="center">Table 2. 계정 유형에 따른 최소 스테이크 수량 및 철회기간 예</p></h5>
<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/account5.png" width=70% height=70% /></p>
<h6><p align="center">* 최소 스테이크 수량 및 철회 기간은 대표자 합의에 의해 최적값으로 변경될 수 있음.</p></h6>
<h6><p align="center">* Lock-in Period 에 Vesting Option 구현</p></h6>

<br>

계정 유형에 따른 최소 스테이크 수량 및 철회 기간은 대표자(Active Representative) 합의를 통해 변경될 수 있습니다. 특정 대표자에 의해 새롭게 제안된 파라미터 값은 36시간 동안 대표자 투표를 받게 되며, ⅔+1 이상 동의를 얻으면 예고(豫告) 기간(Notice Period)을 거친 후 시스템에 반영됩니다.

만약 일부 대표자가 기한 내에 의결권을 행사하지 않아 의사결정에 필요한 의결정족수가 충족되지 않으면 차순위 예비 대표자(Inactive Representative)에게 의사결정권이 이양됩니다.

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/account6.png" width=80% height=70% /></p>
<h5><p align="center">Figure 4.  Representative's Proposal Approval Procedure</p></h5>

<br>

<pre>대표자가 의결권을 행사하지 않을 경우 패널티 점수가 올라가며, 동일한 이벤트가 3회 연속 발생할 경우 7일간 동안 블록 생산에서 제외됩니다.</pre>

<br>

><b id="f1"><sup>1</sup></b> 컴퓨팅 자원 할당을 위해 시스템에 잠긴 비용을 뜻함.[↩](#a1)<br>
<b id="f2"><sup>2</sup></b> eoshub 신규계정 생성 비용 https://eoshub.io/account/create?locale=ko [↩](#a2)<br>
<b id="f3"><sup>3</sup></b> Project Owner의 약자로 주로 분산형 애플리케이션 개발자를 지칭함.[↩](#a3)<br>
<b id="f4"><sup>4</sup></b> 철회 기간은 시스템에 락업된 자원을 철회할 때 계정으로 자원이 복구될 때까지 걸리는 시간을 뜻함.[↩](#a4)<br>

<br>

***

## 03 Resources

### 3.1 RAM 투기 제한 방안 : Limiting Active RAM Usage

&nbsp;&nbsp;&nbsp;&nbsp;eosBLACK 시스템은 RAM 무단점유(RAM Squatting)에 따른 비정상적인 RAM 가격 상승을 막기 위해 Active RAM<sup id="a5">[5](#f5)</sup>을 자동 회수합니다. 이때 RAM 철회 비용은 구매 시점의 가격을 기준으로 하며, 비정상적 RAM 구매에 따른 패널티 적용으로 1%의 거래 수수료가 부과됩니다. Active RAM의 회수량은 미사용 RAM 기준 90%이며, 트리거는 buyram/buyrambytes action과 그 액션으로 획득한 RAM의 50% 이하 사용률입니다.  

<p align="center"><img align="center" src="https://github.com/eosBLACK/Documentation/blob/master/images/resources1.PNG" width=80% height=70% /></p>
<h5><p align="center">Figure 5. Solving RAM Speculation in BLACK</p></h5><br>

EOS Mainnet은 RAM 가격 안정을 도모하기 위해 1 블록당 1KB의 RAM을 추가로 공급하겠다<sup id="a6">[6](#f6)</sup>고 밝힌 바 있지만 실제 네트워크 상의 RAM 수요와 상관 없이 일률적으로 RAM 자원을 늘린다는 점에서 비효율적 방안으로 보입니다.

<strong><pre><p align="center">[1 kbyte/block] x [2 block/sec] x [60 sec/min] x [60 min/hr] x [24hr/day] = 172,800 kbyte</p></pre></strong>

### 3.2 CPU 가격 안정: ① 스테이킹 사용 이원화

&nbsp;&nbsp;&nbsp;&nbsp;eosBLACK은 자원 활용의 효율성을 높이기 위해 CPU와 NET Bandwidth 자원 사용을 위한 스테이킹과 투표를 위한 스테이킹을 분리시키고자 합니다. 실제 상당량의 자원이 투표에 사용되지만 네트워크 자원으로는 활용되고 있지 않습니다. EOS Mainnet과 달리 eosBLACK은 투표에 따른 인센티브를 제공하기 때문에 자원 할당과 무관하게 투표에 자발적으로 참여하는 토큰 홀더들이 많을 것으로 봅니다. 

### 3.3 CPU 가격 안정: ② 커뮤니티를 통한 선별적 DApp 수용

&nbsp;&nbsp;&nbsp;&nbsp;pokereosgame-resolvebet, betdiceadmin-reveal2 등의 Contract으로 인한 Inline Action이 기하급수적으로 증가하면서 CPU 자원 가격과 가용성이 문제화되고 있습니다. Daniel Larimer는 애플리케이션 수준에서의 코드 최적화로 불필요한 CPU 소비를 줄일 수 있다고 미디엄을 통해 밝힌 바 있지만 개별 네트워크 참여자에게 코드 최적화를 강제할 만한 수단이 없기 때문에 사실상 문제 해결 방법으로 보이지 않습니다. 또한 DApp 홍보하기 위해 악의적으로 대량 트랜잭션을 발생시키는 자전거래의 정황이 포착되기도 했습니다. eosBLACK은 커뮤니티 구성원을 통해 체인 위에서 구동할 DApp을 선정하기 때문에 무의미한 트랜잭션을 유발하는 DApp을 원천적으로 차단할 수 있고, 이로 인한 CPU 가격 상승을 예방할 수 있습니다.

<br>

><b id="f5"><sup>5</sup></b> 미사용 RAM[↩](#a5)<br>
<b id="f6"><sup>6</sup></b> 무제한적 RAM 공급 모델[↩](#a6)<br>
