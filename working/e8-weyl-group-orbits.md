# E8 Weyl-group orbits (working note)

Keep. Not a paper. Not a security claim. Separate from NTRU-701 freeze.

W(E8) order: 696729600 = 2^14 · 3^5 · 5^2 · 7.

## Roots: one orbit

W(D8) splits 240 roots as 112 integer + 128 half-integer.
One reflection through a half-integer root joins the families.
W(E8) orbit on Φ: size 240.
Stabilizer of one root = W(E7).
|W(E8)| / |W(E7)| = 240.

## Fix one root s — five inner-product layers

| <r,s> | count | meaning |
|---|---|---|
| +2 | 1 | s |
| +1 | 56 | E7 minuscule 56 |
| 0 | 126 | E7 roots orthogonal to s |
| -1 | 56 | other 56 |
| -2 | 1 | −s |

1+56+126+56+1 = 240.
Orthogonal continuation ⟨v1,v2⟩B = 0 lives in the 126-layer.

## Lattice shells

Norm is W-invariant. First shells of E8: one orbit each at norm 2 (240) and norm 4 (2160).
2R is the root orbit scaled by 2; it sits on the norm-8 shell (17520 vectors), not in S4.

## Glue code C = E8/2E8, |C| = 256 — three W-orbits

| orbit | size | name | lattice vectors in class |
|---|---|---|---|
| zero | 1 | 0 | 2E8 |
| root classes | 120 | πC(R) | pair {α,−α} |
| frames | 135 | πC(S4) | 16 norm-4 vectors per class |

1+120+135 = 256. 2160/16 = 135.
These are Tully Layer I projection counts, classical.

Unrestricted depth-2 walks use all pair-types and fill 256 classes (kill-switch does not fire).
72 / 136 only after the extra orthogonal cut.

## Do not braid

Not the 248-dim Lie algebra adjoint.
Not NTRU-701. Not QEI. Not bit security.
The integer 256 here is |C|, not a security parameter.

Cite for roots / W: standard E8; glue orbits: Berkeley E8 notes / Conway–Sloane.
Cite Tully correction: 10.5281/zenodo.22712977.
Do not cite Academia 174440406 for 1920 or kill-switch.
