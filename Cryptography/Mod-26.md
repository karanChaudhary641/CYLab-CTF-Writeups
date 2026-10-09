# Mod 26

## Challenge Overview
* **Category:** Cryptography
* **Concepts Tested:** Classical substitution ciphers, Modular Arithmetic, ROT13.

## Methodology

### 1. Conceptual Analysis
The challenge presents a string obscured using a cipher based on **Modular 26** arithmetic. In cryptography, this points directly to a shift cipher (Caesar cipher). Specifically, the title hints at **ROT13** (Rotate by 13 places). 

Mathematically, the transformation for any character index \(x\) is defined as:
\[E(x) = (x + 13) \pmod{26}\]

Because 13 is exactly half of the 26-letter English alphabet, the cipher is symmetric. Applying the exact same algorithm a second time decrypts the text:
\[D(x) = (x + 13 + 13) \pmod{26} = x \pmod{26}\]

### 2. Decryption Routine
I passed the obfuscated flag string through a ROT13 rotation mechanism. Every alphabetic character shifted by 13 positions (e.g., `A` \(\leftrightarrow\) `N`, `B` \(\leftrightarrow\) `O`), while special characters and underscores remained intact to yield the final token.

## Key Takeaways
* Solidified understanding of symmetric substitution ciphers.
* Gained practical experience applying modular operations to data stream manipulation.
