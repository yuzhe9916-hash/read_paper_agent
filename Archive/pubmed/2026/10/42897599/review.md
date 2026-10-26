## Review setup
- **Input scope** 全文（含摘要、方法、结果、讨论、补充材料说明）
- **Assessment boundary** 仅基于提供的稿件文本进行评估；补充材料（图、表、视频）内容不可直接核验，仅能依据正文中的描述进行推断
- **Shared manuscript claim summary** 作者首次建立了猪成体干细胞来源的肺类器官（PLO），并开发了一种基于GFP引导富集（GFP-guided enrichment）的CRISPR/Cas9和prime editing基因组编辑平台，通过GFP阴性筛选和单类器官克隆扩增实现高效、高均一性的基因编辑
- **Visible evidence base** 正文中的图2（PLO建立与表征）、图3（CFTR/CD163编辑与克隆）、图4（双sgRNA截断与PE）、表1-4（深度测序与Sanger测序数据）、补充图1-5及补充表1-3的正文描述
- **Missing materials affecting confidence** 补充图1-5、补充表1-3、补充视频3-8、全膜/全胶原始图像均未提供，无法独立核验关键定量数据和原始证据

## Reviewer
- **Overall assessment** 该稿件报告了一项技术上合理且具有一定新颖性的工作：首次建立了可长期培养的猪成体干细胞来源肺类器官，并系统验证了GFP引导富集策略在CRISPR/Cas9、双sgRNA介导的基因组截断和prime editing三种编辑模式中的富集效果。方法学逻辑清晰，数据呈现较为完整。然而，稿件存在若干需要澄清或补充的关键问题，尤其是在CFTR编辑后蛋白功能未丧失的解释、GFP阴性筛选的机制假设、以及部分定量数据的统计呈现方面。总体而言，该工作对器官oid基因组编辑领域有潜在贡献，但核心结论的稳健性需在修订中进一步巩固。

- **Who would be interested in the results, and why** 从事类器官工程、基因编辑技术开发、猪作为大动物疾病模型（尤其是囊性纤维化、人畜共患传染病如PRRSV和流感病毒）的研究人员会对此感兴趣。GFP引导富集策略本身具有通用性，可能被推广至其他成体干细胞来源的类器官系统，因此对更广泛的器官oid编辑领域具有方法学参考价值。

- **Major strengths** 
  1. 首次报道了猪成体干细胞来源的肺类器官的长期培养（超过20代）和冻存复苏能力，填补了猪肺类器官模型的空白。
  2. GFP引导富集策略在三种编辑模式（Cas9 indel、双sgRNA截断、prime editing）中均显示出一致的富集效果，方法学验证较为系统。
  3. 通过单类器官克隆扩增实现了高遗传均一性（99.7-99.9% indel频率），解决了类器官编辑中常见的嵌合体问题。
  4. 对CFTR编辑后的功能保留进行了多层面验证（cDNA测序、Western blot、AlphaFold2结构预测、FIS功能实验），体现了较为严谨的验证思路。

- **Major Concerns**

- **Concern ID** R1-M1
- **Severity** Major
- **Blocking** Yes
- **Axis** 结论稳健性
- **Claim pointer** "These results confirmed that DNA to protein levels modifications were successfully induced. However, alternative translation initiation downstream of the original start codon led to the production of a functional protein isoform despite successful gene editing."
- **Evidence pointer** 图3G、补充图4A-C、补充材料3-8
- **Concern** 作者在CFTR基因起始密码子附近引入移码突变后，Western blot仍检测到正常大小的CFTR蛋白，且FIS实验显示氯离子通道功能保留。作者将此归因于下游替代起始密码子的使用，但未提供任何直接证据（如N端截短蛋白的特异性抗体检测、质谱分析、或针对替代起始密码子的突变实验）来验证这一假设。此外，AlphaFold2预测的"结构基本完整"并不能替代实验验证。如果替代翻译起始的假设不成立，则"成功生成完全基因编辑类器官"的核心结论将受到根本性质疑。
- **Why it matters** 该稿件声称建立了高效基因编辑平台，但CFTR编辑后蛋白功能未丧失这一事实意味着编辑并未实现功能性敲除。如果读者期望使用该系统进行疾病建模（如囊性纤维化），则功能性敲除的失败将直接限制该平台的实用性。
- **Resolution test** 需要提供直接证据证明替代起始密码子的使用，例如：(1) 使用识别N端区域的抗体进行Western blot，显示截短蛋白；(2) 对替代起始密码子进行定点突变后功能丧失；(3) 质谱分析确认N端序列缺失。若无法提供此类证据，应明确承认功能性敲除未实现，并讨论其对平台适用性的影响。

- **Concern ID** R1-M2
- **Severity** Major
- **Blocking** No
- **Axis** 方法学完整性
- **Claim pointer** "GFP-guided enrichment significantly enriched edited cells; the mutation ratio in the GFP-negative group was significantly higher than that in the GFP-positive group."
- **Evidence pointer** 图3C、表1、补充图2D、3D
- **Concern** 稿件未报告GFP阴性筛选的富集倍数或绝对编辑效率提升幅度。表1中CFTR编辑的GFP(−)组indel频率为92.1%，GFP(+)组为68.7%，富集效果显著但并非完全分离。CD163编辑的GFP(−)组仅34.1%，远低于CFTR编辑，但作者未讨论为何不同基因位点间富集效果差异如此之大。此外，GFP(−)组中仍存在未编辑细胞（7.9%和65.9%），作者未讨论这些残留未编辑细胞的来源（是筛选不彻底还是编辑失败后GFP沉默？）。
- **Why it matters** 富集策略的普适性和效率边界需要明确界定。如果CD163位点的富集效果远弱于CFTR位点，读者无法判断该策略在不同基因位点间的可预期表现。
- **Resolution test** 建议补充：(1) 不同基因位点的富集效率对比分析及可能的影响因素讨论；(2) GFP(−)组中未编辑细胞的单细胞分析或连续传代后的编辑频率追踪，以排除GFP沉默导致的假阴性筛选。

- **Concern ID** R1-M3
- **Severity** Major
- **Blocking** No
- **Axis** 数据呈现完整性
- **Claim pointer** "The GFP(−) group exhibited a significantly higher gene-editing efficiency of 93.8%, whereas the GFP(+) group showed a considerably lower efficiency of 26.7%"
- **Evidence pointer** 补充图4E、补充表3
- **Concern** 针对CFTR外显子11（F508区域）的编辑实验中，GFP(+)组的编辑效率为26.7%，远高于此前外显子4编辑实验中GFP(+)组的68.7%和29.6%（表1和表4中对应数据）。作者未解释为何不同靶位点间GFP(+)组的"未富集"基线编辑效率差异如此之大。此外，外显子11的编辑实验仅报告了GFP(+)与GFP(−)两组的比较，未提供未转染对照或NS组的编辑效率数据，无法评估该位点的基线编辑效率。
- **Why it matters** 富集策略的有效性评估需要基线编辑效率作为参照。如果不同位点的基线编辑效率差异显著，则GFP富集的绝对增益需要重新计算。
- **Resolution test** 建议补充外显子11编辑实验中NS组的编辑效率数据，并讨论不同靶位点间编辑效率差异的可能原因（如染色质可及性、gRNA活性差异等）。

- **Concern ID** R1-M4
- **Severity** Major
- **Blocking** No
- **Axis** 统计方法
- **Claim pointer** "P < 0.0000001"（表1、表4及正文多处）
- **Evidence pointer** 表1、表4、图3C、图4G-H
- **Concern** 所有统计检验均报告为Fisher's exact test，但未说明各组的样本量（测序reads数）、独立生物学重复数、以及效应量。对于深度测序数据，数十万reads的差异在统计上几乎必然显著，但生物学意义需要效应量和重复性来支撑。此外，Sanger测序数据（表3）未报告统计检验方法。
- **Why it matters** 极小的P值可能掩盖较小的效应量或缺乏生物学重复的问题。读者无法判断富集效果在不同实验批次间的稳定性。
- **Resolution test** 建议补充：(1) 各组的reads数、独立实验重复数；(2) 效应量（如富集倍数及95%置信区间）；(3) 对Sanger测序数据采用适当的统计检验或明确说明为描述性统计。

- **Minor Comments**

- **Concern ID** R1-m1
- **Severity** Minor
- **Axis** 方法学描述
- **Affected element** 类器官来源与细胞类型组成
- **Evidence pointer** 图2C-D、方法部分
- **Issue** 作者报告PLO表达SP-C、KRT5、SOX2和vimentin，但未报告细胞类型组成的定量分析（如各标记共表达比例、细胞类型占比）。"Composite lung organoid identity"的结论主要基于定性染色。
- **Required correction** 建议补充定量分析（如流式细胞术或单细胞RNA测序）或至少提供多个视野的定量统计，以支持多谱系组成的结论。

- **Concern ID** R1-m2
- **Severity** Minor
- **Axis** 方法学描述
- **Affected element** 猪源材料伦理声明
- **Evidence pointer** 方法部分"Porcine lung tissue was obtained from piglets that have been euthanized by farm personnel for routine management purposes"
- **Issue** 作者声明不需要IACUC批准，但未提供任何机构伦理委员会关于该豁免决定的书面确认或政策引用。
- **Required correction** 建议补充机构伦理委员会关于该豁免的正式声明或政策文件编号。

- **Concern ID** R1-m3
- **Severity** Minor
- **Axis** 数据呈现
- **Affected element** 图3F和表2的突变模式分析
- **Evidence pointer** 图3F、表2
- **Issue** 表2中"1 bp ins or 8 bp del"的突变模式描述过于笼统，未区分各克隆中两种突变类型的比例。图3F的indel图谱未标注具体克隆编号。
- **Required correction** 建议在表2中为每个克隆提供两种突变类型的详细比例，并在图3F中标注克隆编号以便对应。

- **Concern ID** R1-m4
- **Severity** Minor
- **Axis** 讨论深度
- **Affected element** 与已有猪肺类器官研究的比较
- **Evidence pointer** 讨论部分
- **Issue** 作者声称"首次建立"猪成体干细胞来源肺类器官，但未系统比较已有猪肺类器官或猪气道类器官研究（如参考文献29、30中可能涉及的猪气道类器官）与本研究的差异。
- **Required correction** 建议在讨论中明确区分本研究与已有猪气道类器官研究在细胞来源、培养条件和谱系组成方面的差异，以支持"首次"声明。

- **Concern ID** R1-m5
- **Severity** Minor
- **Axis** 数据呈现
- **Affected element** 补充图4C的FIS实验
- **Evidence pointer** 补充图4C、补充材料3-8
- **Issue** FIS实验仅提供了代表性图像和视频，未报告定量数据（如类器官面积变化百分比、响应类器官比例）。
- **Required correction** 建议补充FIS实验的定量分析（至少3个独立实验的汇总数据），以支持"功能保留"的结论。

- **Concern ID** R1-m6
- **Severity** Minor
- **Axis** 方法学描述
- **Affected element** prime editing效率的绝对数值
- **Evidence pointer** 图4E-H、表4
- **Issue** 正文仅报告了GFP(−)组PE效率为1.8%，但未报告NS组的绝对PE效率（表4中NS组为0.7%）。虽然富集效果显著，但1.8%的绝对效率仍较低，作者未讨论这是否足以支持后续应用。
- **Required correction** 建议在讨论中明确承认PE绝对效率的局限性，并讨论可能的优化方向。

## Risk / unsupported claims
1. "完全基因编辑的类器官克隆"（fully gene-edited clones）的表述可能过度，因为表2中克隆#7的indel频率为86.2%，克隆#11为58.2%，克隆#13为98.6%，并非所有克隆都达到99%以上。作者在正文中称"12 out of 14 exhibited indel mutation frequencies exceeding 98%"，但表2中克隆#7（86.2%）和#11（58.2%）明显低于此阈值，存在数据不一致。
2. "首次建立猪成体干细胞来源肺类器官"的声明需要更系统的文献比较来支撑，特别是与已有猪气道类器官研究的差异。
3. 关于GFP引导富集机制的解释（GFP阴性反映共递送成功）缺乏直接证据，如单细胞水平的共定位分析或转染效率的定量比较。
4. 补充材料中声称的"全膜/全胶原始图像"未提供，无法核验Western blot数据的完整性。
5. 表1中CFTR编辑的GFP(+)组indel频率为68.7%，远高于CD163编辑的GFP(+)组（1.4%），作者未解释这一巨大差异，可能反映不同位点的基线编辑效率差异，但也可能涉及实验条件的不一致。