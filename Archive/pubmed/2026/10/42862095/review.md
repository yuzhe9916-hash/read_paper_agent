## Review setup
- **Input scope** Abstract only
- **Assessment boundary** Claims and conclusions as presented in the abstract; structural and biochemical evidence referenced but not directly assessable
- **Shared manuscript claim summary** The authors report crystal structures of a CRISPR-associated Nudix hydrolase (LngNH) from *Limisphaera ngatamarikiensis* in apo and ITP-bound forms, and propose a structural basis for ITP-selective hydrolysis that mitigates CAAD-induced toxicity.
- **Visible evidence base** Abstract text only; no figures, tables, methods, or structural coordinates provided
- **Missing materials affecting confidence** Full manuscript, crystallographic statistics, mutagenesis data, kinetic measurements, and structural figures

## Reviewer
- **Overall assessment** The abstract presents a potentially interesting structural study linking a Nudix hydrolase to CRISPR-associated defense systems. The central claim, that LngNH selectively hydrolyzes ITP via a distinct hypoxanthine-binding pocket, is plausible but cannot be evaluated from the abstract alone. The connection to CAAD toxicity mitigation is framed as a functional hypothesis rather than a demonstrated mechanism. The work may appeal to structural biologists and microbiologists studying nucleotide metabolism and CRISPR immunity, but the current evidence base is insufficient to assess technical soundness or the strength of the selectivity claims.

- **Who would be interested in the results, and why** Structural biologists studying Nudix hydrolases and nucleotide sanitization enzymes; microbiologists investigating CRISPR-associated defense mechanisms and self-protection strategies; researchers interested in nucleotide homeostasis during antiviral immunity. The structural framework could inform future engineering or inhibitor design efforts.

- **Major strengths** The study addresses a relatively underexplored intersection of CRISPR biology and nucleotide quality control. The use of crystal structures with catalytic mutants to capture substrate complexes is an appropriate approach. The proposed selectivity mechanism, involving a hydrophobic pocket and hydrogen-bond network for hypoxanthine recognition, is mechanistically coherent and testable.

- **Major Concerns**

  - **Concern ID** R1-M1
  - **Severity** Major
  - **Blocking** Yes
  - **Axis** Evidence sufficiency
  - **Claim pointer** "LngNH mitigates CAAD-induced toxicity by hydrolyzing ITP to IMP and pyrophosphate"
  - **Evidence pointer** Abstract; location not provided
  - **Concern** The abstract states that LngNH mitigates CAAD-induced toxicity, but no functional data (e.g., growth assays, in vivo complementation, or cellular toxicity measurements) are described. The only evidence mentioned is structural and biochemical (crystal structures, mutagenesis). The causal link between ITP hydrolysis and toxicity mitigation is asserted rather than demonstrated.
  - **Why it matters** This is a central functional claim that extends beyond the structural findings. If not supported by direct experimental evidence, the conclusion overreaches the data presented.
  - **Resolution test** Provide in vivo or in vitro functional assays showing that LngNH activity reduces ITP accumulation or rescues CAAD-induced growth defects. Alternatively, revise the claim to state that ITP hydrolysis is consistent with a toxicity-mitigation role, without asserting causality.

  - **Concern ID** R1-M2
  - **Severity** Major
  - **Blocking** Yes
  - **Axis** Selectivity claim support
  - **Claim pointer** "This enzyme specifically recognizes and hydrolyzes ITP while avoiding related cellular nucleotides"
  - **Evidence pointer** Abstract; location not provided
  - **Concern** The abstract claims specificity for ITP over related nucleotides, but no comparative data (e.g., activity against GTP, ATP, XTP, or other NTPs/NDPs) are presented. The structural basis for selectivity is described, but whether this translates to biochemical specificity is not shown.
  - **Why it matters** Selectivity is a core claim of the paper and is central to the proposed biological role. Without quantitative comparison against related substrates, the specificity assertion is unsupported.
  - **Resolution test** Include enzymatic assays with a panel of nucleotide substrates showing relative hydrolysis rates and, if available, kinetic parameters (kcat/Km) for ITP versus related nucleotides.

  - **Concern ID** R1-M3
  - **Severity** Major
  - **Blocking** No
  - **Axis** Structural evidence completeness
  - **Claim pointer** "The hypoxanthine of ITP is deeply buried in a hydrophobic pocket and engages a distinct hydrogen-bond network, whereas the triphosphate tail is coordinated by conserved residues and divalent metal ions"
  - **Evidence pointer** Abstract; location not provided
  - **Concern** The structural description is plausible but cannot be verified without the actual electron density maps, crystallographic refinement statistics, and structural figures. The use of catalytic mutants to trap the substrate complex is mentioned, but the specific mutations and their effects on catalysis versus binding are not described.
  - **Why it matters** The structural claims are the foundation of the paper. Without access to the structural data and validation metrics, the reliability of the proposed binding mode cannot be assessed.
  - **Resolution test** Provide crystallographic tables (resolution, Rfree, geometry), omit maps for the ligand, and structural figures showing the binding pocket and coordination geometry. Describe the catalytic mutants used and confirm that they abolish activity without disrupting fold or substrate binding.

- **Minor Comments**

  - **Concern ID** R1-m1
  - **Severity** Minor
  - **Axis** Clarity
  - **Affected element** Terminology
  - **Evidence pointer** Abstract; "nucleoside diphosphates linked to moiety-X (Nudix)"
  - **Issue** The abstract spells out "nucleoside diphosphates linked to moiety-X" twice, which is redundant and interrupts flow.
  - **Required correction** Define the term once at first mention and use "Nudix" thereafter.

  - **Concern ID** R1-m2
  - **Severity** Minor
  - **Axis** Contextual framing
  - **Affected element** Introduction of CAAD
  - **Evidence pointer** Abstract; "CRISPR-Cas-associated adenosine deaminases (CAAD)"
  - **Issue** The abstract introduces CAAD without explaining what these systems do or why they generate ITP. Readers unfamiliar with this specific system may struggle to follow the rationale.
  - **Required correction** Add one sentence briefly describing CAAD function and the source of ITP generation in the context of antiviral defense.

  - **Concern ID** R1-m3
  - **Severity** Minor
  - **Axis** Generalizability
  - **Affected element** Conclusion scope
  - **Evidence pointer** Abstract; "suggest that CRISPR-associated Nudix hydrolases function as local self-protection modules"
  - **Issue** The generalization from a single enzyme to a class-wide function is speculative, especially without comparative data from other CRISPR-associated Nudix hydrolases.
  - **Required correction** Soften the language to indicate this is a hypothesis arising from the current study, or provide supporting bioinformatic or functional evidence from additional homologs.

- **Technical failings that need to be addressed before the case is established** R1-M1 (toxicity mitigation claim unsupported by functional data), R1-M2 (selectivity claim lacks comparative biochemical data), R1-M3 (structural evidence not assessable from abstract alone)

- **Assessment against Nature-style criteria** Originality: moderate to high, as the intersection of CRISPR immunity and Nudix-mediated nucleotide sanitation is relatively novel. Scientific importance: moderate, as the findings may illuminate self-protection mechanisms in CRISPR systems, but the broader significance depends on whether this is a general phenomenon or a niche case. Interdisciplinary readership: the topic bridges structural biology, microbiology, and immunology, but the abstract may not fully convey the broader relevance to nonspecialists. Technical soundness: not assessable from the abstract; requires full structural and biochemical data. Readability for nonspecialists: the abstract is reasonably accessible but assumes familiarity with CRISPR-associated systems and nucleotide metabolism; the IMPORTANCE section helps contextualize the work.

## Risk / unsupported claims
- The claim that LngNH "mitigates CAAD-induced toxicity" is not supported by any functional evidence described in the abstract.
- The claim of specificity for ITP "while avoiding related cellular nucleotides" is not supported by comparative biochemical data.
- The generalization to "CRISPR-associated Nudix hydrolases" as a class is speculative based on a single enzyme.
- The structural basis for selectivity cannot be evaluated without access to crystallographic data and figures.