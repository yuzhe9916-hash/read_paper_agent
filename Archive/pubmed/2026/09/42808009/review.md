## Review setup
- **Input scope** Full manuscript text (abstract, introduction, results, discussion, methods, data availability)
- **Assessment boundary** Scientific and technical evaluation of the ProNA3D tool, its demonstrated applications, and the validity of claims made in the provided text. No code execution or hands-on testing was performed.
- **Shared manuscript claim summary** The authors present ProNA3D, a UCSF ChimeraX plug-in and command-line tool for unified interface analysis of protein–nucleic acid and nucleic acid-only complexes. The tool supports experimental and predicted structures (including AlphaFold 3 scoring metrics), offers 2D interface visualization and secondary-structure topology plots, and includes cryo-EM density zoning. Applications include case studies on a hammerhead ribozyme, an HIV-1 RNA–antibody complex, a Cre recombinase–DNA complex, and a DHX36–G-quadruplex RNA complex, plus a large-scale PDB analysis revealing interface connectivity trends.
- **Visible evidence base** Four case study descriptions (Sections: X-ray structure of an RNA-only complex; Predicted protein–RNA complex; Predicted protein–DNA complex; Cryo-EM structure of a protein–RNA complex), large-scale PDB analysis (Section: Systematic analysis), Methods section, Figures 1–6 referenced, Tables S1–S14 referenced, Supplementary Figures S1–S7 referenced.
- **Missing materials affecting confidence** Figures and supplementary materials not provided. No code repository contents, no user documentation, no benchmark comparisons against existing tools, no statistical details beyond Mann–Whitney U test references, no validation metrics for the connectivity analysis beyond descriptive statistics.

## Reviewer
- **Overall assessment** The manuscript describes a timely and potentially useful software tool that addresses a genuine gap in the analysis of nucleic acid-containing complexes, particularly for predicted structures. The integration of interface detection, topology visualization, confidence scoring, and cryo-EM density zoning into a ChimeraX plug-in is a sensible and practical design. The case studies are appropriate demonstrations, and the large-scale PDB analysis provides interesting biological observations. However, the manuscript as presented has several weaknesses: the validation of the tool's core algorithms is limited, the novelty relative to existing tools (e.g., DNAproDB, RNAproDB, PICKLUSTER) is not crisply articulated, and the large-scale analysis conclusions are somewhat descriptive without deeper functional or structural interpretation. The absence of figures and supplementary data in the provided material limits full assessment.

- **Who would be interested in the results, and why** Structural biologists studying protein–nucleic acid complexes, particularly those working with cryo-EM or AlphaFold 3 predictions; computational biologists developing or using interface analysis tools; researchers studying RNA biology, ribozymes, CRISPR systems, and DNA-modifying enzymes. The tool's accessibility as a ChimeraX plug-in broadens its potential user base within the structural biology community.

- **Major Strengths**
  1. Addresses a real and current need: unified analysis of nucleic acid-containing interfaces in both experimental and predicted structures, with explicit support for AlphaFold 3 outputs.
  2. The integration of multiple analysis modalities (interface detection, topology plots, 2D graphs, confidence metrics, cryo-EM density zoning) into a single plug-in is practical and likely to be adopted.
  3. The large-scale PDB analysis (45,244 sub-interfaces) provides a useful community resource and reveals potentially interesting trends (e.g., base flipping, connectivity differences between nucleic acid-only and protein–nucleic acid interfaces).
  4. The case studies are well chosen to demonstrate the tool's versatility across experimental and predicted structures of different complex types.

- **Major Concerns**

- **Concern ID** R1-M1
- **Severity** Major
- **Blocking** Yes
- **Axis** Technical validation
- **Claim pointer** "ProNA3D identified 5 sub-interfaces... Increasing the dHA to 4.0 Å reduced this to 2 sub-interfaces, and at 5.0 Å, only a single interface was identified" (hammerhead ribozyme case)
- **Evidence pointer** Section: X-ray structure of an RNA-only complex; Figure 2
- **Concern** The sensitivity of sub-interface detection to the dHA parameter is demonstrated, but there is no validation of whether these sub-interfaces are biologically meaningful or merely artifacts of the clustering algorithm. The manuscript does not compare ProNA3D's sub-interface partitioning against known functional or structural units in these well-characterized complexes. Without such validation, the core feature of the tool (sub-interface identification) remains unsubstantiated.
- **Why it matters** The central claim of the tool is that it can identify meaningful sub-interfaces within larger interfaces. If the sub-interface boundaries are highly sensitive to arbitrary cutoffs and do not correspond to known structural or functional features, the tool's primary output may mislead users.
- **Resolution test** Provide a validation analysis on a set of well-characterized complexes where sub-interfaces are known (e.g., from mutagenesis or evolutionary analysis), showing that ProNA3D's sub-interface detection recovers these known features across a range of dHA values. Alternatively, demonstrate that sub-interface boundaries are stable across small perturbations of the input structure.

- **Concern ID** R1-M2
- **Severity** Major
- **Blocking** Yes
- **Axis** Novelty and comparative assessment
- **Claim pointer** "Tools for the integrated analysis of interfaces within such complexes remain limited" (Abstract); "ProNA3D addresses this gap" (Introduction)
- **Evidence pointer** Introduction; Table S1
- **Concern** The manuscript claims that existing tools are limited, but the comparison in Table S1 (not provided) is not discussed in sufficient detail in the main text. Specifically, the authors do not clearly articulate what ProNA3D offers beyond DNAproDB and RNAproDB, which already provide topology plots and interaction analysis for nucleic acid complexes. The extension from PICKLUSTER is mentioned, but the specific new capabilities (beyond supporting nucleic acids) are not enumerated.
- **Why it matters** For a software tool paper, the novelty and differentiation from existing tools is a primary criterion for publication. Without a clear comparative analysis, readers cannot assess whether ProNAD3D represents a significant advance or an incremental extension.
- **Resolution test** Add a dedicated section or table in the main text that systematically compares ProNA3D's features against DNAproDB, RNAproDB, PICKLUSTER, and other relevant tools (e.g., Arpeggio, NucPlot), with explicit statements of what is new and what is inherited.

- **Concern ID** R1-M3
- **Severity** Major
- **Blocking** No
- **Axis** Statistical rigor of large-scale analysis
- **Claim pointer** "distinct interface connectivity trends and interaction modes characteristic of specific classes of nucleic acid-containing complexes" (Abstract); "protein–DNA and protein–RNA interfaces exhibited higher mean maximum connectivity and broader distributions than nucleic acid-only interfaces" (Systematic analysis section)
- **Evidence pointer** Section: Systematic analysis; Figure 5; Tables S2–S6
- **Concern** The large-scale analysis reports descriptive statistics (medians, standard deviations) and Mann–Whitney U test results, but the effect sizes are not reported, and the biological interpretation of the connectivity differences is limited. The claim of "distinct trends" is not supported by any clustering or classification analysis that would demonstrate that interface types can be distinguished based on connectivity features. Additionally, the analysis of outliers (connectivity ≥ 18) is anecdotal, with only two examples discussed.
- **Why it matters** The large-scale analysis is presented as a key outcome of the tool, but without effect sizes, confidence intervals, or a more rigorous classification framework, the biological conclusions remain weak. The claim of "distinct trends" requires more than statistical significance; it requires demonstration that the distributions are sufficiently different to be informative.
- **Resolution test** Report effect sizes (e.g., Cliff's delta or rank-biserial correlation) for the pairwise comparisons. Add a classification analysis (e.g., random forest or simple threshold-based classifier) showing that interface type can be predicted from connectivity features with reasonable accuracy. Provide a more systematic analysis of high-connectivity outliers, including a functional enrichment analysis.

- **Concern ID** R1-M4
- **Severity** Major
- **Blocking** No
- **Axis** Validation of predicted structure analysis
- **Claim pointer** "interface contact similarity score of 0.875" (Predicted protein–RNA complex section)
- **Evidence pointer** Section: Predicted protein–RNA complex; Figure 3
- **Concern** The comparison between predicted and experimental interfaces relies on a single similarity score, but the metric is not defined in the main text or methods. It is unclear whether this score is based on residue-residue contacts, spatial overlap, or some other measure. Additionally, the significance of a score of 0.875 is not established (i.e., what would a random or poor prediction score?).
- **Why it matters** The ability to analyze predicted structures is a key selling point of ProNA3D. Without a clear definition and benchmark of the similarity metric, the claim that the tool can meaningfully analyze predicted interfaces is not fully supported.
- **Resolution test** Define the interface contact similarity score in the Methods section. Provide a benchmark against a set of decoy or incorrect predictions to establish a baseline for the score. Ideally, compare ProNA3D's assessment of predicted interfaces against other established metrics (e.g., DockQ, lDDT).

- **Minor Comments**

- **Concern ID** R1-m1
- **Severity** Minor
- **Axis** Clarity
- **Affected element** Methods, Interface extraction
- **Evidence pointer** Methods section, Equation 1
- **Issue** The mathematical notation in Equation 1 is ambiguous. The expression "I=rirjmina∈rib∈rjxa,i−xb,j≤dHA" is not standard mathematical notation and is difficult to parse.
- **Required correction** Rewrite Equation 1 using standard set-builder notation, e.g., I = {(ri, rj) | min_{a∈ri, b∈rj} ||x_a,i − x_b,j|| ≤ dHA}.

- **Concern ID** R1-m2
- **Severity** Minor
- **Axis** Reproducibility
- **Affected element** Methods, Dataset curation
- **Evidence pointer** Methods section, Dataset curation for large-scale PDB analysis
- **Issue** The dataset curation is described, but the exact date of the PDB snapshot, the version of the PDB, and the specific filtering criteria (beyond resolution) are not fully specified. The statement "yielding 10,806 complexes" lacks context for reproducibility.
- **Required correction** Specify the PDB release date or version, and provide a more detailed flowchart of the filtering steps (e.g., in a supplementary figure).

- **Concern ID** R1-m3
- **Severity** Minor
- **Axis** Interpretation
- **Affected element** Discussion, Limitations
- **Evidence pointer** Discussion section
- **Concern** The Discussion does not explicitly address the limitation that the connectivity analysis is based on static structures and does not account for conformational dynamics or ensemble representations. Given the emphasis on cryo-EM and flexibility, this is a notable omission.
- **Required correction** Add a paragraph in the Discussion acknowledging this limitation and suggesting potential future directions (e.g., ensemble analysis, integration with molecular dynamics).

- **Concern ID** R1-m4
- **Severity** Minor
- **Axis** Accessibility
- **Affected element** Data Availability
- **Evidence pointer** Data Availability section
- **Issue** The statement "the repository contains the results of the large-scale analyses" is vague. It is unclear what format the results are in, whether they are raw data or processed summaries, and whether they are easily queryable.
- **Required correction** Provide a brief description of the data files (e.g., CSV tables, SQLite database) and their schema in the Data Availability section or a supplementary note.

- **Technical failings that need to be addressed before the case is established**
  R1-M1 (sub-interface validation), R1-M2 (comparative novelty), R1-M3 (statistical rigor of large-scale claims), R1-M4 (definition and benchmarking of similarity metric).

- **Assessment against Nature-style criteria**
  - **Originality**: Moderate. The combination of features (nucleic acid interface analysis + AlphaFold 3 scoring + cryo-EM zoning) in a single plug-in is somewhat novel, but each individual component exists in some form in other tools. The large-scale connectivity analysis is a useful contribution but not conceptually groundbreaking.
  - **Scientific importance**: Moderate to high. The tool addresses a practical need in a growing area (analysis of predicted nucleic acid complexes). The large-scale analysis could be a useful resource, but its biological insights are currently limited.
  - **Interdisciplinary readership**: Moderate. The tool will appeal to structural biologists, computational biologists, and possibly RNA biologists. The cryo-EM integration broadens appeal, but the manuscript is unlikely to attract readers outside these fields.
  - **Technical soundness**: Currently insufficient. The core algorithm (sub-interface detection) lacks validation, the similarity metric is undefined, and the statistical analysis of the large-scale dataset is incomplete. The software design appears sound, but the evidence presented does not fully establish its reliability.
  - **Readability for nonspecialists**: Acceptable. The manuscript is generally well-written and the concepts are explained clearly. However, the Methods section assumes familiarity with structural biology terminology and tools.

- **Recommendation posture** Currently not established from the provided evidence. The tool has clear potential and addresses a real need, but the manuscript requires substantial revisions to validate the core algorithms, clarify novelty, and strengthen the statistical and biological analysis of the large-scale dataset. I would be supportive of reconsideration after major revisions.