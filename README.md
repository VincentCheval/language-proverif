# language-proverif

Syntax support for the automatic prover ProVerif

ProVerif is an automatic cryptographic protocol verifier, in the formal model (so called Dolev-Yao model). This protocol verifier is based on a representation of the protocol by Horn clauses. Its main features are:
- It can handle many different cryptographic primitives, including shared and public-key cryptography (encryption and signatures), hash functions, and Diffie-Hellman key agreements, specified both as rewrite rules or as equations.
- It can handle an unbounded number of sessions of the protocol (even in parallel) and an unbounded message space. This result has been obtained thanks to some well-chosen approximations. This means that the verifier can give false attacks, but if it claims that the protocol satisfies some property, then the property is actually satisfied. The considered resolution algorithm terminates on a large class of protocols (the so-called "tagged" protocols). When the tool cannot prove a property, it tries to reconstruct an attack, that is, an execution trace of the protocol that falsifies the desired property.

ProVerif can prove the following properties:

- secrecy (the adversary cannot obtain the secret)
- authentication and more generally correspondence properties
- strong secrecy (the adversary does not see the difference when the value of the secret changes)
equivalences between processes that differ only by terms

Official webpage of ProVerif: https://prosecco.gforge.inria.fr/personal/bblanche/proverif/

##### Changelog

- 15/03/2021 - Version 1.2.0 - Rely now on a tree-sitter grammar.
- 02/10/2017 - Version 1.0.0 - First release
