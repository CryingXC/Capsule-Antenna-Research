# MIMO Capsule Antennas

A MIMO capsule antenna adds a second design axis: the antennas must work individually **and** coexist without excessive coupling.

## From SISO to MIMO

For a two-port antenna system:

- \(S_{11}\): reflection at port 1;
- \(S_{22}\): reflection at port 2;
- \(S_{21}\) / \(S_{12}\): coupling between the two ports.

A good single antenna can still produce a poor MIMO system if the elements strongly excite each other.

## Isolation

Isolation is commonly discussed using \(|S_{12}|\) or \(|S_{21}|\). More negative values indicate weaker power transfer between antenna ports.

For example, \(-20\,\text{dB}\) coupling corresponds to a voltage-wave magnitude ratio of

\[
10^{-20/20} = 0.1
\]

while \(-10\,\text{dB}\) corresponds to about 0.316. This is why a seemingly modest dB improvement can represent a meaningful reduction in coupling.

## Envelope Correlation Coefficient (ECC)

For a simplified two-port, high-efficiency case, an S-parameter approximation sometimes used for ECC is

\[
\rho_e \approx
\frac{|S_{11}^{*}S_{12}+S_{21}^{*}S_{22}|^2}
{(1-|S_{11}|^2-|S_{21}|^2)(1-|S_{22}|^2-|S_{12}|^2)}.
\]

For lossy in-body antennas, far-field-based ECC is often more physically meaningful because tissue loss and radiation efficiency complicate a purely S-parameter interpretation.

## Isolation strategies in a capsule

Possible design levers include:

- increasing element separation where geometry permits;
- rotating elements to reduce field overlap;
- exploiting polarization diversity;
- using different current-path orientations;
- introducing decoupling structures;
- modifying ground / return-current paths;
- tuning feed positions independently.

## Capsule-specific difficulty

The capsule is small enough that “move the antennas farther apart” is often not available. Therefore MIMO design becomes a **current-distribution problem**: control where currents flow and how strongly the fields of one port project onto the other element.

## Undergraduate thesis direction

The associated undergraduate thesis, **Design and Analysis of MIMO Capsule Antenna**, explored this transition from compact single-element capsule antennas toward multi-antenna operation. This public repository focuses on the reusable methodology; project-specific unpublished figures and raw HFSS files are intentionally excluded.
