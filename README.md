# Incident Response Readiness Score (IRRS) Toolkit

This repository supports the paper *"Understanding Incident Response Readiness Through Human and System Telemetry"* (Information and Computer Security, 2026) and the earlier conference version presented at EuroUSEC 2025. It provides evaluator tools, scenario materials, human-centric telemetry instruments, and reproducibility resources for simulation-based incident response readiness assessment.

---

## Contents

### Evaluator Scoring Rubrics
Used by facilitators to assign sub-metric scores (sᵢ) based on observed behaviour during simulations.

- `Evaluator_Rubric_Ransomware.pdf`
- `Evaluator_Rubric_InsiderThreat.pdf`
- `Evaluator_Rubric_CredentialLeakage.pdf`
- `Evaluator_Rubric_CloudMisconfig.pdf`

### Scenario Weighting Guides
Predefined weights (wᵢ) for each sub-metric based on scenario risk impact and SRI level.

- `Scenario_Weights_Ransomware.pdf`
- `Scenario_Weights_InsiderThreat.pdf`
- `Scenario_Weights_CredentialLeakage.pdf`
- `Scenario_Weights_CloudMisconfig.pdf`

### Scoring Template
- `IRRS_Blank_Scoring_Card.pdf`

### Human-Centric Telemetry Instruments (v2.0)
These instruments support the diagnostic telemetry layer of the IRRS framework, enabling evaluators to capture Decision Latency, Communication Entropy, and Authority Drift during simulations. Each document includes a pre-simulation setup section, structured recording tables, classification guidance, scenario-contextualised threshold bands, and a fully worked example aligned with the Insider Threat scenario used in the paper.

- `Checklist_A_Decision_Latency_Capture_Sheet_v2.docx`
- `Checklist_B_Communication_Entropy_Tally_Sheet_v2.docx`
- `Checklist_C_Authority_Drift_Tracker_v2.docx`

#### Checklist A — Decision Latency Capture Sheet
Measures the elapsed time between actionable intelligence becoming visible to a responsible operator and the first valid technical response action being executed. Includes valid action rules, a recording table, mean and maximum Decision Latency summary, and scenario-specific threshold guidance. For example, a Decision Latency exceeding 10 minutes is classified as critical in SRI 5 ransomware scenarios, while the same duration falls within the elevated band for SRI 4 insider threat investigations where deliberate verification before action is operationally appropriate.

#### Checklist B — Communication Entropy Tally Sheet
Measures the ratio of discrete communication artefacts to valid technical actions per response phase. Includes counting rules, a communication pattern classification table covering instruction-driven, consensus-seeking, and approval-seeking dynamics, a phase-by-phase recording table covering triage, containment, eradication, and recovery, and scenario-specific threshold guidance.

#### Checklist C — Authority Drift Tracker
Measures the proportion of critical actions taken outside predefined role boundaries during a simulation. Includes a mandatory pre-simulation Role Registry that must be completed before the simulation begins, a drift type classification table distinguishing downwards drift (strategic roles performing technical actions) from upwards drift (technical roles assuming executive decisions), a tracking table, and scenario-specific threshold guidance.

---

## Threshold Reference Summary

The table below summarises the critical classification thresholds across all three telemetry instruments by scenario class. Full calibration tables including acceptable and elevated bands are included within each instrument.

| Scenario Class | SRI | Decision Latency (Critical) | Communication Entropy (Critical) | Authority Drift (Critical) |
|---|---|---|---|---|
| Ransomware Propagation | 5 | Over 10 mins | Over 20:1 | Over 20% |
| Insider Data Exfiltration | 4 | Over 15 mins | Over 25:1 | Over 25% |
| Cloud Misconfiguration | 3 | Over 25 mins | Over 30:1 | Over 30% |
| Credential Leakage | 3 | Over 25 mins | Over 30:1 | Over 30% |

These thresholds are practitioner-informed reference points intended to be refined through repeated simulation cycles as empirical data accumulates.

---

## Intended Use Statement

All instruments in this repository are designed for diagnostic analysis of incident response processes at the system level. They must not be used to evaluate individual competence, performance, or personal conduct. All measurements reflect organisational behaviour under simulated conditions and are intended exclusively for improvement and remediation purposes.

---

## Reference

For full methodology, scoring formulas, worked examples, and framework architecture, please refer to:

> Abid, M. et al. (2026). *Understanding Incident Response Readiness Through Human and System Telemetry*. Information and Computer Security.

For the earlier conference version of this work, please refer to the EuroUSEC 2025 paper.

---

## Contact

For questions regarding the framework or instrumentation, please raise an issue in this repository.
