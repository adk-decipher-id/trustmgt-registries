## FG-TIDA WGx: Trust Management \- Verifier/Relying Party Network Registries (trustmgt-registries)

## Charter Information

- **Charter version:** v0.1  
- **Date:** 2026-11-10  
- **Status:** Draft / Under review by FG-TIDA
- 
## Documentation

Backgrounder Documents: (links to be updated when contributed to TIDA github repository)

* Terminology: [https\://docs.google.com/document/d/1NE\_dGQ-5iBBbAu7jJr9p\_9M-w76rExpe/edit\#heading=h.o62psr6yucfb](https://docs.google.com/document/d/1NE_dGQ-5iBBbAu7jJr9p_9M-w76rExpe/edit#heading=h.o62psr6yucfb)&nbsp;  
* Challenge: [https\://docs.google.com/document/d/1OPCxgF5ZsoJkk3bkBKchm2pby6CuCBac/edit](https://docs.google.com/document/d/1OPCxgF5ZsoJkk3bkBKchm2pby6CuCBac/edit)  
* Building & Enforcing Conventions as Policy: [https\://docs.google.com/document/d/1NIIRz8avy1gJwrZbJ\_IgmnJk9\_ytQzeof1OJ7vW\_qxU/edit?tab=t.0](https://docs.google.com/document/d/1NIIRz8avy1gJwrZbJ_IgmnJk9_ytQzeof1OJ7vW_qxU/edit?tab=t.0)&nbsp;  
* Examples of Government Accreditation of Verifier Networks serving vertical markets: [https\://www\.gov.uk/government/collections/uk-digital-verification-services-trust-framework](https://www.gov.uk/government/collections/uk-digital-verification-services-trust-framework)&nbsp;
  
## WG Goals

The Working Group will:

1. **Publish the Verifier Network Operator Framework:** Define the reference architectures, governance baselines, policy subsets, and operational lifecycles required for a Verifier Network Operator (VNO) to organize relying parties within specific vertical markets around binding, enforceable ecosystem Conventions.  Use examples from member vertical markets for expertise.  
2. **Specify Reader Registrar Architecture and Trust Mechanism Integration:** Standardize the operational profiles for deputized Reader Registrars that assess verifier compliance, issue cryptographic Reader ID Certificates, maintain revocation endpoints, and publish discoverable Reader Trust Lists (e.g., RICAL-style registries) functioning across credential formats.  
3. **Establish a Staged Deployment Pathway (Domestic to Cross-Border):** Provide an operational blueprint that allows a VNO to deploy a Reader Registrar within a single domestic legal environment first, establishing legal and regulatory compliance, and then extend the model to federated, cross-border vertical networks through international policy harmonization.  
4. **Define Runtime Conformance and Trust Vector Enforcement:** Consider and explain how digital wallets and reader devices execute mutual authentication and dynamic policy enforcement at transaction time across the critical trust vectors: *Ecosystem Trusts Reader*, *User Trusts Verifier*, and *Reader Trusts Wallet*.  This WG must work directly with Wallet standards, certification bodies, and Wallet Providers as Policy Enforcement Points for the Ecosystems.  
5. **Inform Global Certification Schemes for Readers and Wallets:** Establish normative evaluation criteria and testable profiles that inform independent third-party certification authorities (e.g., Kantara Initiative, ISO/IEC compliance bodies, and commercial test laboratories) regarding Reader Authentication conformance, data minimization, and triple-barrier receipt isolation.  
6. **Codify Credential Acceptance Selection Criteria:** Define standard formats and procedures for VNOs to evaluate, ingest, and apply external issuer metadata to designate acceptable and unacceptable credentials for specific vertical market use cases without assuming issuer governance responsibilities.  On top of this responsibility, VNOs must know how to add Verifier behavior and meaningful Policy to their set of operations so that Users trust participants in their operating space and vertical market (perhaps through Trust Marks or verifiable badges)
  
## What's in this repository

- [src/doc/index.rst](src/doc/index.rst) — the charter itself (the content you edit).
- [CONTRIBUTING.md](CONTRIBUTING.md) — how to contribute, build, preview, and publish.
- [WG-ONBOARDING.md](WG-ONBOARDING.md) — the author's guide.
