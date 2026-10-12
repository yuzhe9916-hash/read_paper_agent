## Review setup
- **Input scope** 全文（含摘要、引言、方法、结果、讨论）
- **Assessment boundary** 仅基于所提供手稿内容进行评审，不涉及外部文献或未提供数据
- **Shared manuscript claim summary** 作者通过7个冷冻电镜捕获的R-loop中间态（6–18 nt）的分子动力学模拟，提出CRISPR-Cas9的HNH结构域激活经历"解锁-预组织-前催化门控"三阶段变构程序，并在18-nt检查点出现动态挫抑（dynamically frustrated）的亚稳态，该状态与构象校对（conformational proofreading）模型一致。作者进一步通过深度学习分析和深度突变扫描交叉验证，鉴定出Y450和K1200两个候选传感器残基，并通过细胞报告实验对部分预测进行了初步验证。
- **Visible evidence base** 35 μs全原子MD模拟（7状态×5重复×1 μs）、PCA分析、ΔRMSF分析、动力学网络分析（GCCM、介数中心性、社区分析）、VESM和ProteinMPNN深度学习分析、Spencer-Zhang DMS数据交叉验证、GFP报告实验（19个构建体）
- **Missing materials affecting confidence** 补充图S1–S18、补充表S1–S8、补充注释1–5均未提供；MD轨迹原始数据未提供；流式细胞术原始数据未提供；DMS交叉验证的具体统计细节未提供

## Reviewer
- **Overall assessment** 该手稿提出了一个具有概念新颖性的Cas9激活模型，将MD模拟、深度学习和实验验证相结合，体现了计算生物学与实验生物学的良好整合。然而，核心概念"动态挫抑"的操作性定义与形式化验证之间存在明显张力，且关键实验证据（报告实验）仅测量了单一匹配靶点的切割活性，无法支撑关于"校对"或"保真度"的结论。手稿在方法学上有一定创新性，但核心结论的证据链尚不完整。

- **Who would be interested in the results, and why** 该研究对以下群体具有潜在吸引力：(1) CRISPR-Cas9工程改造领域的研究者，特别是关注高保真变体设计的研究组；(2) 计算生物物理学家，尤其是从事变构调控和构象动力学模拟的学者；(3) 分子机制导向的核酸酶研究者。其"多阶段变构检查点"框架可能为Cas9工程提供新的理性设计靶点。

- **Major strengths** 
  1. 系统性地覆盖了7个实验捕获的R-loop中间态，是目前对Cas9激活路径最全面的MD研究之一
  2. 将MD模拟、深度学习（VESM、ProteinMPNN）和DMS数据三方交叉验证，方法论上具有示范意义
  3. 对Y450和K1200的传感器功能预测具有可检验性，且Y450的预测与已有实验数据吻合
  4. 作者对"挫抑"一词的操作性定义进行了明确限定，避免了过度解释

- **Major Concerns**

- **Concern ID** R1-M1
- **Severity** Major
- **Blocking** Yes
- **Axis** 核心概念的操作性定义与验证
- **Claim pointer** "At the 18-nt checkpoint, HNH and REC2 regain mobility but do not adopt a fully cleavage-competent orientation; this dynamically frustrated metastate is consistent with a conformational-proofreading model."
- **Evidence pointer** Results: "A dynamically frustrated checkpoint emerges at the 18-nt state"; Discussion
- **Concern** 作者明确承认"挫抑"是操作性定义（"renewed mobility and weakened directional coupling"），而非形式化的能量挫抑计算。然而，手稿的核心标题和主要结论均围绕"动态挫抑"展开。问题在于：(1) "renewed mobility"和"weakened directional coupling"如何被定量化？ΔRMSF的+0.483 Å（HNH）和+0.442 Å（REC2）是否具有统计显著性？(2) "weakened directional coupling"的度量标准是什么？文中未提供耦合强度的定量比较或置信区间。(3) 如果"挫抑"仅指"流动性增加"，那么它与"未完全就绪"有何本质区别？缺乏一个可证伪的定量判据来区分"挫抑的亚稳态"与"简单的未激活态"。
- **Why it matters** 核心概念的操作性定义若缺乏定量支撑，整个"构象校对"模型的解释力将被削弱。读者无法判断该"挫抑态"是Cas9激活路径中的功能性检查点，还是MD采样不足或力场误差的产物。
- **Resolution test** 提供HNH/REC2在16-nt与18-nt状态间的构象自由能面（如umbrella sampling或metadynamics），或提供耦合强度的定量度量（如广义相关系数）及其统计置信区间，以证明"挫抑"是一个可区分的动力学状态而非采样噪声。

---

- **Concern ID** R1-M2
- **Severity** Major
- **Blocking** Yes
- **Axis** 实验验证与核心结论的匹配度
- **Claim pointer** "In a cellular cleavage reporter assay, R1210D reproduces the attenuated low-completion phenotype of eSpCas9, identifying it as a candidate for direct specificity testing"
- **Evidence pointer** Results: "Experimental testing of computational nominations"; Figure 8
- **Concern** 报告实验仅使用了一个完全匹配的靶点，测量的是切割活性（cleavage activity），而非特异性（specificity）或保真度（fidelity）。R1210D表现出与eSpCas9(1.1)相似的"低完成度"表型，但这只能说明该突变降低了切割效率，不能说明它提高了辨别能力。事实上，一个仅降低活性而不影响辨别力的突变也会产生类似表型。作者在摘要和讨论中均谨慎地使用了"candidate for direct specificity testing"的表述，但标题和整体叙事框架暗示该模型与"conformational proofreading"直接相关，而实验部分并未提供任何错配靶点的数据来检验校对假说。
- **Why it matters** 构象校对的核心预测是：错配靶点应在检查点被更有效地拒绝。没有匹配vs错配的对比数据，就无法区分"活性降低"与"保真度提高"两种截然不同的机制。这直接影响到"conformational proofreading"这一核心结论的可检验性。
- **Resolution test** 在报告实验中加入错配靶点（如PAM远端1-3个错配），比较R1210D在匹配与错配靶点上的相对活性变化。若R1210D在错配靶点上的活性降低幅度显著大于匹配靶点，则支持保真度提高的假说。

---

- **Concern ID** R1-M3
- **Severity** Major
- **Blocking** No
- **Axis** 因果推断的强度
- **Claim pointer** "Two sensors, Y450 at the sgRNA:DNA hybrid interface and K1200 in the PI domain, respond to distinct maturation milestones, encoding heteroduplex length into domain-specific conformational outputs."
- **Evidence pointer** Results: "Dynamical network analysis identifies Y450 and K1200 as candidate sensor residues"
- **Concern** Y450和K1200被鉴定为"传感器"主要基于介数中心性峰值和与核酸的接触模式。然而，相关性不等于因果性。Y450在8-nt处的高介数中心性可能只是R-loop构象重排的伴随现象，而非主动"感知"异源双链长度的功能元件。作者未提供突变Y450或K1200后网络拓扑变化的对照模拟，也未在实验部分测试Y450突变体（仅测试了R1210、Q771、K772、Y271、L625等）。"传感器"这一功能归属需要更直接的因果证据。
- **Why it matters** 如果Y450和K1200并非功能性传感器，而只是网络分析中的人为产物，那么"双传感器架构"这一模型将失去实验基础。该模型是手稿对Cas9工程改造建议的核心依据。
- **Resolution test** 对Y450和K1200进行丙氨酸扫描突变后的MD模拟，检验网络拓扑和耦合路径是否发生预期变化；或在实验部分加入Y450突变体的报告实验数据。

---

- **Concern ID** R1-M4
- **Severity** Major
- **Blocking** No
- **Axis** 模拟的力场选择与验证
- **Claim pointer** "Using extensive molecular dynamics simulations across seven experimentally trapped heteroduplex states (6–18 nt)"
- **Evidence pointer** Materials and methods: "Molecular dynamics simulations"
- **Concern** 手稿未说明使用的力场版本（如ff19SB与OL3/bsc1的组合是否经过针对蛋白质-核酸复合物的参数验证）、水模型、离子浓度和盐桥处理方式。更重要的是，未提供模拟与实验数据（如冷冻电镜结构、FRET距离、氢氘交换等）的直接对比验证。对于35 μs的累积采样量，力场偏差可能被放大，特别是在涉及HNH结构域大尺度构象重排的模拟中。
- **Why it matters** MD模拟的结论高度依赖力场准确性。若力场对蛋白质-核酸界面相互作用的描述存在系统偏差，则"动态挫抑"和"传感器"等结论可能反映的是力场伪影而非真实生物学。
- **Resolution test** 提供力场参数验证数据（如与实验B因子、Rg或FRET距离的对比），或至少提供不同力场（如ff19SB vs. CHARMM36m）的重复模拟结果以证明结论的力场稳健性。

- **Minor Comments**

- **Concern ID** R1-m1
- **Severity** Minor
- **Axis** 可重复性
- **Affected element** 方法学描述
- **Evidence pointer** Materials and methods: "Molecular dynamics simulations"
- **Issue** 模拟参数（力场版本、水模型、离子浓度、温度耦合方式、压力耦合方式、截断距离等）未完整列出，补充注释1未提供。
- **Required correction** 在补充材料中提供完整的模拟参数表，包括软件版本、力场、水模型、离子条件、系综、温度/压力耦合参数、截断距离、模拟时长和重复次数。

- **Concern ID** R1-m2
- **Severity** Minor
- **Axis** 统计显著性
- **Affected element** ΔRMSF分析
- **Evidence pointer** Results: "A dynamically frustrated checkpoint emerges at the 18-nt state"
- **Issue** ΔRMSF的±0.2 Å阈值被用作"操作性"分类标准，但未提供该阈值的统计依据（如噪声水平估计、重复间变异性）。
- **Required correction** 提供重复模拟间的ΔRMSF变异性估计（如标准误或置信区间），并说明±0.2 Å阈值相对于噪声水平的倍数关系。

- **Concern ID** R1-m3
- **Severity** Minor
- **Axis** 概念表述
- **Affected element** 摘要与讨论中的"conformational proofreading"表述
- **Evidence pointer** Abstract; Discussion
- **Issue** 作者在摘要中称模型"consistent with conformational proofreading"，但在讨论中承认"direct matched-versus-mismatched validation is required"。这种"先提出、后限定"的表述方式容易让读者高估证据强度。
- **Required correction** 在摘要中更明确地标注该模型为"proposed"或"hypothesized"，并将"consistent with"改为"motivates a testable model of"。

- **Concern ID** R1-m4
- **Severity** Minor
- **Axis** 数据可视化
- **Affected element** 图8
- **Evidence pointer** Results: "Experimental testing of computational nominations"; Figure 8
- **Issue** 图8的流式细胞术数据以柱状图呈现，未显示单个数据点分布或原始散点图，无法评估重复间的变异性。
- **Required correction** 在补充材料中提供每个构建体的散点图或原始流式细胞术图，并标注每个时间点的独立重复次数。

- **Concern ID** R1-m5
- **Severity** Minor
- **Axis** 文献定位
- **Affected element** 引言与讨论
- **Evidence pointer** Introduction; Discussion
- **Issue** 讨论中未充分对比Lu et al.的gear-wedge模型与本文三阶段模型的异同，特别是两者在HNH激活机制上的预测差异。
- **Required correction** 增加一段对比分析，明确本文模型与gear-wedge模型在机制预测上的区别与互补性。

## Risk / unsupported claims
1. "Dynamically frustrated"作为核心概念，其操作性定义（流动性增加、耦合减弱）缺乏定量判据和统计检验，目前不可评估其是否为真实的物理状态。
2. "Conformational proofreading"模型的适用性：手稿未提供任何错配靶点的模拟或实验数据，该模型目前仅为推测性假说。
3. "Y450和K1200作为传感器"的功能归属缺乏因果验证（如突变模拟或实验），目前仅为相关性推断。
4. "R1210D reproduces the attenuated low-completion phenotype of eSpCas9"仅基于单一匹配靶点的报告实验，无法区分活性降低与保真度提高。
5. "RuvC-III作为变构信号枢纽"的结论主要基于结构开关富集分析，缺乏功能验证。
6. 三阶段模型的普适性：所有模拟均基于Pacesa et al.的冷冻电镜结构，这些结构本身是在特定错配条件下捕获的，模型是否适用于完全匹配的天然底物尚不明确。