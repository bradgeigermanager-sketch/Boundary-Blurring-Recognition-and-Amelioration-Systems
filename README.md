# Boundary-Blurring Recognition and Amelioration Systems

This repository provides a structured framework for detecting, diagnosing, and correcting boundary drift in hybrid socio-technical environments—where organizational actors and devices interact across shared infrastructures.

The goal: **preserve explicit boundaries of agency, signal origin, and responsibility** so systems remain stable, auditable, and resistant to drift.

---

## Contents

- `docs/provenance-router-schema.md`  
  JSON schema for the Provenance Router event format.

- `docs/systems-dynamics.md`  
  Systems-dynamics diagrams modeling drift-prevention loops.

- `docs/boundary-integrity-checklist.md`  
  Compliance audit checklist for boundary integrity.

- `organizational_+_device_-_system-level_boundary_unblurring.txt`  
  Organizational + device/system boundary unblurring guide.  
  (Referenced from your active tab) 

---

## Core Concepts

### Boundary Blurring
Occurs when signals, responsibilities, or device behaviors cross domains without explicit mapping, causing misattributed causality and unstable feedback loops.

### Provenance
Machine-readable metadata describing where a signal originated, who generated it, and how it traversed the system.

### Domains
- **Organizational**: policy, strategy, operations, execution  
- **Device/System**: devices, services, shared infrastructure  
- **Hybrid**: interface layer connecting organizational actors and devices

---

## Provenance Router

The Provenance Router:

- Tags every signal with origin, intent, and authority  
- Routes actionable signals only to owning domains  
- Maintains a provenance path for post-hoc analysis  
- Prevents cross-domain contamination

See `docs/provenance-router-schema.md`.

---

## Systems Dynamics

Boundary drift is governed by three loops:

- **R1 – Provenance Reinforcement**  
- **B1 – Drift Detection & Correction**  
- **R2 – Complexity-Driven Drift**

See `docs/systems-dynamics.md`.

---

## Compliance Checklist

Use the checklist to audit:

- Governance & ownership  
- Signal provenance & routing  
- Namespace integrity  
- Feedback loop design  
- Drift-prevention controls  

See `docs/boundary-integrity-checklist.md`.

---

## Contributing

Contributions may include:

- Additional schemas  
- Case studies  
- Implementations of the Provenance Router  
- Architecture extensions

Open an issue or submit a pull request.

---

## License

MIT
