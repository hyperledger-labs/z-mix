# Lab Name
z-mix

# Short Description
z-mix will offer a generic way to create Zero-Knowledge proofs, proving statements about multiple cryptographic building blocks, containing signatures, commitments, and verifiable encryption.
z-mix facilitates

# Scope of Lab
The goal of z-mix is to become a part of Hyperledger crypto-lib, and eventually be adopted by Hyperledger projects. Multiple existing Hyperledger projects require Zero-Knowledge proofs, e.g., Fabric and Indy. The goal of this library is to provide a single flexible and secure implementation to construct such proofs.

# Initial Committers
* Manu Drijvers (manudrijvers)
* Jan Camenisch (jancamenisch)
* Nathan George (nage)
* Daniel Hardman (dhh1128)
* Angelo De Caro (adecaro)
* Maria Dubovitskaya (dubovitskaya)
* Jason Law (jasonalaw)
* Michael Lodder (mikelodder7)
* Lovesh Harchandani (lovesh)

# Sponsors
* Nathan George
* Hart Montgomery

# Spec
z-mix uses JSON objects to provide a *zero knowledge language (ZKL)* to express

* Requests of attested attribute values
* Resolutions for requests that can be validated
* Proofs that satisfy requests

### Process
z-mix translates a ZKL-ProofSpec and a corresponding ZKL-Witness, both represented as JSON objects, into a ZKL-Proof JSON object.

The **ZKL-ProofSpec** defines the statement to be proven and contains all public information needed by a verifier \[e.g., Credential Definitions, Revocation Authority, Pseudonyms].

The **ZKL-Witness** contains the secrets required to compute a proof \[e.g. secret keys, all attribute values, the credentials involved, the randomness used to compute a pseudonym].

The **ZKL Proof** is the data that satisfies the statement to be proven.
