# HFSS Research Workflow for Capsule Antennas

This chapter records a reproducible **method**, not a private HFSS project file.

## 1. Define the physical environment first

Before optimizing geometry, define:

- capsule dimensions and shell material;
- conformal substrate;
- tissue / phantom material properties;
- distance to phantom boundaries;
- feed model;
- target frequency bands.

An antenna optimized in the wrong dielectric environment can converge to the wrong design.

## 2. Parameterize the geometry

Useful parameters include:

- fractal iteration scale;
- conductor width;
- gap / spacing;
- feed location;
- substrate thickness;
- bending radius;
- MIMO element rotation / separation.

Avoid hard-coding dimensions when a parameter sweep is likely.

## 3. Convergence before optimization

Check mesh convergence and solution convergence before interpreting small differences between candidate designs. A 0.2 dB “improvement” is meaningless if the numerical uncertainty is comparable.

## 4. Optimize in stages

A practical sequence is:

```mermaid
flowchart LR
    A[Resonance placement] --> B[Impedance bandwidth]
    B --> C[Gain / efficiency]
    C --> D[Robustness]
    D --> E[MIMO isolation]
    E --> F[Measurement correlation]
```

Trying to optimize every metric simultaneously from the first iteration makes cause-and-effect harder to understand.

## 5. Use field/current plots diagnostically

When a geometry change helps or hurts, inspect the surface-current distribution. Ask:

- Which segment carries the strongest current?
- Did the effective path length change?
- Is energy trapped in a near-field region?
- In MIMO, where does coupled current enter the passive element?

This turns optimization from parameter hunting into electromagnetic reasoning.

## 6. Keep a simulation log

For each important run, record:

- geometry revision;
- material model;
- solver settings;
- frequency sweep;
- S-parameter extrema;
- gain/efficiency;
- qualitative current-distribution observation.

A compact design log is often more valuable than hundreds of unlabeled project copies.
