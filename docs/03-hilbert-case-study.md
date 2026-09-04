# Hilbert-Fractal Conformal Capsule Antenna — ICMMT 2024 Case Study

**Paper:** *A High Gain Conformal Antenna Based on Hilbert Fractal for Capsule Endoscopy Application*  
**Role:** First author  
**Venue:** 2024 International Conference on Microwave and Millimeter Wave Technology (ICMMT)  
**IEEE Xplore:** https://ieeexplore.ieee.org/document/10672431  
**DOI:** https://doi.org/10.1109/ICMMT61774.2024.10672431

## Problem framing

A capsule antenna needs enough electrical length for low-frequency operation while remaining compatible with the curved, volume-constrained surface of a swallowable device. A Hilbert-inspired path is a natural candidate because it folds conductor length into a compact area.

## Publicly reported results

The official UESTC research feature reports:

| Metric | Publicly reported value |
|---|---:|
| Effective operating range | **0.4–3 GHz** |
| Muscle-environment resonance highlighted in the report | **1.43 GHz** |
| Reported maximum gain at that stage | **−18.4 dBi** |
| Later project-stage optimized gain reported by UESTC | **−11.2 dBi** |

Source: official UESTC feature linked in [SOURCES.md](../SOURCES.md).

## Design interpretation

### Hilbert folding increases path length

The Hilbert geometry allows a longer current path to be packed onto a limited surface. That can help lower the resonant frequency relative to a simpler conductor of comparable footprint.

### Conformal placement is part of the antenna

For a capsule, bending is not a cosmetic post-process. Curvature modifies mutual coupling between nearby conductor segments and changes the impedance seen at the feed.

### Gain must be interpreted in-body

Negative dBi gain is common for deeply embedded miniature antennas because surrounding tissue is lossy. The relevant comparison is not against a free-space consumer antenna, but against other designs under similar tissue and size constraints.

## Reproducible study questions

When revisiting a Hilbert capsule antenna in HFSS, useful sweeps include:

1. iteration order;
2. line width and spacing;
3. feed location;
4. capsule radius / bending radius;
5. tissue dielectric properties;
6. distance from surrounding phantom boundaries.

The point of the sweep is to identify which geometric variable moves **resonance**, which changes **bandwidth**, and which primarily affects **gain/efficiency**.
