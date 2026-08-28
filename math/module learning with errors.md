---
tags: mathematics, cryptography, cyber
alias: MLWE, module-LWE, learning with errors, LWE
crystal-type: pattern
crystal-domain: mathematics
crystal-size: atom
---
the hardness assumption behind most practical lattice cryptography: given noisy inner products of a secret vector over a module of polynomial rings, recover the secret. the noise makes the linear system computationally opaque — solving it is as hard as worst-case lattice problems like the [[shortest vector problem]]

module-LWE interpolates between plain LWE (large keys, loose structure) and ring-LWE (small keys, more structure): security tunes by module rank. it underlies Kyber, Dilithium and the TFHE regime of the [[mudra]] ladder — encrypted balances in [[strata]] rest on this assumption holding

[[module short integer solution]] · [[shortest vector problem]]
