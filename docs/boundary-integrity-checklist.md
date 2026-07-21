# Boundary Integrity Compliance Checklist

Use this checklist for quarterly audits across organizational and device/system domains.

---

## A. Governance & Ownership

- Is there a current map of domains of control, influence, and concern?
- Are decision-makers formally authorized for the domains they affect?
- Are any processes “shadow-owned” without explicit assignment?

---

## B. Signal Provenance & Routing

- Do all signals carry source, domain, actorId, and intent?
- Are actionable signals routed only to actors with authority?
- Are cross-domain signals mediated by a defined interface layer?

---

## C. Namespace & Configuration Integrity

- Are logs and telemetry segregated by device/namespace?
- Are configuration files scoped to specific devices/services?
- Do automation scripts declare and enforce their domain of effect?

---

## D. Feedback Loop Design

- Are feedback loops documented with owner and domain?
- Are cross-domain loops explicitly designed with contracts?
- Have misalignment incidents been logged and analyzed?

---

## E. Drift-Prevention Controls

- Do integration changes undergo boundary impact assessment?
- Are boundary-related incidents feeding back into standards?
- Is there a scheduled review to re-segment domains as systems evolve?

