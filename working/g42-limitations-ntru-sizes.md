# G42 Limitations — NTRU-701 sizes (from the locked toy)

C.J. Tully · 19 September 2026  
Object: `ly_core/ntru701_toy.py`. QEI not in the path.

## Parameters

n = 701, q = 2048 = 2^11, p = 3, d_f = 106  
f = 1 + p F, h = p g f^{-1} in Z_q[x]/(x^n − 1)  
c = r h + m

## Bytes

Packed 11-bit coefficients (q fits in 11 bits):

- public key h: 701 × 11 = 7711 bits → 964 bytes
- ciphertext c: same → 964 bytes

Stored as uint16 (what the G42 table’s 1402/1404 looks like):

- public key h: 701 × 2 = 1402 bytes
- ciphertext c: 701 × 2 = 1402 bytes  
  (table +2 on CT is a header/tag, not extra math)

Secret f is 701 small coeffs (values in a width-O(p d_f) band). Do not publish f.

## Security line (for Limitations)

Lattice layer is NTRU-701 class. Four seeds, four messages, roundtrip held.  
Bit security is not measured. Do not write 256. QEI is not part of these bytes.  
Yardstick for size: ML-KEM-768 is CT 1088 B / PK 1184 B.

## Not changed

n, q, p, d_f, the multiply, the invert. Freeze holds.

## One paragraph for the G42 Limitations section

Under the locked toy `ntru701_toy.py` the lattice layer is NTRU-701 class with n = 701, q = 2048 = 2^11, p = 3, d_f = 106, f = 1 + p F, h = p g f^{-1} in Z_q[x]/(x^n − 1), c = r h + m; packed 11-bit coefficients give public key and ciphertext of 701 × 11 = 7711 bits = 964 bytes each, while uint16 storage is 701 × 2 = 1402 bytes each and the manuscript table’s 1404-byte ciphertext is a two-byte header or tag rather than extra mathematics; secret f remains 701 small coefficients and is not published; four seeds and four messages round-tripped; bit security is unmeasured and must not be written as 256; QEI is not in this byte path; size yardstick is ML-KEM-768 at CT 1088 B / PK 1184 B; n, q, p, d_f, multiply and invert are frozen.
