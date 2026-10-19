## 01 基本信息

- **标题**：CasNano: An ultracompact CRISPR-Cas12f with a GC-rich PAM for epigenome editing with therapeutic potential
- **作者**：Kim, Dongkyeong; Huang, Chia-Wei; Pan, Richard; Qian, Junming; Wu, Xuebing; Devinsky, Orrin; Tsai, Yi-Ting; Liu, Shawn
- **单位**：未提供（摘要未列出作者单位）
- **期刊/平台**：Molecular Therapy - Nucleic Acids
- **年份**：2026（在线日期 2026-10-17）
- **论文类型**：研究论文（original research article）
- **领域**：CRISPR 基因编辑、表观基因组编辑、基因治疗递送
- **关键词**：Cas12f、超紧凑 CRISPR、表观基因组编辑、PAM、基因激活/沉默、病毒递送
- **DOI**：10.1016/j.omtn.2026.103106
- **代码**：未提供
- **数据**：未提供
- **阅读日期**：2026-05-13（基于当前对话日期推断）
- **在本课题方向中的位置**：本文属于 CRISPR 系统小型化与表观编辑方向，核心对象为 Cas12f（V-U4 型）的工程化改造。与 stagger-cleavage（交错切割）机制的直接关联有限——Cas12f 天然具有交错切割活性，但本文将其改造为催化失活（dCasNano）用于表观编辑，未涉及切割机制本身。对碱基编辑（base editing）方向的可迁移价值在于：其 sgRNA 优化策略、结构引导突变方法、以及 dCas 融合效应器（VPR/DNMT3A/TET1）的模块化架构，均可直接迁移至碱基编辑器的小型化与递送优化。

---

## 02 一句话总结

本文通过结构引导的蛋白突变与系统性 sgRNA 优化，将 400 氨基酸的 Blautia lenta Cas12f 改造为高效靶向哺乳动物基因组的超紧凑平台 "CasNano"，其催化失活形式（dCasNano）融合 VPR/DNMT3A/TET1 可实现与 SpCas9 相当或更优的基因激活及双向表观编辑，TET1 介导的激活在 hESC 中持续 5 个月，但 DNMT3A 甲基化在分裂细胞中 2 周内未保留。

---

## 03 研究问题

- **具体问题**：CRISPR-Cas 蛋白的大尺寸限制了其在体内的病毒递送效率，能否将天然活性极低的 400 aa Cas12f 工程化为高效、多功能的哺乳动物基因组靶向工具？
- **为什么重要**：腺相关病毒（AAV）等病毒载体的包装容量有限（~4.7 kb），SpCas9（~4.2 kb）加上 sgRNA 表达框后已接近容量上限，难以同时容纳效应器结构域（如碱基编辑器、表观编辑因子）。超紧凑 Cas 蛋白可释放载体容量，为体内治疗应用打开空间。
- **现有方法为何不足**：已报道的 Cas12f 家族（如 AsCas12f、Un1Cas12f）虽小，但编辑效率普遍偏低，且 PAM 偏好多为 AT-rich，限制了靶向范围；同时缺乏系统的 sgRNA 优化与效应器融合验证。
- **精确研究问题**："Can a minimally active 400-aa Cas12f ortholog be engineered into a potent, versatile epigenome editing platform for mammalian cells with efficiency comparable to SpCas9?"

---

## 04 背景与发展脉络

> 注：以下脉络基于本文框架及作者引述，标注「仅本文框架」或「经外部核验」。

| 阶段 | 代表性方法 | 优点 | 局限 | 本文位置 |
|------|-----------|------|------|---------|
| 早期 Cas9 系统 | SpCas9（~4.2 kb） | 效率高、靶向灵活 | 尺寸大，AAV 递送受限 | 作为基准对照 |
| 小型 Cas 蛋白发现 | Cas12f（Cas14）家族，~400-500 aa | 尺寸极小 | 天然活性低、PAM 受限（多为 AT-rich） | 起点：BlCas12f（400 aa） |
| Cas12f 工程化 | 结构引导突变 + sgRNA 优化（如 AsCas12f 的工程化） | 效率提升 | 多数仍低于 Cas9；PAM 偏好未根本改善 | 本文的多阶段策略 |
| 表观编辑融合 | dCas9-VPR / dCas9-DNMT3A / dCas9-TET1 | 可逆、不切割 DNA | 依赖大尺寸 dCas9 | 本文：dCasNano 融合上述效应器 |

**脉络核验状态**：以上背景中 SpCas9 尺寸、Cas12f 家族特征、VPR/DNMT3A/TET1 融合策略均属领域内广泛认可的知识（经外部核验）；具体 BlCas12f 的天然活性描述仅基于本文摘要（仅本文框架）。

---

## 05 核心痛点

| 痛点 | 表现 | 成因或作者解释 | 文中证据 |
|------|------|---------------|---------|
| Cas 蛋白尺寸过大 | SpCas9 等无法高效装入 AAV 等病毒载体 | 蛋白结构域多、分子量大 | 摘要首句："Clinical use of CRISPR-Cas proteins... constrained by their large size, limiting in vivo delivery" |
| 天然 Cas12f 活性极低 | 400 aa BlCas12f 在哺乳动物细胞中几乎无编辑活性 | 天然蛋白未适应真核环境，需工程化改造 | 摘要："minimally active, 400-amino acid Cas12f protein" |
| sgRNA 结构不匹配 | 天然 sgRNA 在哺乳动物细胞中表达/折叠效率低 | 原核来源的 sgRNA 支架与真核 RNA 加工机制不兼容 | 摘要提及 "systematic single guide RNA (sgRNA) optimization" 为必要步骤 |
| 表观编辑持久性差异 | DNMT3A 甲基化在分裂细胞中 2 周内丢失 | DNA 甲基化在 DNA 复制过程中被动稀释 | 摘要："DNMT3A-deposited methylation was not retained at 2 weeks in a dividing reporter line" |
| 公平比较困难 | 与 SpCas9 的效率比较受转染 stoichiometry 影响 | 不同编辑器表达水平无法归一化 | 摘要明确声明："editor expression was not quantified and stoichiometric differences would... preclude equivalent normalization" |

---

## 06 核心思想

### 1) 表面方法
- 从 Blautia lenta 中鉴定 400 aa Cas12f 直系同源物
- 结构引导的蛋白突变（多轮迭代）
- 系统性 sgRNA 支架优化
- 将优化后的 Cas12f 催化失活（dCasNano），融合 VPR（激活）、DNMT3A（甲基化沉默）、TET1（去甲基化激活）
- 在哺乳动物细胞（含 hESC）中验证功能

### 2) 核心洞察
- **尺寸不是效率的天然障碍**：通过合理的蛋白工程，极小尺寸的 Cas12f 可以达到与 SpCas9 相当的功能输出——关键在于蛋白与 sgRNA 的协同优化，而非单一因素。
- **GC-rich PAM（CCN）是差异化优势**：不同于多数 Cas12f 的 AT-rich PAM，CCN PAM 扩展了靶向空间，与现有工具形成正交互补。
- **表观编辑的持久性取决于效应器机制而非 Cas 骨架**：TET1 介导的激活可持续 5 个月，而 DNMT3A 甲基化在分裂细胞中快速丢失——这提示 Cas 骨架本身不决定表观修饰的稳定性。

### 3) 可能的普适教训 [Analysis]
- 小型 Cas 蛋白的工程化应同时优化蛋白与 RNA 组件，二者是耦合的协同系统，而非独立变量。
- 在比较不同尺寸的编辑器时，功能输出（而非分子活性）可能是更实际的评估标准，但必须明确声明比较的边界条件。
- 表观编辑工具的开发应明确目标细胞的增殖状态——分裂与非分裂细胞的表观修饰持久性预期应不同。

---

## 07 方法总览

- **输入**：Blautia lenta Cas12f 蛋白序列、天然 sgRNA 序列、目标基因位点
- **输出**：工程化 CasNano 平台（含 dCasNano 融合效应器），可在哺乳动物细胞中实现基因激活/沉默
- **模块**：
  1. 蛋白工程模块：结构引导突变
  2. sgRNA 优化模块：系统性支架改造
  3. 效应器融合模块：VPR / DNMT3A / TET1
  4. 功能验证模块：哺乳动物细胞转染、hESC 实验
- **训练/优化**：多轮迭代突变 + sgRNA 筛选（具体轮次未在摘要中说明）
- **反馈回路**：编辑效率/激活水平 → 指导下一轮突变设计
- **文字流程**：
  BlCas12f 鉴定 → 结构分析 → 蛋白突变 → sgRNA 优化 → 获得 CasNano → 催化失活（dCasNano）→ 融合效应器 → 转染哺乳动物细胞 → 检测基因激活/沉默效率 → 与 SpCas9 比较 → hESC 中验证持久性

---

## 08 核心模块拆解

| 模块 | 功能 | 为何需要 | 输入输出 | 支撑证据 | 移除后的已知或预期影响 |
|------|------|---------|---------|---------|---------------------|
| 结构引导蛋白突变 | 提升 BlCas12f 在哺乳动物细胞中的靶向活性 | 天然蛋白活性极低 | 输入：BlCas12f 结构/序列；输出：突变体文库 | 摘要："structure-guided protein mutagenesis" 为多阶段策略第一步 | 预期影响：无突变则活性不足以检测（作者暗示"minimally active"起点）[预期效应，未实测] |
| sgRNA 系统优化 | 适配哺乳动物表达系统，提升靶向效率 | 天然 sgRNA 在真核细胞中效率低 | 输入：天然 sgRNA 支架；输出：优化支架 | 摘要："systematic sgRNA optimization" 为必要步骤 | 预期影响：无优化则编辑效率显著下降 [预期效应，未实测] |
| dCasNano-VPR | 基因激活 | 验证激活功能 | 输入：dCasNano-VPR + sgRNA；输出：内源基因上调 | 摘要："activates endogenous genes with efficiency... comparable or superior to SpCas9" | 预期影响：无 VPR 则无激活功能 [预期效应] |
| dCasNano-DNMT3A | DNA 甲基化介导的基因沉默 | 验证沉默功能 | 输入：dCasNano-DNMT3A + sgRNA；输出：靶基因甲基化/沉默 | 摘要："DNMT3A-deposited methylation was not retained at 2 weeks" | 预期影响：无 DNMT3A 则无甲基化沉积 [预期效应] |
| dCasNano-TET1 | DNA 去甲基化介导的基因激活 | 验证激活的持久性 | 输入：dCasNano-TET1 + sgRNA；输出：靶基因去甲基化/再激活 | 摘要："TET1-mediated reactivation persisted for 5 months in hESCs" | 预期影响：无 TET1 则无去甲基化活性 [预期效应] |

> 注：摘要未提供消融实验数据，所有"移除后影响"均为基于功能逻辑的预期效应，非实测消融结果。

---

## 09 关键公式符号

**不适用**。本文为实验生物学研究，摘要中未包含数学模型或定量公式。涉及的定量概念（如效率比较、持久性时间）均为实验测量值，无公式化表达。

---

## 10 实验设计与证据链

- **数据集/群体**：哺乳动物细胞系（具体类型未在摘要中说明）、人胚胎干细胞（hESC）、报告基因细胞系（"dividing reporter line"）
- **规模**：未提供（具体基因位点数量、sgRNA 数量未说明）
- **指标**：基因激活效率、基因沉默效率、甲基化水平、去甲基化水平、持久性（时间）
- **基线/对照**：SpCas9 系统（等质量质粒转染）
- **预算/资源**：未提供
- **骨干/仪器**：未提供
- **oracle 输入**：不适用（非计算研究）
- **评测协议**：等质量质粒转染比较；未定量编辑器表达水平

| 实验 | 检验的 claim | 对比与条件 | 结果 | 支持的结论 | 不支持更强的结论 | 来源 |
|------|-------------|-----------|------|-----------|----------------|------|
| CasNano 靶向活性验证 | 工程化后 CasNano 可高效编辑哺乳动物基因组 | 与 SpCas9 等质量转染比较 | 激活效率与 SpCas9 相当或更优 | CasNano 是有效的靶向工具 | 无法推断其分子固有活性高于 SpCas9（表达量未归一化） | 摘要 |
| dCasNano-VPR 基因激活 | dCasNano 可融合效应器实现基因激活 | 特定 gRNA 和位点 | 激活成功 | dCasNano 支持 VPR 融合 | 未证明对所有基因位点均有效 | 摘要 |
| dCasNano-DNMT3A 沉默 | dCasNano 可介导 DNA 甲基化沉默 | 分裂报告细胞系 | 甲基化沉积但 2 周内丢失 | dCasNano-DNMT3A 可实现瞬时沉默 | 不适用于需要长期沉默的场景 | 摘要 |
| dCasNano-TET1 激活持久性 | TET1 介导的激活可长期维持 | hESC 中 | 持续 5 个月 | dCasNano-TET1 可实现持久激活 | 未说明是否所有位点均如此 | 摘要 |
| PAM 特性验证 | CasNano 识别 GC-rich（CCN）PAM | 序列分析/靶向实验 | CCN PAM 确认 | 与 AT-rich PAM 的 Cas12f 形成互补 | 未提供 PAM 全谱或特异性定量 | 摘要 |

---

## 11 结论正确解读

- **任务范围**：本文证明了 CasNano 在哺乳动物细胞（含 hESC）中作为表观编辑平台的功能可行性，包括基因激活（VPR、TET1）和沉默（DNMT3A）。
- **oracle/真值输入**：不适用（非计算研究）。
- **端到端状态**：从蛋白工程到功能验证的完整流程已实现，但尚未进入动物模型或临床前阶段。
- **算力成本**：不适用。
- **历史数据依赖**：依赖已知 Cas12f 结构信息进行突变设计。
- **模型依赖**：依赖哺乳动物细胞系和 hESC 作为功能验证模型。
- **最难情形**：分裂细胞中 DNMT3A 甲基化的不持久性——这提示该工具在快速增殖细胞中的沉默应用受限。
- **群体/领域边界**：结论限于所测试的 gRNA 和位点；与 SpCas9 的比较是功能输出层面的，非分子活性层面的。
- **不确定性**：编辑器表达量未定量，等质量转染的比较可能受蛋白稳定性、mRNA 翻译效率等差异影响。
- **有边界的复述**：在等质量质粒转染条件下，dCasNano-VPR 对测试位点的内源基因激活效率与 SpCas9 相当或更优；dCasNano-TET1 在 hESC 中可实现持续 5 个月的基因再激活；dCasNano-DNMT3A 在分裂细胞中沉积的甲基化在 2 周内丢失。这些结论不扩展到未测试的位点、细胞类型或体内环境。

---

## 12 作者自认局限

| 局限 | 具体表现 | 作者提出的未来方向 | 来源 |
|------|---------|-------------------|------|
| 与 SpCas9 比较的公平性受限 | 编辑器表达量未定量，等质量转染下 stoichiometry 差异无法排除 | 未明确提及（摘要中仅声明比较描述的是功能输出） | 摘要："editor expression was not quantified and stoichiometric differences would, in any case, preclude equivalent normalization" |
| DNMT3A 甲基化不持久 | 分裂报告细胞系中 2 周内甲基化丢失 | 未明确提及 | 摘要："DNMT3A-deposited methylation was not retained at 2 weeks in a dividing reporter line" |

**作者提及的相关约束**（非正式局限）：
- 比较结论限定于"所测试的 gRNA 和位点"（"for the guide RNAs (gRNAs) and loci tested"）
- 治疗潜力为"未来"方向（"potential for future therapeutic applications"），尚未进入临床验证

---

## 13 批判性分析

| [Analysis] 观察 | 潜在问题或替代解释 | 为何重要 | 如何检验 | 依据 |
|----------------|-------------------|---------|---------|------|
| 与 SpCas9 的比较仅基于功能输出 | 若 CasNano 蛋白表达量显著高于 SpCas9，则"相当或更优"可能反映表达差异而非固有活性优势 | 影响对 CasNano 实际效力的判断 | 定量检测两种编辑器在转染细胞中的蛋白/ mRNA 水平，计算单位分子活性 | 摘要明确声明表达量未定量 |
| "CCN PAM" 的靶向范围未定量 | 摘要未提供 PAM 全谱、位点覆盖率或脱靶率数据 | GC-rich PAM 是本文核心卖点之一，但缺乏定量支持 | 进行 PAM 全谱测定（如 PAM-SCANR）和全基因组脱靶分析 | 摘要仅提及 "distinct CCN PAM sequence" |
| DNMT3A 甲基化不持久可能受限于报告系统 | 报告细胞系为"dividing"状态，非分裂细胞（如神经元）中甲基化可能更稳定 | 影响对工具适用场景的判断 | 在非分裂细胞（如 post-mitotic neurons）中重复甲基化实验 | 摘要仅报告了分裂细胞中的结果 |
| 未报告 CasNano 的脱靶活性 | 小型 Cas 蛋白常因结构紧凑而特异性降低 | 脱靶是基因编辑工具临床转化的关键指标 | 进行全基因组脱靶检测（如 GUIDE-seq、CIRCLE-seq） | 摘要未提及脱靶数据 |
| hESC 中 5 个月持久性未说明细胞传代条件 | 若 hESC 在培养中持续传代，5 个月持久性可能受选择压力影响 | 影响对持久性机制的解读 | 检查实验方法中 hESC 的培养和传代条件 | 摘要未提供实验细节 |

---

## 14 学到什么

> **Agent 提炼的知识候选**

| 可迁移知识 | 来源 | 如何迁移到本课题（CRISPR 系统、stagger-cleavage、碱基编辑） |
|-----------|------|-----------------------------------------------------------|
| **蛋白与 sgRNA 协同优化策略** | 本文多阶段策略：结构引导突变 + 系统性 sgRNA 优化 | 碱基编辑器的小型化可借鉴此双轨优化思路——不仅优化脱氨酶结构域，还需同步优化 sgRNA 支架以适应紧凑骨架的构象变化 |
| **GC-rich PAM 作为正交靶向维度** | CasNano 的 CCN PAM | 碱基编辑器的靶向范围受 PAM 限制，开发 GC-rich PAM 的紧凑碱基编辑器可扩展可编辑位点，与现有 AT-rich PAM 工具形成互补 |
| **dCas 融合效应器的模块化验证流程** | dCasNano-VPR/DNMT3A/TET1 三系统并行验证 | 碱基编辑器可借鉴此模块化思路：将同一 Cas 骨架分别融合不同效应器（如胞嘧啶脱氨酶、腺苷脱氨酶），系统比较各融合体的效率与特异性 |
| **功能输出 vs 分子活性的比较框架** | 作者明确区分功能输出与内在活性 | 在碱基编辑器比较研究中，应明确报告表达量归一化状态，避免将表达差异误读为活性差异 |
| **表观编辑持久性取决于效应器而非骨架** | TET1 5 个月 vs DNMT3A 2 周 | 碱基编辑（DNA 永久改变）与表观编辑（可逆改变）的持久性机制不同，设计时应明确目标修饰类型及其在目标细胞增殖状态下的稳定性预期 |
| **超紧凑骨架的递送优势论证** | 400 aa 尺寸 vs AAV 容量限制 | 碱基编辑器（通常 >5 kb）的 AAV 递送是瓶颈，CasNano 的紧凑骨架可作为碱基编辑器的小型化支架候选，或拆分为双 AAV 系统时的组件优化参考 |

---

## 15 与已有知识连接

- **Cas12f 家族工程化**：本文与 AsCas12f（Wu et al., 2021, Nature Chemical Biology）、Un1Cas12f（O'Connell 实验室相关工作）的工程化研究形成直接对话。已知 Cas12f 家族成员经工程化后可在哺乳动物细胞中实现编辑，但 PAM 多为 AT-rich（如 AsCas12f 的 TTTR、Un1Cas12f 的 T-rich）。本文的 CCN PAM 是差异化贡献。
- **紧凑 CRISPR 系统**：与 CasX（~980 aa）、CasΦ（~700-800 aa）等小型系统研究脉络一致，均以尺寸最小化为目标。CasNano 的 400 aa 是目前已知最小的功能性 Cas 骨架之一。
- **表观编辑工具**：dCas9-DNMT3A/TET1 系统（Liu et al., 2016; Xu et al., 2016 等）是领域金标准，本文将其移植到 Cas12f 骨架，验证了紧凑骨架对效应器融合的兼容性。
- **碱基编辑连接** [Analysis]：本文未直接涉及碱基编辑，但其紧凑骨架 + 效应器融合的架构与碱基编辑器（dCas9-脱氨酶）的模块化设计逻辑一致。CasNano 骨架理论上可替换为碱基编辑器支架，但需验证脱氨酶融合后的活性与特异性——这是未经验证的候选方向。
- **AAV 递送**：AAV 包装容量 ~4.7 kb 是领域共识（经外部核验），本文的尺寸优势论证建立在此约束上。
- **潜在冲突** [Analysis]：作者声称与 SpCas9 "comparable or superior"，但未定量表达量，这一比较的稳健性存疑。领域内其他 Cas12f 工程化研究（如 AsCas12f）通常报告低于 SpCas9 的编辑效率，本文的"相当或更优"需要更严格的验证。

---

## 16 研究想法

> **Agent 生成的研究候选**

### 候选 1：CasNano 骨架的碱基编辑器开发
- **名称**：CasNano-BE（碱基编辑器）
- **来源局限/观察**：CasNano 已验证可融合 VPR/DNMT3A/TET1 等效应器，且尺寸极小（400 aa），但未测试脱氨酶融合
- **核心假设**：dCasNano 融合胞嘧啶脱氨酶（如 rAPOBEC1）或腺苷脱氨酶（如 TadA-8e）可实现高效的碱基编辑，且总尺寸 < 4.7 kb 可装入单 AAV
- **相对本文的增量**：将 CasNano 从表观编辑扩展到碱基编辑，验证其作为通用紧凑支架的潜力
- **初步方法**：构建 dCasNano-脱氨酶-UGI 融合体，在 HEK293T 中测试多个内源位点的编辑效率与窗口；与 dCas9-BE 比较；测定 PAM 兼容性
- **验证方式**：Sanger 测序/靶向 NGS 检测编辑效率与 bystander 编辑；全基因组脱靶分析
- **可能的失败模式**：Cas12f 骨架与脱氨酶的构象不兼容导致编辑窗口异常或活性极低；紧凑骨架可能缺乏足够的 DNA 结合稳定性
- **创新状态**：unverified

### 候选 2：CasNano 的 stagger-cleavage 机制表征
- **名称**：CasNano 切割机制解析
- **来源局限/观察**：Cas12f 家族天然具有交错切割（staggered cleavage）活性，但本文将其催化失活，未表征其切割模式
- **核心假设**：CasNano 的工程化突变可能改变了其天然切割模式（切口位置、5' 突出端长度），这些信息对理解 Cas12f 机制和优化 HDR 编辑有参考价值
- **相对本文的增量**：补充 CasNano 的生化表征，为后续基于切割的编辑应用（如 HDR、基因敲入）提供基础
- **初步方法**：体外切割实验 + 测序确定切口位置；比较野生型 BlCas12f 与 CasNano 的切割模式
- **验证方式**：体外切割产物 Sanger 测序/凝胶电泳
- **可能的失败模式**：CasNano 的突变可能已完全消除切割活性（若催化残基被突变），需先确认是否保留活性
- **创新状态**：unverified

### 候选 3：CasNano 在非分裂细胞中的表观编辑持久性
- **名称**：CasNano 在 post-mitotic 细胞中的表观编辑稳定性
- **来源局限/观察**：DNMT3A 甲基化在分裂细胞中 2 周内丢失，但未测试非分裂细胞
- **核心假设**：在非分裂细胞（如神经元）中，DNMT3A 介导的甲基化可能更持久，因为缺乏 DNA 复制导致的被动稀释
- **相对本文的增量**：扩展 CasNano 的适用场景，评估其在神经系统疾病（如癫痫、局灶性皮质发育不良）中的治疗潜力
- **初步方法**：在分化神经元或 post-mitotic 细胞中测试 dCasNano-DNMT3A 的甲基化维持时间
- **验证方式**：亚硫酸盐测序检测甲基化水平随时间变化
- **可能的失败模式**：非分裂细胞中 DNMT3A 的初始甲基化效率可能更低，导致即使持久也无法达到功能阈值
- **创新状态**：unverified

### 候选 4：CasNano 的 PAM 谱全表征与工程化扩展
- **名称**：CasNano-PAM 工程
- **来源局限/观察**：本文仅提及 "CCN PAM"，未提供 PAM 全谱或特异性定量
- **核心假设**：通过蛋白工程可扩展 CasNano 的 PAM 兼容性，或提高其特异性
- **相对本文的增量**：为 CasNano 的靶向范围提供更完整的图谱，并探索 PAM 工程化
- **初步方法**：PAM-SCANR 或类似方法测定全 PAM 谱；基于结构信息设计 PAM 互作域突变体
- **验证方式**：高通量 PAM 测定 + 活性验证
- **可能的失败模式**：CCN PAM 的 GC-rich 特性可能由蛋白结构刚性决定，工程化空间有限
- **创新状态**：unverified

### 候选 5：CasNano 与碱基编辑器的 AAV 递送比较
- **名称**：单 AAV 递送 CasNano-BE 的体内可行性
- **来源局限/观察**：CasNano 的尺寸优势（400 aa）理论上可容纳碱基编辑所需的所有组件于单 AAV
- **核心假设**：CasNano-BE 的总表达框 < 4.7 kb，可单 AAV 递送，且体内编辑效率不低于双 AAV 系统
- **相对本文的增量**：将 CasNano 从体外验证推进到体内递送可行性
- **初步方法**：计算 CasNano-BE 表达框大小；构建单 AAV 载体；在小鼠模型中验证
- **验证方式**：体内编辑效率检测（靶向 NGS）
- **可能的失败模式**：即使尺寸允许，表达框的顺式调控元件（启动子、polyA）可能超出容量；体内递送效率受组织特异性影响
- **创新状态**：unverified