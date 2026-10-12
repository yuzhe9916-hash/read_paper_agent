## Review setup
- **Input scope** Abstract only
- **Assessment boundary** Claims and evidence as presented in the abstract; no figures, methods, or data tables were available for inspection
- **Shared manuscript claim summary** The authors report a Cas12a-based biosensor (CDMS) for DNA methyltransferase (MTase) detection, using a branched split-activator design with steric hindrance to suppress nonspecific activation. They report detection limits of 1.06 × 10⁻⁶ U/mL for M.SssI and 7.41 × 10⁻⁸ U/mL for Dam MTase, specificity for inhibitor screening, and a portable device (iCas-Analyzer) for point-of-care testing.
- **Visible evidence base** Abstract text only; no experimental sections, figures, tables, or supplementary information provided
- **Missing materials affecting confidence** Full methods, all figures and tables, characterization data (e.g., gel images, fluorescence curves), specificity and inhibition data, device validation data, and statistical analyses

## Reviewer
- **Overall assessment** The abstract presents a conceptually interesting approach that combines structural control of Cas12a activation with MTase detection, potentially addressing background-signal issues in existing CRISPR-based biosensors. The reported detection limits are impressive if reproducible. However, the abstract alone provides insufficient experimental detail to evaluate the robustness of the design, the validity of the analytical performance claims, or the practical utility of the device. The core mechanism is described at a conceptual level, and key control experiments are not visible. The work is potentially of interest to the biosensing and epigenetics communities, but the case is not established from the supplied material.
- **Who would be interested in the results, and why** Researchers in CRISPR-based diagnostics, epigenetic enzyme sensing, and point-of-care device development would find this work relevant. The steric-hindrance-based split-activator design could offer a generalizable strategy for reducing background in Cas12a systems, and the MTase detection application addresses a gap in CRISPR-based epigenetics assays. The portable device component may appeal to those working on decentralized diagnostics.
- **Major strengths** The conceptual design of using a branched split activator with steric hindrance to gate Cas12a activity is creative and addresses a known limitation of CRISPR-based sensors, namely uncontrolled background activation. The reported detection limits are notably low and, if confirmed, would represent a meaningful advance. The inclusion of a portable device for POCT suggests attention to translational applicability.
- **Major Concerns**

- **Concern ID** R1-M1
- **Severity** Major
- **Blocking** Yes
- **Axis** Technical soundness
- **Claim pointer** The branched split structure "significantly inhibits nonspecific Cas12a activation while efficiently restoring its activity upon removal of steric hindrance in response to DNA MTase activity."
- **Evidence pointer** Abstract only; no figures or methods provided
- **Concern** The abstract claims that the split-and-reconstituted design suppresses nonspecific activation and restores activity upon MTase-mediated steric-hindrance removal, but no experimental evidence is shown to support this mechanism. Key questions include: how is the steric hindrance introduced and removed; what is the kinetic profile of activation; and what are the background signals in the absence of MTase? Without these data, the central mechanistic claim is unverifiable.
- **Why it matters** The entire analytical performance of the sensor depends on the dynamic range between suppressed background and MTase-triggered activation. If the background suppression is incomplete or the activation efficiency is low, the reported detection limits would not be achievable. This is the foundational claim of the work.
- **Resolution test** Provide gel or fluorescence data showing Cas12a cleavage activity in the presence and absence of MTase, with and without the branched split structure, including quantitative background-to-signal ratios and time-course experiments.

- **Concern ID** R1-M2
- **Severity** Major
- **Blocking** Yes
- **Axis** Technical soundness
- **Claim pointer** "Ultra-low detection limit of 1.06 × 10⁻⁶ U/mL for M.SssI MTase and 7.41 × 10⁻⁸ U/mL for Dam MTase"
- **Evidence pointer** Abstract only; no calibration curves or statistical methods provided
- **Concern** The detection limits are reported without any supporting calibration data, definition of how the limit of detection (LOD) was calculated, or information on the number of replicates and error analysis. The values are exceptionally low, and without standard curves, blank measurements, and signal-to-noise calculations, these numbers cannot be assessed.
- **Why it matters** Detection limit is the primary quantitative claim of the paper. If the LOD calculation method is nonstandard or the blank variability is underestimated, the reported values could be misleading. Reproducibility of such low detection limits is a common challenge in biosensor literature.
- **Resolution test** Provide calibration curves with error bars, a clear definition of LOD (e.g., 3σ/slope method), the number of independent replicates, and raw fluorescence data for blank and near-LOD concentrations.

- **Concern ID** R1-M3
- **Severity** Major
- **Blocking** Yes
- **Axis** Technical soundness
- **Claim pointer** "Exhibiting excellent specificity and robust applicability for MTase inhibitor screening"
- **Evidence pointer** Abstract only; no specificity or inhibition data provided
- **Concern** The abstract claims specificity and inhibitor-screening capability, but no data are shown for selectivity against other MTases or non-MTase enzymes, nor for inhibitor dose-response experiments. The choice of inhibitor, the range of concentrations tested, and the assay format for screening are not described.
- **Why it matters** Specificity is critical for any biosensor claiming bioanalytical utility, and inhibitor screening is a stated application. Without evidence that the sensor distinguishes among MTases and responds to inhibitors in a dose-dependent manner, these claims are unsupported.
- **Resolution test** Provide specificity data against a panel of related and unrelated enzymes, and inhibitor titration curves with calculated IC₅₀ values compared to known values from literature.

- **Concern ID** R1-M4
- **Severity** Major
- **Blocking** No
- **Axis** Reproducibility and robustness
- **Claim pointer** "A palm-sized portable optical device, named iCas-Analyzer, to further explore the CDMS's potential for point-of-care testing (POCT), which can be easily operated by nonexpert end users"
- **Evidence pointer** Abstract only; no device description, images, or user studies provided
- **Concern** The portable device is mentioned as a significant component, but no technical details are given regarding its optical components, readout mechanism, limit of detection in the device format, or validation with clinical or real-world samples. The claim that it can be operated by nonexpert users is not supported by any usability data.
- **Why it matters** The POCT claim is a major part of the translational significance. Without device characterization and comparison to benchtop results, the practical utility remains speculative.
- **Resolution test** Provide device schematics, optical path description, side-by-side comparison of device vs. benchtop detection limits, and a small user study with nonexpert operators showing consistent results.

- **Minor Comments**

- **Concern ID** R1-m1
- **Severity** Minor
- **Axis** Clarity
- **Affected element** Terminology
- **Evidence pointer** Abstract, title
- **Issue** The term "Branched Split Activator-Regulated" in the title is not defined in the abstract. The relationship between "branched" and "split" is unclear, and the structural details of the activator are not described.
- **Required correction** Define the branched split activator structure in the abstract, or adjust the title to reflect the actual design more clearly.

- **Concern ID** R1-m2
- **Severity** Minor
- **Axis** Completeness
- **Affected element** Comparison to existing methods
- **Evidence pointer** Abstract, first paragraph
- **Issue** The abstract states that existing methods are "laboratory-bound" and "time-consuming," and that emerging approaches "depend on complex enzymatic amplifications or suffer from uncontrolled background signals," but no specific prior methods are cited or compared quantitatively.
- **Required correction** Add brief quantitative comparison to at least one or two representative existing methods, including detection limits and assay time, to contextualize the claimed advantages.

- **Concern ID** R1-m3
- **Severity** Minor
- **Axis** Reproducibility
- **Affected element** Units and precision
- **Evidence pointer** Abstract, detection limit values
- **Issue** The detection limits are reported to three significant figures (1.06 × 10⁻⁶ and 7.41 × 10⁻⁸). This level of precision is unusual for biosensor LODs and suggests either a very stable assay or over-reporting of precision.
- **Required correction** Report LODs with appropriate significant figures based on the variability of blank measurements, and state the number of replicates used.

- **Concern ID** R1-m4
- **Severity** Minor
- **Axis** Scope
- **Affected element** Generalizability claim
- **Evidence pointer** Abstract, final sentence
- **Issue** The abstract claims the sensor "extends CRISPR-based diagnostics into the field of epigenetics," which is a broad claim given that only two MTases are demonstrated.
- **Required correction** Soften the claim to reflect the demonstrated scope, e.g., "demonstrates the potential of CRISPR-based diagnostics for epigenetic enzyme detection."

## Risk / unsupported claims
- The central mechanism of steric-hindrance-controlled Cas12a activation is described but not experimentally supported in the provided material.
- The reported detection limits are unsupported by calibration data, LOD calculation methods, or replicate information.
- Specificity and inhibitor-screening claims are made without any selectivity or dose-response data.
- The portable device (iCas-Analyzer) is claimed to be functional and user-friendly, but no device characterization or usability data are provided.
- The general claim of extending CRISPR diagnostics into epigenetics is broader than what the demonstrated scope supports.
- The abstract implies clinical or precision-medicine relevance, but no clinical samples or real-world validation are mentioned.