# E8 geometry working pack

Keep for use. Not a paper. Not a security claim. Not NTRU-701.
C.J. Tully / NOUS_ONE working copies · 19 September 2026.

Cite Tully icosian correction: 10.5281/zenodo.22712977
Companion lemma: 10.5281/zenodo.22307539
Do not cite Academia 174440406 for 1920 or kill-switch.
Classical geometry: Baez arXiv:1712.06436; Conway–Sloane; Nebe–Sloane E8.

---

## 1. Two objects named E8

- Lattice E8 ⊂ R^8: rank 8, even, unimodular, unique. Shortest vectors ||x||^2 = 2, 240 of them.
- Lie algebra e8: dimension 8 + 240 = 248. Smallest faithful rep is the adjoint.
G42 names the adjoint. Icosian papers name the lattice. Do not add them.

---

## 2. Baez pairing

Icosian ring I ⊂ H is dense in 4-space. Coordinates in K = Q(√5).
Quaternion norm |q|^2 = x + y√5.
Baez / Conway–Sloane Euclidean form: ||q||_B^2 = x + y.
Equivalently q ↦ (q, τ(q)) with τ: √5 ↦ −√5.
Four golden slots × two Galois components = 8 reals.
That form is even, integral, unimodular, positive definite → isometric to E8.

Unit icosians |U| = 120 = 2I, N(q) = 1. They are not the 240 roots.
The Z-span of 2I, measured with ||·||_B, is the lattice.

---

## 3. Baez-norm 8

|| · ||_B is quadratic, homogeneous of degree 2.
Roots R: ||r||_B^2 = 2, |R| = 240.
||2r||_B^2 = 4 · 2 = 8.
2R lives on the norm-8 shell (17520 vectors), not in S4.

Shells from theta series Θ = 1 + 240 Σ σ3(n) q^{2n}:

| ||x||^2 | count | name |
|---|---|---|
| 2 | 240 | R |
| 4 | 2160 | S4 |
| 8 | 17520 | contains 2R (240 of them) |

Draft error: treated 2R ⊂ S4 and split 2160 = 240 + 1920. Withdrawn.
D = S4.

---

## 4. Lattice coordinate model

x in E8 iff coordinates all Z or all Z+1/2, and sum even.
112 roots: perms of (±1,±1,0^6).
128 roots: (±1/2)^8, even number of minuses.
Kissing number κ(8) = 240.

Glue: E8 = ⟨D8, v⟩ with v = (1/2)(1^8).

---

## 5. Root system geometry

240 equal-length vectors, simply laced, irreducible.
Inner products of distinct roots: {0, ±1, ±2}.
Angles: 60°, 90°, 120°, or opposite.
Convex hull: Gosset 4_21 on S^7 of radius √2.
H3/H4 projections look icosahedral (600-cell scaled by φ). That is a projection, not a second root system.

---

## 6. Lie algebra structure

dim e8 = 8 + 240 = 248.
Chevalley: [H, Xα] = α(H) Xα; [Xα, X−α] = Hα; [Xα, Xβ] = Nαβ X_{α+β} or 0.
Constructions:
- so(16) (120) plus 128-dim Spin(16) spinor.
- Magic square: 3×3 anti-Hermitian over O⊗O plus derivations (Wilson–Dray–Manogue).
Three real forms. Weyl group is not the Lie group.
G42 “248-dimensional adjoint” = this module, not the lattice.

---

## 7. Weyl-group orbits

|W(E8)| = 696729600.

Roots: one W-orbit of 240. W(D8) had two; E8 reflections join them.
Stabilizer of one root = W(E7).

Fix root s, layers of other roots:

| ⟨r,s⟩ | count |
|---|---|
| +2 | 1 |
| +1 | 56 |
| 0 | 126 |
| −1 | 56 |
| −2 | 1 |

Orthogonal filter ⟨v1,v2⟩B = 0 = the 126-layer.

Glue code C = E8/2E8 ≅ (Z/2Z)^8, |C| = 256, three W-orbits:

| orbit | size | lattice meaning |
|---|---|---|
| 0 | 1 | 2E8 |
| πC(R) | 120 | {α,−α} per class |
| πC(S4) | 135 | 16 norm-4 vectors per class (a frame) |

1+120+135 = 256. 2160/16 = 135.
Tully Layer I counts are these orbits.

---

## 8. Protocol III (correction only)

Walk: Δ(c,v) = (c + πC(v), 2).
As written, unrestricted depth-2 fills all 256 classes.
|F2^Geom| = 256 = |F2^Markov|. Kill-switch does not fire.
Extra filter ⟨v1,v2⟩B = 0 and root-avoiding: 72 cosets at depth 2 from every start in πC(S4); 136 at depth 3.
That is a declared extra cut, not Protocol III as written.

---

## 9. Do not braid

Not TT-G41 / G42 NTRU bytes.
Not QEI. Do not write 256 as bit security (256 here is |C|).
Not the RFSoC decoder.
Locked toy remains: n=701, q=2048, p=3, df=106; packed 964 B; uint16 1402 B; freeze holds.
