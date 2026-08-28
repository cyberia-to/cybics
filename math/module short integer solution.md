---
tags: mathematics, cryptography, cyber
alias: MSIS, module-SIS, short integer solution, SIS
crystal-type: pattern
crystal-domain: mathematics
crystal-size: atom
---
the collision side of lattice hardness: given a random matrix over a module of polynomial rings, find a short nonzero vector it maps to zero. an attacker who forges a lattice signature or finds a hash collision has solved it — so its hardness prices unforgeability

module-SIS is the signing counterpart of [[module learning with errors]]: MLWE hides secrets, MSIS prevents forgeries. together they carry the post-quantum signature schemes of the Dilithium family

[[module learning with errors]] · [[shortest vector problem]]
