# GRC-08 — Policy Suite & Statement of Applicability

> **PS-4 / AC-2(h) → POL-01 §4.6: "Disable within 24 hours, 8 for privileged, fed from the HR system of record." Every one of 53 policy clauses names the 800-53 and ISO control it satisfies.**
> **ISO/IEC 27001:2022 SoA: all 93 Annex A controls. 58 implemented, 31 partial, 2 planned, 2 excluded with justification. Each one tied to a GRC-03 risk, a legal or contractual driver, and evidence.**
> **The policies are written to close audit findings: POL-01 §4.6–4.8 answer GRC-04 F-01 and F-02 clause for clause.**

`Section 03 // Framework & Policy` · Part of the [GRC Control Lab Docket](https://github.com/DesmondHinds94/grc-portfolio)

---

## The suite

| Policy | Version | Clauses | Key controls |
|---|---|---|---|
| [POL-01 Access Control](policies/POL-01-access-control-policy.md) | 2.1 | 23 | AC-2, AC-6, IA-2, IA-5, PS-4 · A.5.15–5.18, A.8.2, A.8.5 |
| [POL-02 Acceptable Use](policies/POL-02-acceptable-use-policy.md) | 1.4 | 15 | PL-4, AC-19/20, MP-7 · A.5.10, A.6.2, A.8.1 |
| [POL-03 Incident Response](policies/POL-03-incident-response-policy.md) | 3.0 | 15 | IR-1 to IR-8 · A.5.24–5.28, A.6.8 |

### How a clause is written

> **4.6** On separation, access is disabled within **24 hours**, or **8 hours** for privileged users. Separations are fed automatically from the HR system of record. — *Satisfies: PS-4(a), AC-2(h) · ISO A.6.5, A.5.18*

Each clause is a testable requirement with a number in it, followed by its trace. An assessor can pick any clause, find the control it satisfies, and test it.

## What's in this repo

| File | What it is |
|---|---|
| [policies/](policies/) | Three policies with an ownership/approval header and per-clause control traces |
| [statement-of-applicability.csv](statement-of-applicability.csv) | All 93 ISO 27001:2022 Annex A controls: applicable?, inclusion reason (risk ID / legal / contractual / good practice), implementation or exclusion justification, status, 800-53 mapping, evidence |
| [traceability-matrix.csv](traceability-matrix.csv) | Generated from the policy text: policy → clause → requirement → 800-53 → ISO |
| [tools/build_soa.py](tools/build_soa.py) | Builds both CSVs and checks that every ISO control a policy cites is marked applicable in the SoA |

```bash
python3 -I tools/build_soa.py
# SoA: 93 controls {'Implemented': 58, 'Partially implemented': 31, 'Planned': 2, 'Excluded': 2}
# Traceability: 53 clauses across 3 policies
# Policy-cited ISO controls not applicable in SoA: none
```

## Exclusions (and why only two)

| Control | Justification |
|---|---|
| A.7.12 Cabling security | CivicStack runs no data center or wiring closet. Data-center cabling is covered through the AWS inheritance documented under A.5.23 |
| A.8.30 Outsourced development | All HAP development is done by CivicStack employees. Re-evaluate if contractors are engaged |

The other physical controls are **included and marked inherited**, not excluded. An auditor expects inherited controls to appear in the SoA with the provider's evidence behind them.

## Links

Controls and statuses line up with [GRC-02](https://github.com/DesmondHinds94/grc-02-gap-analysis-poam) (gap analysis), [GRC-05](https://github.com/DesmondHinds94/grc-05-800-53a-control-testing) (test results) and [GRC-07](https://github.com/DesmondHinds94/grc-07-framework-crosswalk) (mappings).

---

*Fictional organization. ISO/IEC 27001 control identifiers and titles are referenced for mapping only; the standard is © ISO.*
