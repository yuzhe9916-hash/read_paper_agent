## Review setup
- **Input scope** Full manuscript text (abstract, introduction, structural basis, structure-empowerment strategies, applications, outlook, conclusion). Figures and tables referenced but not supplied as visual content.
- **Assessment boundary** Assessment is limited to the supplied text. No figure panels, table data, supplementary information, or reference list were provided, so quantitative claims, figure-dependent claims, and citation-dependent claims cannot be independently verified.
- **Shared manuscript claim summary** The manuscript is a review arguing that G-quadruplex (G4) aptamer biosensing performance is governed by higher-order structure rather than sequence-level affinity alone. It proposes a "structural empowerment" framework linking topology, conformational energetics, folding kinetics, loop and terminal organization, ion coordination, and nano-interfacial coupling to analytical outputs, and it claims to establish a quantitative structure-performance framework correlating G4 structural descriptors with sensing metrics across fluorescence, colorimetric, SERS, and electrochemical platforms.
- **Visible evidence base** Narrative synthesis of cited literature, conceptual schematics described in text (Figure 1A/B, Figure 2A/B, Figure 3, Figure 4), and two summary tables (Table 1, Table 2, Table 3 referenced). No primary data, no meta-analysis, no systematic search protocol, no extracted numerical dataset.
- **Missing materials affecting confidence** Figure panels and captions; Table 1 to Table 3 contents; reference list; any supplementary methods describing literature selection; any quantitative compilation underlying the claimed "quantitative structure-performance framework."

## Reviewer
- **Overall assessment** This is a broadly conceived and well-organized review that advances a coherent conceptual thesis, namely that G4 aptamer sensing is structure-governed rather than affinity-governed. The narrative arc from structural fundamentals to empowerment strategies to modality-specific applications is logical, and the repeated emphasis on kinetics, conformational ensembles, and matrix effects is a genuine improvement over stability-centric reviews. However, the manuscript's central and most distinctive claim, that it establishes a quantitative structure-performance framework, is not substantiated by the supplied text. The text is predominantly qualitative and programmatic, with quantitative content appearing as isolated literature values rather than as an integrated, testable framework. Several mechanistic statements are asserted without the supporting figure or table content needed to evaluate them. The review is therefore valuable as a conceptual synthesis but currently overstates its quantitative and predictive contribution.
- **Who would be interested in the results, and why** Researchers in functional nucleic acid chemistry, aptasensor development, DNA nanotechnology, and bioanalytical chemistry, particularly those working on G4-hemin DNAzymes, CRISPR-coupled nucleic acid reporters, and nanointerface-based sensing. Also relevant to groups interested in conformational energy landscape descriptions of nucleic acids and to those translating aptasensors into serum, food, or environmental matrices.
- **Major strengths** The manuscript articulates a clear and defensible conceptual position, that G4 structure actively shapes signal generation rather than serving as a passive scaffold, and it sustains this position consistently across sections. The treatment of kinetics alongside thermodynamics, including the distinction between k_on and k_off contributions to signal behavior, is a substantive and useful framing. The repeated and specific attention to matrix translation, including nuclease degradation, Na+/K+ competition, nonspecific protein adsorption, and interfacial fouling, is a strength that many reviews in this area omit. The organization by signal modality with a unifying mechanistic section is effective, and the writing is generally clear and readable.
- **Major Concerns**
  - **Concern ID** R1-M1
  - **Severity** Major
  - **Blocking** Yes
  - **Axis** Claim-evidence alignment
  - **Claim pointer** The review "establishes a quantitative structure-performance framework by correlating G4 structural descriptors, conformational energetics, kinetic parameters, and analytical outputs," providing a basis for predictive design.
  - **Evidence pointer** Abstract; Section "Quantitative Structural Descriptors Governing G4 Activity and Sensing Performance"; Section "General Principles of G-Quadruplex-Enabled Sensing System"; location not provided for any supporting dataset or table.
  - **Concern** The supplied text does not contain a quantitative framework in any operational sense. No descriptor set is defined with units or measurement conventions, no correlation is reported with a coefficient or fit, no dataset is compiled across studies, and no predictive model or validation is presented. The descriptors listed (loop length, G-tract organization, terminal G-tetrad accessibility, groove geometry, SASA, electrostatic surface distribution, folding kinetics) are enumerated but not linked numerically to LOD, linear range, response time, or background level. The claim of a quantitative framework is therefore asserted rather than demonstrated.
  - **Why it matters** This is the manuscript's principal novelty claim and the basis for its stated contribution to predictive design. If the framework is conceptual rather than quantitative, the abstract, introduction, and conclusion must be revised to reflect that, since the current wording will lead readers to expect a transferable quantitative model.
  - **Resolution test** Either provide an explicit descriptor table with defined metrics and units, a compiled cross-study dataset with reported correlations, and at least one worked predictive example, or revise all framework claims from "quantitative" to "conceptual" or "descriptor-based" throughout the abstract, introduction, and conclusion.

  - **Concern ID** R1-M2
  - **Severity** Major
  - **Blocking** Yes
  - **Axis** Evidence sufficiency for mechanistic claims
  - **Claim pointer** Under K+ conditions, conformational transitions follow ordered pathways through intermediates I1 to I4 and transition states T1 to T4, with associated energy barriers of 0.70 and 1.13 kcal/mol, whereas Na+ produces a more dispersed energy distribution with lower or irregular barriers.
  - **Evidence pointer** Section "Molecular Construction and Topological Diversity," Figure 1A and Figure 1B; figure content not provided.
  - **Concern** These are specific quantitative mechanistic assertions attributed to figure panels that were not supplied. The origin of the barrier values is unclear, whether from molecular dynamics, metadynamics, or another method, and the intermediate and transition state nomenclature is not defined in the text. The comparison between K+ and Na+ landscapes is central to the manuscript's argument that ions reshape the conformational landscape rather than merely stabilize it, yet it cannot be evaluated from the supplied material.
  - **Why it matters** The ion-dependent landscape argument underpins the subsequent sections on ion regulation and on matrix-related Na+/K+ competition. If the underlying evidence is a single simulation study or a schematic, the strength of the claim must be calibrated accordingly.
  - **Resolution test** Provide the figure panels with captions, state the computational or experimental method generating the barrier values, define I1 to I4 and T1 to T4, and specify whether the values derive from a single cited study or from the authors' own analysis.

  - **Concern ID** R1-M3
  - **Severity** Major
  - **Blocking** No
  - **Axis** Reproducibility of literature synthesis
  - **Claim pointer** The review synthesizes recent advances across fluorescence, colorimetric, SERS, and electrochemical G4 sensing and summarizes representative systems in Tables 1 to 3.
  - **Evidence pointer** Section "Applications of G-Quadruplex Aptamers in Analytical Detection"; Table 1, Table 2, Table 3; table contents not provided.
  - **Concern** No literature selection strategy is described. There is no statement of search scope, time window, inclusion or exclusion criteria, or how representative systems were chosen. For a review that positions itself as establishing structure-performance relationships, the absence of a transparent selection protocol limits reproducibility and raises the possibility of selective citation. The tables, which would carry the comparative burden, were not supplied.
  - **Why it matters** Without a described selection method, readers cannot judge whether the reported trends reflect the field or the authors' sampling. This directly affects the credibility of any generalization drawn across modalities.
  - **Resolution test** Add a brief methods paragraph specifying databases, search terms, time range, and inclusion criteria, and provide the full tables with the performance metrics used to support cross-system comparisons.

  - **Concern ID** R1-M4
  - **Severity** Major
  - **Blocking** No
  - **Axis** Internal consistency
  - **Claim pointer** The manuscript states that structural stability does not directly correspond to sensing performance and that an optimal balance between rigidity and dynamic accessibility is required, while elsewhere treating increased terminal G-tetrad exposure and enhanced rigidity as generally favorable for hemin catalysis and dye stacking.
  - **Evidence pointer** Section "Quantitative Structural Descriptors Governing G4 Activity and Sensing Performance"; Section "Ion and Cofactor Regulation"; Section "Nanointerfaces and Confinement Engineering."
  - **Concern** The text oscillates between a nuanced position, that performance depends on a balance and on kinetics, and a simpler position, that greater exposure, rigidity, or confinement improves output. For example, nanointerface confinement is described as suppressing nonproductive folding and increasing residence time of target-sensing topologies, but also as potentially restricting the conformational switching that many sensing schemes require. The conditions under which confinement helps versus hinders are not specified.
  - **Why it matters** The review's practical value depends on giving design guidance that is conditional rather than uniformly directional. As written, a reader could extract contradictory design rules.
  - **Resolution test** Add explicit conditional statements identifying the sensing modalities and target classes for which rigidity, exposure, or confinement is beneficial versus detrimental, ideally with at least one contrasting example for each direction.

  - **Concern ID** R1-M5
  - **Severity** Major
  - **Blocking** No
  - **Axis** Scope and completeness
  - **Claim pointer** The abstract states that the review covers fluorescence, electrochemical, colorimetric, SERS, photoelectrochemical, and catalytic sensing systems.
  - **Evidence pointer** Abstract; Section "Applications of G-Quadruplex Aptamers in Analytical Detection," which contains subsections for fluorescence and colorimetric, SERS, and electrochemical only.
  - **Concern** Photoelectrochemical sensing is listed in the abstract but no corresponding section or substantive discussion appears in the supplied body text. Catalytic sensing is treated within colorimetric and electrochemical contexts rather than as a distinct modality. This is a mismatch between the stated scope and the delivered content.
  - **Why it matters** Abstract scope statements guide reader expectations and indexing. An unfulfilled modality listing weakens the manuscript's completeness claim.
  - **Resolution test** Either add a photoelectrochemical subsection with comparable depth to the other modalities, or remove photoelectrochemical from the abstract and adjust the scope statement.

- **Minor Comments**
  - **Concern ID** R1-m1
  - **Severity** Minor
  - **Axis** Terminology
  - **Affected element** "Structural empowerment" as a defined concept
  - **Evidence pointer** Section "Structural Empowerment: From Structure to Function"
  - **Issue** The term is defined once but is used throughout as though it were an established framework concept. It overlaps substantially with existing concepts such as conformational preorganization, energy landscape engineering, and structure-based design, and the manuscript does not clarify what the new term adds beyond relabeling.
  - **Required correction** Add a short statement distinguishing "structural empowerment" from adjacent established terms, or adopt an existing term consistently.

  - **Concern ID** R1-m2
  - **Severity** Minor
  - **Axis** Precision of quantitative statements
  - **Affected element** Reported performance figures
  - **Evidence pointer** Section "Ion and Cofactor Regulation," statement that detection limits reach fM or even aM; Section "Catalytic Amplification via Nano-Interface Coupling," approximately 11-fold improvement
  - **Issue** Numerical values are reported without specifying the analyte, platform, or measurement conditions, and without citation anchors in the supplied text.
  - **Required correction** Attach each numerical claim to a specific cited system and state the analyte and detection format.

  - **Concern ID** R1-m3
  - **Severity** Minor
  - **Axis** Figure dependence
  - **Affected element** Figure callouts
  - **Evidence pointer** Figure 1A, Figure 1B, Figure 2A, Figure 2B, Figure 3, Figure 4
  - **Issue** Multiple mechanistic arguments depend on figure content that is not described in sufficient standalone detail. Several callouts are grammatically incomplete, for example "As shown in Figure 2A In such systems" and "As shown in Figure 3, G-quadruplexes are no longer isolated catalytic units."
  - **Required correction** Ensure each figure is self-explanatory from its caption and that in-text callouts form complete sentences.

  - **Concern ID** R1-m4
  - **Severity** Minor
  - **Axis** Editorial quality
  - **Affected element** Section numbering and cross-references
  - **Evidence pointer** Introduction, "Scope and Objectives of This Review," and multiple later sections
  - **Issue** Section cross-references appear as blank placeholders, for example "Section  ," "Section  ," and "Section  ." Reference callouts similarly appear as bare commas, for example "Nucleic acid aptamers ,  have emerged" and "G4 aptamers ,  have attracted growing attention."
  - **Required correction** Restore all section numbers and citation markers before resubmission.

  - **Concern ID** R1-m5
  - **Severity** Minor
  - **Axis** Structural logic
  - **Affected element** Section "Structure-Activity Relationships: From Affinity to Energy Landscape"
  - **Evidence pointer** Same section, paragraph beginning "Accordingly, G4 SAR should not be evaluated solely by equilibrium affinity."
  - **Issue** The paragraph contains a duplicated argument, stating twice that SAR should not rest on equilibrium affinity alone, and the sentence "Instead, the same apparent K d may correspond to different sensing behaviors" follows a "Therefore" clause that does not logically connect to it.
  - **Required correction** Consolidate the repeated argument and repair the logical connective.

  - **Concern ID** R1-m6
  - **Severity** Minor
  - **Axis** Claim calibration
  - **Affected element** Statements about AI-assisted design
  - **Evidence pointer** Section "Emerging Integration and Outlook"
  - **Issue** The manuscript states that recent models enable prediction of folding propensity, topology, and stability from spectral and sequence features, and that AI-assisted design may enable predictive modeling of G4 folding landscapes. The first is a present-tense capability claim, the second a future possibility, and the boundary between them is not marked.
  - **Required correction** Separate demonstrated capabilities from proposed directions and cite specific models for the former.

- **Technical failings that need to be addressed before the case is established** R1-M1 (quantitative framework claim unsupported), R1-M2 (figure-dependent mechanistic values unverifiable), R1-M3 (no literature selection protocol), R1-M5 (abstract scope exceeds delivered content). R1-M4 requires conditional clarification but is not blocking.
- **Assessment against Nature-style criteria** Originality is moderate. The organizing thesis, that G4 structure actively governs sensing behavior, is a reasonable and increasingly held position, but the specific framing as "structural empowerment" is largely a relabeling of conformational preorganization and energy landscape engineering rather than a new conceptual advance. Scientific importance is potentially high if the quantitative framework were delivered, since predictive structure-performance relationships for G4 sensors would be genuinely useful, but the supplied text delivers a qualitative synthesis and therefore falls short of the stated importance. Interdisciplinary readership is plausible, spanning analytical chemistry, nucleic acid biophysics, and materials science, though the manuscript is written primarily for the aptasensor community and does not strongly reach outward. Technical soundness is uneven. The conceptual reasoning is generally careful, particularly on kinetics and matrix effects, but the central quantitative claim is unsupported, key mechanistic values depend on unavailable figures, and the literature synthesis lacks a stated protocol. Readability for nonspecialists is fair. The prose is clear and the structure is easy to follow, but the density of undefined abbreviations and the reliance on figure content that is not self-describing in the text will impede readers outside the field.
- **Recommendation posture** Supportive of the conceptual direction, but the manuscript's central quantitative claim is currently not established from the provided evidence. Major revision is required, specifically either delivering the quantitative framework or recalibrating all framework claims, together with provision of figure and table content and a literature selection protocol.

## Risk / unsupported claims
- The claim that the review "establishes a quantitative structure-performance framework" is unsupported. No descriptor definitions with units, no compiled dataset, no correlation statistics, and no predictive validation are present in the supplied text. Status, unsupported as stated.
- The claim that the review provides "a basis for predictive design of G4-based sensing systems" is unsupported. No predictive model, training set, or test case is presented. Status, unsupported as stated.
- The specific energy barrier values of 0.70 and 1.13 kcal/mol and the I1 to I4 and T1 to T4 state assignments are not evaluable, since the originating figure and method are not provided. Status, not evaluable.
- The claim that the review covers photoelectrochemical sensing is unsupported by the supplied body text, which contains no photoelectrochemical section. Status, unsupported as stated.
- The claim that detection limits reach the fM or aM level is weakly supported, since no specific systems, analytes, or citations are attached in the supplied text. Status, weak.
- The claim of an approximately 11-fold catalytic improvement in pesticide detection is weakly supported, since the system, analyte, and measurement conditions are not specified. Status, weak.
- The claim that recent models enable prediction of G4 folding propensity, topology, and stability from spectral and sequence features is weakly supported, since no specific models are cited in the supplied text. Status, weak.
- The claim that nanointerface confinement increases the residence time of target-sensing topologies is plausible but not evaluable, since no supporting data or citations are provided in the supplied text. Status, not evaluable.