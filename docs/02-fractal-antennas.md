# Fractal Antenna Fundamentals

Fractal-inspired geometries are useful in electrically small antennas because they can fold a long current path into a compact physical area. They are not a universal solution: more geometric complexity can also introduce loss, fabrication sensitivity and unwanted resonances.

## Why electrical length matters

Antenna resonance is related to the current path measured in wavelengths. If a geometry increases the effective path length while preserving a compact footprint, the resonant frequency can be reduced without proportionally increasing the physical envelope.

## Hilbert geometry

The Hilbert curve is a space-filling recursive curve. Increasing the iteration order creates a longer path inside a bounded region.

```text
Order 0:  └─┘
Order 1:  ┌─┐ ┌─┐
          │ └─┘ │
          └─────┘
Concept: more folded path inside a similar footprint
```

For a conformal capsule antenna, the useful property is the ability to obtain a relatively long conductor path while keeping the design compatible with a narrow curved surface.

## Minkowski-like geometry

Minkowski-like structures introduce repeated indentations or stepped perturbations along a line. These perturbations can lengthen the current path and create multiple nearby resonant behaviors, which may be used to broaden the matched band.

## What fractal iteration changes

Changing iteration depth or geometric scale can alter:

- total current path length;
- resonant frequencies;
- impedance trajectory;
- bandwidth;
- current concentration;
- radiation efficiency;
- sensitivity to fabrication and bending.

## Practical caution

A fractal should not be judged only by how complicated it looks. The useful question is:

> Does this geometric modification create a measurable electromagnetic benefit under the real in-body boundary conditions?

The case studies in this repository use Hilbert and Minkowski-like geometries as two different ways of trading physical size against electrical behavior.
