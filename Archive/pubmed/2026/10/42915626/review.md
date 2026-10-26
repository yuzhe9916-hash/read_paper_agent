## Review setup
- **Input scope** Abstract only
- **Assessment boundary** Claims and conclusions as stated in the abstract; no methods, figures, or data tables were provided for verification
- **Shared manuscript claim summary** The authors report a structure-aware deep learning-guided engineering approach to generate a tunable CcdB variant (CcdB_L96P) with reduced basal toxicity and retained inducible lethality, demonstrated across multiple E. coli strains, in antibiotic-free CRISPR gRNA plasmid construction, and in a succinic acid-producing chassis without detectable metabolic burden
- **Visible evidence base** Abstract text only; no experimental details, statistical analyses, or supplementary information were accessible
- **Missing materials affecting confidence** Full methods, all figures and tables, strain list, induction conditions, quantitative toxicity and killing data, metabolic burden measurements, and any computational model details

## Reviewer
- **Overall assessment** The abstract presents a conceptually interesting application of deep learning-guided protein engineering to tune a toxic counter-selection marker, which could be of practical value in synthetic biology. However, the current evidence base is limited to the abstract alone, and several quantitative claims (e.g., "minimal leakage," "no detectable metabolic burden," "high accuracy") cannot be assessed without underlying data. The core concept is plausible, but the strength of the conclusions cannot be verified from the supplied material.

- **Who would be interested in the results, and why** Researchers in synthetic biology, genetic circuit design, and metabolic engineering would be interested, particularly those working on counter-selection systems, antibiotic-free plasmid maintenance, and CRISPR-based genome editing. The potential for a tunable toxin variant with low basal toxicity could simplify cloning workflows and enable tighter control of cell killing in industrial chassis.

- **Major strengths** 
  - The problem addressed is practically relevant: wild-type CcdB toxicity limits its utility, and a tunable variant would be broadly useful
  - The use of structure-aware deep learning to prioritize mutations is a modern and potentially generalizable approach
  - The demonstration across multiple E. coli strains and in a metabolic engineering context suggests potential for broad applicability
  - The antibiotic-free selection application addresses a real need in plasmid construction

- **Major Concerns**

- **Concern ID** R1-M1
- **Severity** Major
- **Blocking** Yes
- **Axis** Evidence sufficiency
- **Claim pointer** "CcdB_L96P significantly reduces basal toxicity while preserving effective killing upon induction"
- **Evidence pointer** Abstract only; no quantitative data provided
- **Concern** The central claim of reduced basal toxicity and retained inducible lethality is stated without any quantitative metrics. No data are shown for toxicity levels, killing efficiency, induction kinetics, or comparison to wild-type CcdB.
- **Why it matters** This is the foundational claim of the paper. Without quantitative evidence, the reader cannot judge whether the improvement is meaningful or merely marginal.
- **Resolution test** Provide dose-response curves for basal toxicity and induced killing, with statistical comparisons to wild-type CcdB across the tested strains.

- **Concern ID** R1-M2
- **Severity** Major
- **Blocking** Yes
- **Axis** Generalizability
- **Claim pointer** "This variant exhibits minimal leakage and robust inducible lethality across multiple Escherichia coli strains without requiring specialized hosts"
- **Evidence pointer** Abstract only; strain names and numbers not specified
- **Concern** The claim of "minimal leakage" and "robust" performance across multiple strains is not supported by any strain-specific data. The number and identity of strains, the variability in performance, and the criteria for "minimal" and "robust" are undefined.
- **Why it matters** Generalizability across strains is a key selling point for a counter-selection tool. Without strain-level data, the claim is unverifiable.
- **Resolution test** Provide a table or figure showing basal toxicity and induced killing for each strain tested, with appropriate controls and statistical analysis.

- **Concern ID** R1-M3
- **Severity** Major
- **Blocking** Yes
- **Axis** Application validation
- **Claim pointer** "It enables antibiotic-free CRISPR gRNA plasmid construction with high accuracy and efficient enrichment of correctly assembled clones"
- **Evidence pointer** Abstract only; no cloning efficiency or accuracy data provided
- **Concern** The application claim is central to the paper's practical value, but no data are shown for cloning accuracy, enrichment efficiency, or comparison to standard methods.
- **Why it matters** If the variant does not perform well in a real application, its utility is questionable regardless of in vitro characterization.
- **Resolution test** Provide quantitative comparison of cloning accuracy and colony recovery with and without the CcdB_L96P-based selection, ideally against a standard antibiotic-based method.

- **Concern ID** R1-M4
- **Severity** Major
- **Blocking** Yes
- **Axis** Metabolic burden assessment
- **Claim pointer** "In a succinic acid-producing chassis, CcdB_L96P imposes no detectable metabolic burden and supports effective removal of residual cells using low concentrations of anhydrotetracycline"
- **Evidence pointer** Abstract only; no growth, yield, or killing data provided
- **Concern** The claim of "no detectable metabolic burden" is a strong negative claim that requires sensitive assays and appropriate controls. The "effective removal" of residual cells is also not quantified.
- **Why it matters** Metabolic burden is a common concern with toxin-antitoxin systems in production strains. A negative claim requires robust evidence.
- **Resolution test** Provide growth curves, product yield data, and cell viability counts with statistical comparison to a control strain without the CcdB variant.

- **Minor Comments**

- **Concern ID** R1-m1
- **Severity** Minor
- **Axis** Clarity
- **Affected element** "structure-aware deep learning-guided strategy"
- **Evidence pointer** Abstract
- **Issue** The description of the computational approach is vague. It is unclear what specific deep learning architecture was used, what training data were employed, and how "structure-aware" was operationalized.
- **Required correction** Provide a brief description of the computational method in the abstract or ensure the main text clearly details the model architecture, training data, and prediction criteria.

- **Concern ID** R1-m2
- **Severity** Minor
- **Axis** Reproducibility
- **Affected element** "low concentrations of anhydrotetracycline"
- **Evidence pointer** Abstract
- **Issue** The concentration range is not specified, making it difficult to assess practicality or compare with other inducible systems.
- **Required correction** Specify the concentration range used and, if possible, the induction time and temperature.

- **Concern ID** R1-m3
- **Severity** Minor
- **Axis** Terminology
- **Affected element** "tunable CcdB variant"
- **Evidence pointer** Abstract
- **Issue** The term "tunable" implies a range of adjustable activities, but the abstract only describes a single variant (CcdB_L96P). It is unclear whether multiple variants with graded activities were generated.
- **Required correction** Clarify whether multiple variants were characterized or whether "tunable" refers to the inducible nature of the system rather than a range of basal activities.

- **Concern ID** R1-m4
- **Severity** Minor
- **Axis** Completeness
- **Affected element** "generalizable protein-level strategy"
- **Evidence pointer** Abstract
- **Issue** The claim of generalizability is made without evidence that the approach was applied to other toxins or systems.
- **Required correction** Either temper the claim to reflect that it is a proof-of-concept for CcdB, or provide evidence of application to at least one other toxin.

## Risk / unsupported claims
- "Significantly reduces basal toxicity" is unsupported without quantitative data
- "Minimal leakage" is unsupported without defined thresholds or comparative data
- "No detectable metabolic burden" is a strong negative claim that cannot be assessed from the abstract
- "High accuracy" in CRISPR gRNA plasmid construction is unquantified
- "Generalizable protein-level strategy" is an extrapolation from a single example
- The deep learning-guided approach is described but its contribution to the outcome cannot be evaluated without model details and ablation or comparison to non-guided approaches