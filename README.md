# Rebellion Data Funder 简介

Rebellion Data Funder 致力于构建一个全球性的数据众筹平台，赋予用户对个人数据的完全控制权，并通过去中心化的经济激励机制获得实际回报。用户可以透明、安全地共享数据，并通过 RBL token 实现直接经济收益，从而推动数据经济的公平发展和隐私保护。

Rebellion Data Funder 由一个隐私保护的数据共享平台（Data Network）和一个去中心化的经济激励机制（RLB token）组成。每个用户通过分享数据，验证后即可获得 RLB  token 的经济收益。该平台采用先进的加密技术和区块链基础设施支持，在保护隐私的同时将人类与人工智能区分开来，确保数据的有效性和隐私性。

**“数据隐私保护”** 是 Rebellion Data Funder 的核心理念，旨在确保用户数据的隐私和控制权。平台通过加密技术验证数据的真实性，并通过去中心化的机制确保数据使用的透明性，使用户能够在不泄露现实世界身份的情况下安全地分享数据。

目前，数据隐私保护在全球范围内仍是一个亟待解决的问题，尤其是在隐私法规日益严格的背景下。随着数据共享和经济激励机制的不断发展，Rebellion Data Funder 可能成为全球数据隐私保护和经济回报的标准。

Rebellion Data Funder 的核心假设包括：

- **数据隐私保护的必要性**：数据隐私保护是当前数字时代的核心需求。随着对数据安全的关注加剧，这一需求将变得更加重要。
- **可扩展的经济激励**：RBL token 是 Rebellion Data Funder 的经济激励核心，用于对所有参与者进行激励，以确保平台的长期发展和激励用户参与数据共享，并保障数据的有效性和透明度。
- **技术创新**：Rebellion Data Funder 基于先进的加密技术构建了一个隐私保护的数据网络。用户通过平台控制个人数据的共享，并确保数据在传输和存储过程中得到最高级别的保护。加密技术的应用确保了数据的真实性和隐私，防止了数据的滥用和泄露。

未来，Rebellion Data Funder 将继续推动数据隐私保护的技术进步，扩大用户基础，并为数据经济提供创新的激励机制和应用场景。以下是项目书分享了该项目实施背后的原因以及当前状态和路线图。

![Framework](https://github.com/ContributeDAO/.github/blob/main/profile/Framework.png)


# 参与方

- 数据上传者：浏览需求并自愿选择参与数据共享；
- 验证者：验证上传者的数据是否符合购买方的要求；
- 购买方：发布数据需求悬赏；
- Rebellion App：前端应用，管理用户的 **Rebellion ID** 认证信息。

# Rebellion ID

**Rebellion ID 是用户的人格证明，**确保每个用户的数据在共享过程中的安全性，并且使得盗用或滥用数据变得极其困难**。**用户需要在注册时通过绑定验证他们的指纹信息来生成 **Rebellion ID**，确保身份的真实性和唯一性。这一机制允许个人向验证者证明其为真实用户，防止机器人和虚假账户污染数据共享环境。

<p align="center">
  <img src="https://github.com/ContributeDAO/.github/blob/main/profile/RebellionID.png" alt="RebellionID" width="900" />
</p>

# Rebellion App

**Rebellion App** 是 **Rebellion Data Funder** 的首个前端应用：它引导用户通过数据共享和验证流程，管理用户的 **Rebellion ID** 认证信息，并实现加密协议，以隐私保护的方式与第三方共享数据。**Rebellion App** 旨在提供无缝的全球去中心化数据共享体验，使用户能够方便地响应数据需求悬赏，并通过分享个人数据获得收益。

通过 **Rebellion App**，项目方可以发布数据需求悬赏，用户可以浏览这些需求并自愿选择参与数据共享。用户共享的数据将受到严格保护，同时确保隐私不被泄露。最终，**Rebellion App** 期望支持各种数据需求的发布和响应，并提供对全球去中心化金融基础设施的无摩擦访问，为用户和项目方提供广泛的数据共享和收益机会。

<p align="center">
  <img src="https://github.com/ContributeDAO/.github/blob/main/profile/UI.png" alt="UI" width="300" />
</p>


# 数据上传

### 数据上传者

用户可以通过授权读取或自行上传个人数据。当用户上传数据后，他们将获得该数据集（悬赏任务）的验证者身份，数据被传入脱敏模块（详见脱敏模块）。上传者可以设置数据与验证者的分润比例和衰减函数（详见数据验证者部分），以吸引验证者优先验证其数据。当上传的数据达到一定规模时，将触发验证流程。

### 脱敏模块

用户上传的数据会首先经过数据脱敏模块，去除现实世界中的敏感信息。脱敏模块通过替换、删除或加密敏感数据来保护个人隐私，防止数据在传输、存储或处理过程中被泄露或滥用。数据在经过脱敏处理后，将进入mempool，等待验证者验证。当mempool中的数据规模达到一定数量时，将触发验证流程。

为满足不同场景的需求，开发者可以向社区提交自定义的脱敏模块供用户使用。被积极采用的模块的开发者将获得空投奖励，也可以采用订阅或分润的模式，从数据上传者的收益中获得回报。


<p align="center">
  <img src="https://github.com/ContributeDAO/.github/blob/main/profile/Uploader.png" alt="Uploader" width="900" />
</p>


# 数据验证

当上传的数据达到一定规模时，将触发数据验证。每条数据由两个验证者独立进行验证。如果两者均通过验证，则数据验证通过；如果两个验证者的初步验证结果不一致，则将数据交给第三个验证者进行复审，并以第三个验证者结果为准。验证通过的数据将被标记为已验证，并记录在数据集中并上链保存，确保验证结果的透明和不可篡改。

### 数据验证者

数据验证通过协议进行，上传者和验证者通过单独交换密钥，查看数据内容，检查上传数据是否符合购买方规范。待验证的数据从 mempool 中随机选取，具有更高验证奖励的优先。验证者通过质押的 ETH 参与验证，以保证其审查的公正性。

验证者参与数据验证需要满足以下条件：

1. **质押 ETH**：验证者必须质押一定量的 ETH 作为保证金，以确保其审查的公正性和有效性。
2. **贡献数据**：验证者必须在该 mempool 中上传并贡献过一份数据，以确保其对数据集的熟悉程度和参与度。

<p align="center">
  <img src="https://github.com/ContributeDAO/.github/blob/main/profile/Validator.png" alt="Validator" width="900" />
</p>

### 验证奖励机制

每条数据的验证奖励采用“荷兰拍”机制，即验证奖励会随时间逐渐增加。这种机制旨在鼓励验证者在验证任务发布初期即迅速完成验证，从而提高验证的效率。具体而言，每条数据的初始验证奖励较低，随着时间的推移，奖励会逐步增加，直到达到设定的上限。验证者的绩效将通过积分系统记录，最终奖励会根据验证者在该数据集中的积分与用户的奖励一同在截止日期发放到验证者的账户。

$$
R_v = \frac{I_v \times \sum_{i=1}^N I_{v_i}}{A_s}
$$

- $R_v$ 是验证者的最终奖励。
- $I_v$ 是验证者的积分。
- $A_s$ 是所有分润的金额。
- $\sum_{i=1}^{N} I_{v_i}$是所有参与验证的验证者的积分总和。

数据上传者可以设置价格的增长函数和初始价格，以提高自己数据被验证的优先级。同时，每个数据的验证会有 1min 的最晚时间（DDL），如果在最晚时间前没有完成验证，这份数据就会重新回到池子中，等待验证。奖励最终的实际大小取决于数据上传者定义的分润比例。

$$
I_v = P_d \times \alpha \times \left[ R_{\text{min}} + (R_{\text{max}} - R_{\text{min}}) \times \left(\frac{t}{T}\right)^n \right]
$$

- $I_v$ 是验证者的积分。.
- $P_d$ 是数据单价。
- $\alpha$ 是上传者设置的分润比例。
- $R_{\text{min}}$ 是荷兰拍奖励的最小值。
- $R_{\text{max}}$是荷兰拍奖励的最大值。
- $t$ 是当前时间点。
- $T$ 是荷兰拍奖励的总时间。
- $n$ 是奖励增长的指数。


<p align="center">
  <img src="https://github.com/ContributeDAO/.github/blob/main/profile/PriceCurve.png" alt="PriceCurve" width="900" />
</p>

# 数据购买

### 购买方

在 **Rebellion App** 中，购买方可以通过发布悬赏任务的方式来购买符合自己需求的数据。购买方可以设定价格，并通过悬赏任务吸引数据提供者上传或验证数据。此外，购买方还可以选择购买已经收集到的数据，或者与其他购买方合作，通过众筹方式共同资助购买特定的数据集。这种多样化的购买机制不仅提升了数据的利用率，也为数据提供者带来了更多的收益和激励。

### 质疑与反馈

购买方有权对数据验证结果提出质疑。质疑的提出机制旨在确保验证过程的公正性和透明度。具体而言：

1. **质疑处理**：
    - 若购买方对验证结果提出质疑，平台将启动质疑处理流程。如果质疑成功，验证者将失去与该数据相关的奖励，而质疑的数据的基础金额将转入项目方钱包。
2. **不信任投票**：
    - 如果购买方的拒绝率过高（例如，超过一定阈值），平台将启动不信任投票程序。该程序会对该购买方的行为进行评估，并可能禁用该购买方的发布权限，以防止滥用质疑机制。
    - 不信任投票的机制确保了购买方的质疑行为是真实有效的，而不是用来恶意干扰数据验证过程。


<p align="center">
  <img src="https://github.com/ContributeDAO/.github/blob/main/profile/Argue.png" alt="Argue" width="700" />
</p>

# 代币经济学

RBL token 是平台的流通代币，购买方发布悬赏任务将付给平台一部分佣金。数据上传者的收益和验证者的奖励都通过 RBL token 实现。

**Rebellion Token** 是为了激励网络参与者并推动平台的成长而发行的。代币系统不仅用来奖励数据共享的用户，还用来促进平台的治理和发展。通过发行 **Rebellion Token**，平台能够解决“冷启动问题”，并鼓励用户和开发者参与平台建设，从而扩大其网络效应。

![Tokenomics](https://github.com/ContributeDAO/.github/blob/main/profile/Tokenomics.png)

# RoadMap

**产品研发阶段**（2024年第三季度）

- 完成平台的基础功能开发，包括用户注册、数据上传和验证机制。
- 完成初步的系统集成和内部测试，确保平台功能的稳定性和可靠性。

**测试阶段**（2024年第四季度）

- 进行内部测试，修复系统漏洞和优化平台性能。
- 开展用户测试，收集用户反馈，优化用户体验和平台功能。

**上线阶段**（2025年第一季度）

- 正式上线平台，启动数据共享和验证的实际运营。
- 开展市场推广活动，吸引用户和项目方参与平台。

**扩展阶段**（2025年第二季度及以后）

- 扩大用户基础，增加数据需求，优化平台功能。
- 推动全球数据共享网络的发展，探索新的应用场景和合作机会
