# Research Protocol Outline (v0.1)
**PhD in Deep Tech · UNMSM · Session 3 · Juseph Montesinos Asmat**

## 01 · Title
An advisory digital twin for energy-and-capacity optimization in mid-sized Peruvian data centers with limited telemetry: the INSUR pilot case.

## 02 · Abstract
Mid-sized data centers in emerging economies face rising energy costs and capacity risks but lack the comprehensive sensor instrumentation (DCIM) required by state-of-the-art autonomous digital twins. Grounded in pragmatism and Design Science Research (DSR), this doctoral project designs, builds, and evaluates an advisory (human-in-the-loop) digital twin for INSUR, a regulated Peruvian insurer operating with sparse component-level telemetry (XClarity, VMware, Spectrum Control, managed PDUs, and in-row cooling). Prior to assessing decision utility, model validity and estimation uncertainty are verified on chronologically sealed historical blocks without data leakage. Decision utility is then evaluated through the Framework for Evaluation in Design Science (FEDS) using an Interrupted Time Series (ITS) design normalized for ambient temperature and IT load across two metrics: Power Usage Effectiveness (PUE) and IT energy proportionality. Cross-site re-validation at a second institution (Policlínico Peruano Japonés) abstracts transferable design principles (exaptation) for resource-constrained data centers under Peru's regulatory framework (Law N° 29733 and Law N° 31814).

## 03 · Introduction & Problem Statement ("So What?" Test)
* **The Empirical Gap:** Global data center electricity consumption exceeds 130 GW and Gartner projects it to triple by 2030 driven by AI workloads; meanwhile, Peru lags regionally with only 14 registered data centers. Mid-sized Peruvian facilities operate without DCIM software or dense environmental sensors, whereas scientific literature assumes full telemetry.
* **Why Care ("So What?"):** Energy inefficiency and capacity bottlenecks are the primary operational constraints for regulated mid-sized sites like INSUR. Designing a validated advisory twin that operates strictly on existing component logs provides an immediately deployable optimization pathway without requiring upfront capital expenditure in new sensors.

## 04 · Literature Review Axes
1. **Digital Twins in Data Centers:** Advisory (human-in-the-loop decision support) vs. autonomous closed-loop control (incompatible with high-compliance financial/healthcare sites).
2. **Design Science Methodology:** Relevance, design, and rigor cycles (Hevner et al., 2004; Peffers et al., 2007) and knowledge contribution taxonomy—specifically *exaptation* (Gregor & Hevner, 2013).
3. **Evaluation & Metrics:** FEDS naturalistic summative evaluation (Venable et al., 2016), PUE (infrastructure efficiency), and Energy Proportionality (useful compute/storage work per unit of energy).

## 05 · Research Question & SMART Objectives
* **Research Question:** How can an advisory (non-closed-loop) digital twin for decision support and energy-and-capacity optimization be designed for a Peruvian data center with limited telemetry (the INSUR case), and how can it be evaluated—both its validity as a model and its utility for decisions as improving operational decisions over manual management—such that its design principles are transferable to other sites?
* **General Objective:** To design, build, and naturalistically evaluate an advisory digital twin for energy and capacity optimization in mid-sized data centers with sparse telemetry, abstracting transferable design principles.
* **Specific Objectives (SMART — Doran, 1981):**
  1. **SO1 (Build & Model Validity — Months 7–16, Lead: Doctoral Candidate):** Construct a leak-free advisory digital twin artifact synthesizing 5 sparse telemetry streams (XClarity, VMware, Spectrum Control, PDUs, in-row cooling) and validate its predictive accuracy and 95% uncertainty calibration against held-out historical periods at INSUR.
  2. **SO2 (Decision Utility — Months 17–26, Lead: Doctoral Candidate + INSUR Ops Team):** Evaluate the artifact's operational decision utility at INSUR over a 6-month naturalistic Interrupted Time Series (ITS) intervention, measuring statistically significant improvements in weather/load-normalized PUE and energy proportionality compared to manual management baselines.
  3. **SO3 (Transferability & Design Principles — Months 27–34, Lead: Doctoral Candidate):** Re-validate the artifact architecture at a second independent site (Policlínico Peruano Japonés) under the FEDS framework to formalize transferable DSR design principles for mid-sized Latin American data centers.

## 06 · Methodology
* **Process Model:** Peffers et al. (2007) 6-step DSR methodology.
* **Evaluation Design:** Venable et al. (2016) FEDS Human Risk & Effectiveness strategy, combining formative laboratory episodes (synthetic/historical verification) with naturalistic summative evaluation via Interrupted Time Series regression (Bernal et al., 2017).

## 07 · Ethical Considerations & Regulatory Compliance
* **Scientific Integrity:** Full compliance with CONCYTEC's *Código Nacional de Integridad Científica* (Res. N° 028-2024-CONCYTEC-P) and Law N° 32098 (anti-fraud and anti-plagiarism provisions, prohibiting p-hacking, HARKing, and cherry-picking).
* **Data Protection & Sector Supervision:** Compliance with Peruvian Personal Data Protection Law (Law N° 29733 and DS 016-2024-JUS) and SBS regulatory supervision. Only machine/infrastructure telemetry is ingested (zero PII of policyholders or patients); hostnames and internal IP addresses are pseudonymized prior to analysis.
* **AI Regulation:** Alignment with Peru's AI Promotion Law (Law N° 31814) and its Regulation (DS 115-2025-PCM) by enforcing human-in-the-loop oversight (*advisory* mode) for critical infrastructure.
* **AI-Use Declaration:** Generative AI assistance was used in the green zone for structural editing and formatting; intellectual design, methodological choices, and domain architecture are the author's own.

## 08 · Expected Results
1. A validated open-architecture advisory digital twin prototype (INSUR-AdvisoryTwin-Core).
2. Empirical evidence of model validity under sparse telemetry and measurable improvement in operational decisions (PUE and energy proportionality).
3. Formalized, transferable DSR design principles published in a target venue (DESRIST / *Energy Informatics* / *Sustainable Computing*).

## 09 · Timeline & Budget (36 Months + 25–30% Buffer)
* **Months 1–6:** Protocol refinement, UNMSM Research Ethics Committee (CEI) approval, and formal NDA/Data Governance execution with INSUR (includes a mandatory **25–30% contingency buffer** to absorb institutional/ethical clearance delays).
* **Months 7–16:** Telemetry ingestion pipeline, baseline benchmarking, ablation experiments, and model validity testing (SO1).
* **Months 17–26:** Naturalistic Interrupted Time Series evaluation at INSUR (SO2).
* **Months 27–36:** Secondary site validation at Policlínico Peruano Japonés (SO3), thesis writing, and defense.
* **Budget:** Self-funded/institutional compute using existing server logs ( hardware acquisition for Phase 1 MVP), with optional sensor validation kit (~,500 USD) to test the tension of whether additional instrumentation is justified.

## 10 · Core Bibliography
* Bernal, J. L., Cummins, S., & Gasparrini, A. (2017). Interrupted time series regression for the evaluation of public health interventions: A tutorial. *International Journal of Epidemiology*, 46(1), 348–355.
* Doran, G. T. (1981). There's a S.M.A.R.T. way to write management's goals and objectives. *Management Review*, 70(11), 35–36.
* Flyvbjerg, B. (2006). Five misunderstandings about case-study research. *Qualitative Inquiry*, 12(2), 219–245.
* Gregor, S., & Hevner, A. R. (2013). Positioning and presenting design science research for maximum impact. *MIS Quarterly*, 37(2), 337–355.
* Hevner, A. R., March, S. T., Park, J., & Ram, S. (2004). Design science in information systems research. *MIS Quarterly*, 28(1), 75–105.
* Peffers, K., Tuunanen, T., Rothenberger, M. A., & Chatterjee, S. (2007). A design science research methodology for information systems research. *Journal of Management Information Systems*, 24(3), 45–77.
* Venable, J., Pries-Heje, J., & Baskerville, R. (2016). FEDS: A framework for evaluation in design science research. *European Journal of Information Systems*, 25(1), 77–89.
* Yin, R. K. (2018). *Case study research and applications: Design and methods* (6th ed.). SAGE Publications.
