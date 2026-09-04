# Reading S-Parameters, Bandwidth, Gain and Isolation

These quantities answer different questions. Treating one as a proxy for all the others is a common source of confusion.

## S11 — input matching

\[
S_{11} = \frac{b_1}{a_1}\bigg|_{a_2=0}
\]

It describes how much incident wave at port 1 is reflected back. Return loss is often written as

\[
RL = -20\log_{10}|S_{11}|.
\]

Thus \(|S_{11}|=-10\,\text{dB}\) corresponds to about 10% reflected power and roughly 90% accepted power, **not** 90% radiated power.

## S12 / S21 — coupling

For a reciprocal passive antenna structure, \(S_{12}\) and \(S_{21}\) are typically equal in theory. They describe transmission from one port to the other and are widely used as an isolation indicator.

## Bandwidth

A common impedance-bandwidth definition is the frequency region in which

\[
|S_{11}| < -10\,\text{dB}.
\]

For MIMO, this condition should normally be checked for every antenna port.

## Gain

Realized gain combines radiation directivity with efficiency and mismatch. In lossy tissue, gain can be strongly negative while the antenna still supports a viable short-range telemetry link.

## Why a good S11 can coexist with poor gain

Accepted power may be dissipated in:

- conductor loss;
- dielectric loss;
- biological tissue;
- non-radiating near-field mechanisms.

So the chain is:

```text
Input power → accepted power → radiated power → directional gain
             ↑ S11              ↑ efficiency
```

## Recommended result set

A technically convincing capsule-antenna result should, where possible, include:

1. S11 (and S22 for MIMO);
2. S12/S21 for MIMO isolation;
3. gain versus frequency;
4. radiation efficiency;
5. current distribution;
6. radiation pattern;
7. tissue/environment robustness;
8. measurement-to-simulation comparison.
