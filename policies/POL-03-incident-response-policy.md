# POL-03 — Incident Response Policy

| | |
|---|---|
| **Organization** | CivicStack Solutions LLC |
| **Version** | 3.0 · **Effective** 2026-09-20 · **Next review** 2027-09-20 or after any Sev-1 |
| **Owner** | CISO · **Approved by** CEO |
| **Applies to** | All CivicStack systems and services, including HAP, and every workforce member |
| **Implements** | NIST SP 800-53 Rev 5 IR-1, IR-2, IR-3, IR-4, IR-5, IR-6, IR-7, IR-8 · ISO/IEC 27001:2022 A.5.24–A.5.28, A.6.8 |

The detailed procedures sit in the **IR Plan v3.0** and its playbooks. This policy sets the requirements those documents must meet.

---

## 1. Purpose and scope

**1.1** CivicStack detects, responds to and recovers from security incidents in a way that limits harm to customers and the people whose data we hold, and meets our legal and contractual duties to report. — *Satisfies: IR-1(a)(1) · ISO A.5.24*

**1.2** An **incident** is any event that actually or potentially compromises the confidentiality, integrity or availability of a system or of data, or violates security policy. — *Satisfies: IR-8(a)(4) · ISO A.5.25*

## 2. Roles

**2.1** The **CISO** owns this policy and the IR capability. The IR Plan names, for each role, a primary and a backup: Incident Commander, Deputy, Technical Lead, Communications Lead, Legal, and a Customer Liaison for each government customer. — *Satisfies: IR-8(a)(5), IR-1(b) · ISO A.5.24, A.5.2*

**2.2** Every workforce member reports suspected incidents immediately (POL-02 §6.1). — *Satisfies: IR-6(a) · ISO A.6.8*

## 3. Severity and handling

**3.1** Incidents are triaged within **15 minutes** of a P1 alert and given a severity (Sev-1 to Sev-4) using the matrix in the IR Plan. Any confirmed or suspected exposure of customer PII is **Sev-1 or Sev-2**. — *Satisfies: IR-4(a), IR-8(a)(4) · ISO A.5.25*

**3.2** Incident handling covers preparation, detection and analysis, containment, eradication and recovery. Each phase is logged in the incident record. — *Satisfies: IR-4(a), IR-5 · ISO A.5.26*

**3.3** Evidence is collected and preserved with a chain of custody whenever legal action, law enforcement or regulatory reporting is possible. — *Satisfies: IR-4, AU-9 · ISO A.5.28*

## 4. Notification

**4.1** **Government customers are notified within 24 hours of an incident being declared** (for HAP: the CMHA ISSO), and updated at least every 24 hours until closure. — *Satisfies: IR-6(b), IR-6(3) · ISO A.5.26, A.5.5*

**4.2** Notifications to regulators and affected individuals (state breach-notification law, HUD, and US-CERT/CISA where a contract requires it) are decided by Legal together with the customer, within the time each obligation sets. — *Satisfies: IR-6(b) · ISO A.5.5, A.5.31*

**4.3** Suppliers whose services are involved are notified and their cooperation requested under contract (see the vendor addenda). — *Satisfies: IR-6(3), SR-8 · ISO A.5.19*

## 5. Testing, training and improvement

**5.1** The IR Plan is tested at least **annually** with a tabletop exercise that includes the customer liaison role, and after any major change to the plan. — *Satisfies: IR-3, IR-3(2) · ISO A.5.24*

**5.2** Everyone with an IR role is trained within 30 days of taking the role and every year after that. — *Satisfies: IR-2 · ISO A.6.3*

**5.3** Each Sev-1 or Sev-2 incident and each exercise produces an after-action report within 10 business days. Corrective actions are tracked in the POA&M. — *Satisfies: IR-4(c), IR-8(c) · ISO A.5.27*

## 6. Plan maintenance

**6.1** The IR Plan is reviewed annually and updated after exercises, incidents and organizational changes. Changes are sent to the named roles and acknowledged. — *Satisfies: IR-8(b), IR-8(c), IR-8(d) · ISO A.5.24*

**6.2** The IR Plan is protected from unauthorized disclosure and modification. — *Satisfies: IR-8(e) · ISO A.5.24*
