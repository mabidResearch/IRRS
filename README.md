# Incident Response Readiness Score (IRRS) Toolkit

This repository contains the Incident Response Readiness Score (IRRS) toolkit and associated assessment instruments developed through research into cybersecurity incident response readiness.

The IRRS provides a structured approach for assessing organisational incident response readiness through scenario-based evaluation, scoring rubrics, scenario weighting, and human-centred telemetry. The toolkit is intended to support repeatable simulation-based assessment of incident response processes and organisational response behaviour.

The work is associated with the published paper:

> Abid, M. et al. (2026). *Understanding Incident Response Readiness Through Human and System Telemetry*. Information and Computer Security.

An earlier version of the research was presented at EuroUSEC 2025.

---

## Repository Provenance

The IRRS materials were originally distributed through the [`Tenodex/IRRS`](https://github.com/Tenodex/IRRS) repository in association with the published research.

The original `Tenodex/IRRS` repository is retained as the publication-linked distribution of the toolkit.

This `MAbidResearch/IRRS` repository preserves the imported revision history and is maintained as the current research distribution of the IRRS artefacts.

The imported baseline corresponds to commit:

`1b7053c5c4c9f81440495964c6f87cdbcc3595be`

Subsequent changes to this repository relate to documentation, provenance, reproducibility, artefact governance, and preparation of a stable research release.

A frozen release will be created once the artefact set is finalised. Until that release is created, the default branch should be regarded as the current working distribution rather than an immutable version of record.

---

## Contents

### Evaluator Scoring Rubrics

Used by facilitators to assign sub-metric scores (sᵢ) based on observed organisational response behaviour during simulations.

- `Evaluator_Rubric_Ransomware.pdf`
- `Evaluator_Rubric_InsiderThreat.pdf`
- `Evaluator_Rubric_CredentialLeakage.pdf`
- `Evaluator_Rubric_CloudMisconfig.pdf`

### Scenario Weighting Guides

Provide predefined scenario-specific weighting profiles (wᵢ) for IRRS sub-metrics.

- `Scenario_Weights_Ransomware.pdf`
- `Scenario_Weights_InsiderThreat.pdf`
- `Scenario_Weights_CredentialLeakage.pdf`
- `Scenario_Weights_CloudMisconfig.pdf`

The weighting profiles are design-proposed components of the IRRS assessment mechanism. They support consistent scenario demonstration but should not be interpreted as empirically calibrated universal weights.

### Scoring Template

- `IRRS_Blank_Scoring_Card.pdf`

The scoring card provides a reusable structure for recording scenario-level IRRS assessments using the associated rubrics and weighting guides.

### Human-Centred Telemetry Instruments (v2.0)

The telemetry instruments support the diagnostic layer of the IRRS framework by enabling evaluators to capture:

- Decision Latency
- Communication Entropy
- Authority Drift

Each instrument includes pre-simulation setup guidance, structured recording tables, classification guidance, scenario-contextualised reference bands, and a worked example aligned with the Insider Threat scenario used in the associated research.

Repository instruments:

- `Checklist_A_Decision_Latency_Capture_Sheet_v2.pdf`
- `Checklist_B_Communication_Entropy_Tally_Sheet_v2.pdf`
- `Checklist_C_Authority_Drift_Tracker_v2.pdf`

#### Checklist A — Decision Latency Capture Sheet

Decision Latency measures the elapsed time between actionable intelligence becoming available to the responsible response function and the first valid technical response action being executed.

The instrument includes:

- valid-action rules;
- a structured recording table;
- mean and maximum Decision Latency summaries; and
- scenario-contextualised reference bands.

For example, a Decision Latency exceeding 10 minutes is classified within the critical reference band for an SRI 5 ransomware scenario, whereas the same duration may fall within a lower severity band for a scenario in which deliberate verification before action is operationally appropriate.

#### Checklist B — Communication Entropy Tally Sheet

Communication Entropy measures the relationship between discrete communication artefacts and valid technical response actions during an incident-response phase.

The instrument includes:

- communication counting rules;
- communication-pattern classifications;
- phase-level recording across triage, containment, eradication, and recovery; and
- scenario-contextualised reference bands.

The measure is intended to identify communication overhead and coordination patterns that may affect response efficiency.

#### Checklist C — Authority Drift Tracker

Authority Drift measures the proportion of critical response actions undertaken outside predefined role boundaries during a simulation.

The instrument includes:

- a pre-simulation Role Registry;
- drift classification guidance;
- structured tracking tables; and
- scenario-contextualised reference bands.

The instrument distinguishes between:

- **downwards drift**, where strategic or managerial roles undertake technical response actions; and
- **upwards drift**, where technical roles assume decisions normally assigned to management or executive authority.

Authority Drift is treated as an organisational response-process diagnostic rather than an assessment of individual performance.

---

## Threshold Reference Summary

The table below summarises the critical reference bands used within the three telemetry instruments.

| Scenario Class | SRI | Decision Latency (Critical) | Communication Entropy (Critical) | Authority Drift (Critical) |
|---|---:|---:|---:|---:|
| Ransomware Propagation | 5 | Over 10 mins | Over 20:1 | Over 20% |
| Insider Data Exfiltration | 4 | Over 15 mins | Over 25:1 | Over 25% |
| Cloud Misconfiguration | 3 | Over 25 mins | Over 30:1 | Over 30% |
| Credential Leakage | 3 | Over 25 mins | Over 30:1 | Over 30% |

These bands are design-proposed diagnostic reference points used to support consistent scenario interpretation. They have not been established as universal empirical thresholds and should be adapted and recalibrated where organisations accumulate sufficient local exercise or operational evidence.

---

## Evidentiary Status

The IRRS toolkit is a designed research artefact supported through structured scenario demonstration and associated research analysis.

The repository should therefore be interpreted within the following boundaries:

- the IRRS architecture and assessment mechanism are research-derived;
- the scoring rubrics and scenario weighting profiles are design-proposed;
- the human-centred telemetry instruments provide structured diagnostic measurement;
- the reference bands support scenario interpretation but are not universally empirically calibrated;
- the toolkit is not claimed to provide a universally validated organisational readiness standard; and
- further field application and empirical calibration remain appropriate areas for future validation.

These distinctions are important when applying the toolkit outside the scenarios and demonstrations documented in the associated research.

---

## Intended Use

The instruments in this repository are intended for diagnostic assessment of organisational incident response processes.

They are designed to support:

- incident-response exercises and simulations;
- organisational readiness assessment;
- identification of process bottlenecks;
- assessment of coordination and authority structures;
- repeatable scenario comparison; and
- improvement and remediation planning.

The toolkit is not intended to evaluate individual employee competence, personal performance, or conduct. Measurements should be interpreted at the response-system and organisational-process level.

---

## Versioning

This repository contains the current research distribution of the IRRS toolkit.

A frozen release will be created using the tag:

`v1.0-thesis`

Once published, that release will provide a stable and immutable version of the artefact set for citation and reproducibility purposes.

The original publication-linked repository remains available at:

[`Tenodex/IRRS`](https://github.com/Tenodex/IRRS)

---

## Reference

For the full methodology, framework architecture, scoring mechanism, worked examples, and evidentiary discussion, refer to:

> Abid, M. et al. (2026). *Understanding Incident Response Readiness Through Human and System Telemetry*. Information and Computer Security.

Earlier conference work associated with the development of the readiness approach was presented at EuroUSEC 2025.

---

## Contact

For questions regarding the IRRS framework, toolkit, or associated research artefacts, please raise an issue in this repository.
