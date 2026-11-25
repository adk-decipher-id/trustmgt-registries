# FG-TIDA WGx: Trust Management \- Verifier/Relying Party Network Registries (trustmgt-registries)

## Charter Information

- **Charter version:** v0.1  
- **Date:** 2026-11-10  
- **Status:** Draft / Under review by FG-TIDA

---

## 1\. Group Information

| Field | Content |
| :---- | :---- |
| **Working group name and acronym** | Trust Management (`trustmgt-rp`) — Working Group x? |
| **FG-TIDA theme(s) covered** | Discovery and Cross-Border Trust (Primary), Runtime Enforcement (Control Plane), Dynamic Identity, Delegation (from Humans to Agents) |
| **Chair(s) / co-chairs** | Decipher Identity (requested) / TIDA Trust Management representatives, Vertical Market Verifier representatives (please volunteer\!) |
| **Editor(s) of the main deliverables (mirroring intended audience)** | Trust Architect (Reader Registrar Operations), Policy Manager (Ecosystem/Network Conventions) |
| **Mailing list** | Please create for WGx |
| **Repository and issue tracker** | GitHub FG-TIDA WGx Trust Management Repository |
| **Charter status and version** | Draft v0.1 |

&nbsp;

Backgrounder Documents: (links to be updated when contributed to TIDA github repository)

* Terminology: [https\://docs.google.com/document/d/1NE\_dGQ-5iBBbAu7jJr9p\_9M-w76rExpe/edit\#heading=h.o62psr6yucfb](https://docs.google.com/document/d/1NE_dGQ-5iBBbAu7jJr9p_9M-w76rExpe/edit#heading=h.o62psr6yucfb)&nbsp;  
* Challenge: [https\://docs.google.com/document/d/1OPCxgF5ZsoJkk3bkBKchm2pby6CuCBac/edit](https://docs.google.com/document/d/1OPCxgF5ZsoJkk3bkBKchm2pby6CuCBac/edit)  
* Building & Enforcing Conventions as Policy: [https\://docs.google.com/document/d/1NIIRz8avy1gJwrZbJ\_IgmnJk9\_ytQzeof1OJ7vW\_qxU/edit?tab=t.0](https://docs.google.com/document/d/1NIIRz8avy1gJwrZbJ_IgmnJk9_ytQzeof1OJ7vW_qxU/edit?tab=t.0)&nbsp;  
* Examples of Government Accreditation of Verifier Networks serving vertical markets: [https\://www\.gov.uk/government/collections/uk-digital-verification-services-trust-framework](https://www.gov.uk/government/collections/uk-digital-verification-services-trust-framework)&nbsp;

---

## 2\. Background and Problem Statement

Digital identity systems are shifting from closed, regional, issuer-led models toward an open fabric of decentralized wallets, diverse credential issuers, and Verifier Networks that coordinate behavior around a vertical market. In this mix, **Verifier Network Operators** (see example Use Case, consider Payments networks, Telecom onboarding) lead across a vertical market use case with the policies for accepting Digital ID, the transparency that protects Users, and the Registrars that ensure against rogues while complying with regional consent & purpose legislation.

While significant international standardization has occurred around credential syntax (such as W3C Verifiable Credentials and ISO/IEC 18013-5 mdoc) and presentation protocols (such as ISO/IEC 18013-5/7 and OpenID for Verifiable Presentations), a critical architectural void remains on the relying party interface: the governance, registration, and runtime verification of policy within Verifier Networks.  This void is also deterring adoption of Readers and insecurity about liability and insurance.

Today, relying parties (verifiers) operate uncertified in-person readers that cannot cryptographically identify themselves to wallets during transactions. The absence of mutual Reader Authentication creates severe vulnerabilities:

1. **Rogue Readers and Exploitation:** Rogue unauthorized readers can solicit sensitive identity data without proof of legitimate commercial standing or compliance with data protection laws.  
2. **Commercial Surveillance and Ad-Tech Tracking:** In the absence of binding operational rules, market actors risk replicating web tracking mechanisms—such as tracking users across disparate locations, collecting unneeded personal identifiable information (PII), or fingerprinting government credentials into permanent tracking authenticators.  
3. **Overuse, Overask, and Frequent ID Checks:** Without enforceable collection limitation rules, verifiers tend to over-collect data (such as requesting full dates of birth when an age assertion suffices) and store unencrypted transaction trails.  
4. **Bilateral Friction and Operational Scalability:** Verifiers and wallet providers are forced into brittle, bilateral commercial contracts that prevent seamless cross-border acceptance and eliminate user choice in wallet applications.  
5. **Single Provider Risk**: Phone platform developers already have scaled Developer Programs to include tools to create Relying Party Registrars at the risk of being in their walled gardens.  This can help EU Governments become Verifier Registrars, but they need a policy deployment map. Others like Payment Network Operators do not know how to step into the game and activate their networks of Verifiers.&nbsp;  
6. **Regional Silos**: As market needs for Trust Management arise in one region, they may be solved with custom or incompatible solutions that do not scale globally despite many global verticals.

In high-assurance vertical markets—such as payment onboarding, global banking & fintech, healthcare delivery, and regulated retail—verifiers operate across jurisdictional borders and require dependable risk mitigation before accepting digital credentials. To achieve this, Verifier Network Operators (VNOs) must organize member verifiers around binding Conventions (operational, privacy, and security mandates), select discoverable Trust Mechanisms, and deploy cryptographic Trust Elements (such as Reader ID Certificates and Trust Marks) through deputized Reader Registrars. This can activate insurance providers and cross-market certification schemes that mitigate risk globally.

The International Telecommunication Union Focus Group on Technical Aspects of Digital Identity and Trust (FG-TIDA) and the TIDA.community platform provide a unique forum connecting global technologists, industry consortia, and global policy makers. This working group will bridge vertical market operational realities with international policy harmonization, establishing a structured pathway for Verifier Network Operations.

---

## 3\. Goals

The Working Group will:

1. **Publish the Verifier Network Operator Framework:** Define the reference architectures, governance baselines, policy subsets, and operational lifecycles required for a Verifier Network Operator (VNO) to organize relying parties within specific vertical markets around binding, enforceable ecosystem Conventions.  Use examples from member vertical markets for expertise.  
2. **Specify Reader Registrar Architecture and Trust Mechanism Integration:** Standardize the operational profiles for deputized Reader Registrars that assess verifier compliance, issue cryptographic Reader ID Certificates, maintain revocation endpoints, and publish discoverable Reader Trust Lists (e.g., RICAL-style registries) functioning across credential formats.  
3. **Establish a Staged Deployment Pathway (Domestic to Cross-Border):** Provide an operational blueprint that allows a VNO to deploy a Reader Registrar within a single domestic legal environment first, establishing legal and regulatory compliance, and then extend the model to federated, cross-border vertical networks through international policy harmonization.  
4. **Define Runtime Conformance and Trust Vector Enforcement:** Consider and explain how digital wallets and reader devices execute mutual authentication and dynamic policy enforcement at transaction time across the critical trust vectors: *Ecosystem Trusts Reader*, *User Trusts Verifier*, and *Reader Trusts Wallet*.  This WG must work directly with Wallet standards, certification bodies, and Wallet Providers as Policy Enforcement Points for the Ecosystems.  
5. **Inform Global Certification Schemes for Readers and Wallets:** Establish normative evaluation criteria and testable profiles that inform independent third-party certification authorities (e.g., Kantara Initiative, ISO/IEC compliance bodies, and commercial test laboratories) regarding Reader Authentication conformance, data minimization, and triple-barrier receipt isolation.  
6. **Codify Credential Acceptance Selection Criteria:** Define standard formats and procedures for VNOs to evaluate, ingest, and apply external issuer metadata to designate acceptable and unacceptable credentials for specific vertical market use cases without assuming issuer governance responsibilities.  On top of this responsibility, VNOs must know how to add Verifier behavior and meaningful Policy to their set of operations so that Users trust participants in their operating space and vertical market (perhaps through Trust Marks or verifiable badges)

---

## 4\. Scope and Non-Goals

### In Scope

The Working Group focuses exclusively on the governance, operational mechanisms, and deployment protocols governing Verifier Networks, Relying Parties, Reader Registries, and their transaction-time interaction with digital wallets:

- **Verifier Network Architecture and Lifecycle:** Describing the roles, rights, and duties of the Verifier Network Builder, Verifier Network Operator (VNO), Member Verifiers, and Governance Councils within vertical markets to activate ecosystem building globally.  
- **Convention Formulation across Trust Vectors:** Defining the methodology for translating Tier 1 Operational Considerations (governance models, legal backing, sustainability) and Tier 2 Participant Considerations (social, business, operational, and legal values) into enforceable technical Conventions that satisfy participant Trust Vectors.  
- **Reader Registrars and Registry Profiles:**  
  - Describe the onboarding, vetting, and compliance evaluation of relying parties.  
  - Generating and issuing cryptographic Trust Elements (Reader ID Root Certificates, Intermediate Certificates, and cryptographically verifiable Trust Marks).  
  - Publishing and distributing Reader Trust Lists (e.g., RICAL / Reader CA Trust Lists) and revocation endpoints.  
- **Staged Implementation Architecture:**  
  - *Phase 1 (Single Legal Environment):* Operationalizing a Reader Registrar under a single national or state legal jurisdiction, establishing contract law enforceability, and aligning with local data privacy mandates.  
  - *Phase 2 (Cross-Border / Multi-Jurisdictional):* Federating Reader Registries across national boundaries, defining cross-border dispute resolution hooks, and establishing multilateral recognition frameworks for vertical markets (e.g., global payment systems).  
- **Activate Runtime Reader Authentication and Consent:**  
  - Technical profiles for Reader presentation of Reader ID Certificates to Wallets (via ISO/IEC 18013-5 proximity engagements, ISO/IEC 18013-7 web engagements, and OpenID for Verifiable Presentations).  Coordinate with OIDF HAIP.  
  - Wallet-side introspection of Reader ID Certificates against authorized Reader Trust Lists without requiring real-time external network call-backs.  
  - Rendering standardized Justification Labels to holders during consent flows.  
- **Privacy Safeguards and Data Minimization:** Enforcing zero-knowledge proofs, selective disclosure, presentations anonymity, dynamic ephemeral identifier rotation (e.g., dynamic Mobile Security Objects), and triple-barrier receipt isolation within Verifier operations and across wallet architectures.  
- **Acceptable Credential Ingestion Rules:** Defining the programmatic schemas and policy rules by which a VNO consumes external trust lists and metadata from authorized Issuer Trust List Providers to mark specific credential types as acceptable or unacceptable for defined transaction risk tiers.  Align with the Trust Registries Task Force investigating Issuer federations.  Provide extensive feedback on the metadata describing the “value” of specific credentials to the Reader Registrar ecosystems that enables the creation of these Acceptable Credential Ingestion Rules.  
- **Input to Global Certification Authorities:** Developing testable requirements that feed into formal certification schemes for Reader hardware/software and Wallet application consent engines.  
- **Input to Global Standardization Bodies/Organizations**: Multiple protocols exist across&nbsp;

### Out of Scope / Non-Goals

To prevent scope creep, maintain organizational focus, and respect existing standards bodies, the Working Group strictly bounds its mandate:

- **Infringing on Issuer Trust List Providers:** The Working Group will **NOT** define, operate, or publish Issuer Trust Lists, Verified Issuer Certificate Authority Lists (VICALs), ICAO Public Key Directories (PKD), or sovereign Master Lists. Trust over credential issuers remains strictly the domain of sovereign authorities, issuer associations, and designated Issuer Trust List Providers.  
- **Issuer Governance and Lifecycle Management:** The Working Group will **NOT** address credential issuance protocols, identity proofing standards (e.g., IAL1-3 definitions), credential revocation infrastructure (e.g., 18013-5 status lists), or statutory mandates placed on issuing authorities (e.g., DMVs, passport offices, or national civil registries).  
- **Credential Value Mapping and Assurance Equivalency:** The Working Group will **NOT** define cross-issuer attribute taxonomies, credential value-mapping frameworks, or general-purpose equivalency matrices between disparate national credentials.  
- **External Metadata Generation:** The Working Group's scope regarding credentials is strictly confined to the *consumption* and *selection* of credentials by a VNO for vertical use cases based on external trust information provided by issuers. The WG does not define or alter the issuer's source metadata.  
- **Underlying Transport Protocols:** The Working Group will **NOT** redefine base-level communication standards (such as NFC, Bluetooth Low Energy, QR codes, or HTTP REST APIs), but will profile existing ISO/IEC and OpenID Foundation standards.

---

## 5\. Programme of Work and Deliverables

| \# | Deliverable | Short Description | Input Documents |
| :---- | :---- | :---- | :---- |
| **D3.1** | **Verifier Network Reference Architecture and Conventions Framework** | Technical specification defining the operational model of a Verifier Network Operator (VNO), the formulation of binding Conventions across Tier 1 and Tier 2 considerations, and the enforcement of Trust Vectors (*Ecosystem Trusts Reader*, *User Trusts Verifier*, *Reader Trusts Wallet*). | `verifier-network-operator-use-case.md`<br>`Trust Management: Defining the Challenge`<br>`Trust Management: Developing Conventions Using Trust Vectors` |
| **D3.2** | **Reader Registrar Operational Specification: Staged Domestic to Cross-Border Deployment** | Implementation profile detailing Reader Registrar architecture, Reader ID Certificate profiles, Reader Trust List (RICAL) publication, and the staged deployment roadmap: starting in a single legal jurisdiction and expanding to cross-border federated networks. | `Trust Management: Mechanisms to Promote & Enforce Conventions`<br>SIDI-Hub White Papers |
| **D3.3** | **Global Reader and Wallet Certification Profile for Verifier Networks** | {If Possible} Normative conformance and testing criteria for third-party evaluation of Reader Authentication, collection limitation enforcement, Justification Label rendering, and wallet triple-barrier receipt storage.&nbsp;&nbsp; | `VDC Best Practices - v0.3`<br> `Better Identity Coalition Code of Conduct`<br> |
| **D3.4** | **Vertical Market Credential Selection and Filtering Guidelines** | Operational guidelines for Verifier Network Operators to consume external Issuer Trust Lists and metadata, evaluate credential applicability, and publish vertical-market acceptance/rejection policies for relying parties. | ISO/IEC 18013-5 / 18013-7<br>AAMVA mDL Implementation Guidelines |

---

## 6\. Milestones

| Estimated Target Date\* | Milestone |
| :---- | :---- |
| **Month 1 (2026-12)** | WG3 Charter formally approved by FG-TIDA Plenary; call for contributors and editors issued. |
| **Month 3 (2027-02)** | First working draft of **D3.1 (Verifier Network Architecture)** and **D3.2 (Reader Registrar Specification)** uploaded to repository. |
| **Month 5 (2027-04)** | Interim review of Stage 1 (single-jurisdiction deployment profile) with national regulator liaisons; first draft of **D3.3 (Certification Profile)**. |
| **Month 7 (2027-06)** | First draft of **D3.4 (Credential Selection Guidelines)**; joint workshop with vertical market associations (Banking, Payments, Retail). |
| **Month 9 (2027-08)** | Stable drafts of **D3.1**, **D3.2**, and **D3.3** frozen for broad public and liaison review. |
| **Month 11 (2027-10)** | Working Group agreement on all four deliverables; submission to FG-TIDA Plenary for formal adoption. |
| **Month 12 (2027-12)** | Submission of approved deliverables to ITU-T Study Group 17 (Security) for progression toward formal ITU-T Recommendations. |

&nbsp;

\*To be clarified as WG3 scales with members and determines the scope of its own course

---

## 7\. Coordination, Dependencies and Liaisons

| Group / Organization | Coordination or Dependency |
| :---- | :---- |
| **ITU-T Study Group 17 (SG17)** | Primary parent study group. WG3 will coordinate closely on security architecture, identity management (Question 10/17), and formal recommendation progression. |
| **FG-TIDA WG1 & WG2** | Harmonization with WG1 (Terminology and Use Cases) and WG2 (Architecture and Security Models) to ensure foundational alignment across FG-TIDA deliverables. |
| **European Union Government-led Reader Registries (27 Member States)** | Enablement of Government-led Registries required by EUDI ARF and the implementing acts that set timelines for Regulated Use Cases. |
| **ISO/IEC JTC 1/SC 17 (Cards and Security Devices for Personal Identification)** | Coordination regarding ISO/IEC 18013-5 (mDL proximity), 18013-7 (web engagement), and 23220 series (building blocks) to align Reader Authentication data elements and certificate profiles. |
| **OpenID Foundation (OIDF)** | Coordination on OpenID for Verifiable Presentations (OID4VP), OpenID Federation, and digital credential protocols. |
| **Kantara Initiative** | Alignment with Kantara's Privacy Enhancing Mobile Credentials (PEMC) program, Advanced Notice & Consent Receipts (ANCR), and Trust Mark assessment frameworks. |
| **Better Identity Coalition (BIC)** | Integration of voluntary best practices, codes of conduct for relying parties, and collection limitation principles. |
| **United Nations & Policy Bodies (via TIDA.community)** | Engaging international policy makers, data protection commissioners, and UN trade bodies to align cross-border trust conventions with international human rights and digital sovereignty standards. |
| **Vertical Market Consortia (EMVCo, W3C Web Payments, Global Banking Federations)** | Ensuring VNO specifications meet high-throughput, low-latency, and cross-border settlement requirements. |
| **Fido Alliance** | Dovetail operational reference architectures and the needs of VNOs with any certification schemes for Wallets or Readers that Fido may develop. |
| Legal and Civil Society (Consumer Advocate) Groups | Review of reference architectures to ensure that consumer concerns and protections can be built and enforced by VNOs when appropriate.  Similar review for legal compliance (e.g., GDPR) |

---

## 8\. Terminology

The Working Group will strictly adhere to the standardized terminology established in the SIDI-Hub / TIDA Trust Management corpus. Key terms are defined as follows:

| Term | Meaning |
| :---- | :---- |
| **Verifier Network Operator (VNO)** | The central orchestrating entity, consortium, or business league responsible for managing a network of relying parties within a vertical market, enforcing binding Conventions, and overseeing Reader Registrars. |
| **Reader Registrar** | A deputized or self-organized authority operating a Trust Mechanism to evaluate verifier compliance with Conventions, issue cryptographic Reader ID Certificates, and publish Reader Trust Lists. |
| **Conventions** | Specific, enforceable policies, rules, and guidelines derived from operational and participant considerations that govern how participants behave and utilize Trust Mechanisms. |
| **Trust Vectors** | The six directional trust relationships within digital credential transactions (*Issuer Trusts Wallet*, *Reader Trusts Wallet*, *User Trusts Verifier*, *Reader Trusts Issuer*, *Ecosystem Trusts Reader*, *User Trusts Wallet*). WG3 focuses specifically on the verifier-centric vectors. |
| **Trust Mechanisms** | Standardized technical tools and methods (such as Reader Trust Lists, OpenID Federation endpoints, and revocation registries) used to inspect participant conformity. |
| **Trust Elements** | The verifiable cryptographic artifacts (Reader ID Certificates, Trust Marks, Wallet Attestations, eSeals, and public keys) conveyed during interactions to demonstrate compliance. |
| **Reader Authentication** | The interactive, cryptographic process wherein a Reader presents a verified Reader ID Certificate to a User's Wallet prior to requesting identity attributes. |
| **Reader Certificate Authority List (RICAL)** | A signed, discoverable trust list containing authorized Reader Root and Intermediate CA certificates distributed to wallets for local certificate validation. |
| **Justification Labels** | Standardized, human-readable labels presented in the wallet UI at request time that link specific requested attributes directly to legal, regulatory, or business risk justifications. |
| **Triple-Barrier Isolation** | A privacy architecture ensures wallet transaction receipts are encrypted locally under the user's sole key, isolated from Issuer surveillance, Relying Party tracking, and OS platform access. |

---

## 9\. Use Cases

The primary use case driving this Working Group is (will be) documented in the FG-TIDA repository as:

- **`verifier-network-operator-use-case.md`** (*Verifier Network Operator — Building Conventions for Vertical Market Risk Mitigation*).

This foundational use case details the step-by-step lifecycle of a Verifier Network Builder organizing telecom, banking, or payment relying parties to safely accept Verifiable Digital Credentials across domestic and international borders.

In addition to this primary use case, WG3 may capture and profile representative vertical scenarios, including from the following list:

1. **Regulated Cross-Border Financial Services:** Mutual onboarding of multi-jurisdictional financial verifiers accepting digital IDs under Anti-Money Laundering (AML) / Know-Your-Customer (KYC) rules without creating cross-border data leakage.  
2. **Age-Restricted E-Commerce and Proximity Retail:** In-person and web-based age verification utilizing zero-knowledge selective disclosure, completely eliminating full date-of-birth collection.  
3. **Healthcare Delivery:** Mobile contactless or remote enrollment enforcing strict data minimization and allowing derivation of a Healthcare ID used across a Restricted Healthcare Ecosystem.  Potentially also the operation of Healthcare registrars within that Ecosystem.  
4. **Global Payments**: The extension of payment networks handling card data for mixed-mode readers that handle Identity checks, Age checks, and consumer payment.

All use cases developed within WG3 will be submitted to the FG-TIDA Terminology and Use Cases group in compliance with the ITU-T A.7 process.

---

## 10\. Working Methods

The Working Group will operate according to the following collaborative principles:

- **Open and Inclusive Collaboration:** Participation is open to all ITU members, FG-TIDA participants, academia, civil society representatives, and invited experts, utilizing the TIDA community open infrastructure.  
- **Meeting Cadence:** The group will meet virtually on a bi-weekly basis, supplemented by face-to-face working sessions collocated with FG-TIDA plenary of FG meetings.  
- **Repository-Driven Drafting:** All specifications, drafts, and issue tracking will be conducted openly on GitHub within the FG-TIDA working group repository. Contributions and revisions follow standard open-source pull request workflows.  
- **Consensus-Based Decision Making:** Deliverables will be progressed through consensus as defined in ITU-T Recommendation A.7.  
- **Staged Implementation Focus:** Drafting will adhere strictly to a two-stage development paradigm, validating operational specifications against single-jurisdiction pilot implementations before generalizing to multi-jurisdictional cross-border federations.

---

## 11\. Security and Privacy Considerations

The technical output of WG3 places user privacy, human-centricity, and transaction security as non-negotiable architectural requirements:

- **Elimination of Surveillance Capitalism:** Specifications will strictly prohibit relying parties from utilizing digital credentials, attribute presentation sessions, or transaction receipts for corporate surveillance, behavioral tracking, or targeted advertising.  
- **Enforced Data Minimization:** Reader specifications will mandate selective disclosure and zero-knowledge proofs (e.g., age thresholds over full birthdates) whenever supported by the underlying credential data model.  
- **Mitigating "Identity-on-Demand":** Guidelines will require verifiers to establish explicit, documented risk justifications for requesting identity attributes, actively preventing the normalization of routine identity checks for low-risk online browsing.  
- **Cryptographic Reader Integrity and Rapid Delisting:** Specifications for Reader Registrars will mandate rapid revocation and delisting mechanisms capable of propagating revoked Reader ID Certificates across distributed Reader Trust Lists within fifteen minutes of confirmed compromise or convention breach.  
- **Triple-Barrier Receipt Isolation:** WG3 will profile wallet-reader interaction requirements ensuring that post-transaction receipts are processed internally within user-controlled encrypted storage, fully isolated from issuer "phone-home" tracking, relying party re-identification, and operating system platform exploitation.

---

## 12\. Success Criteria and Conclusion

The Working Group will have completed its chartered mandate when:

1. Deliverables **D3.1**, **D3.2**, **D3.3**, and **D3.4** achieve formal consensus within WG3 and are adopted by the FG-TIDA Plenary.  
2. At least one production or pilot reference implementation demonstrates the end-to-end operation of a Reader Registrar in a single domestic jurisdiction, validating the issuance and wallet-side verification of Reader ID Certificates.  
3. A formal transition plan is executed transferring the approved deliverables to **ITU-T Study Group 17** for formal standardization as ITU-T Recommendations.  
4. Global certification authorities (such as Kantara Initiative and recognized testing laboratories) officially acknowledge and adopt the conformance criteria defined in Deliverable D3.3.

Following completion of these deliverables, WG3 will conclude its focus group activities or transition into a permanent Question rapporteur group under ITU-T SG17.

---

## 13\. Revision History

| Version | Date | Change |
| :---- | :---- | :---- |
| **0.1** (Proposed by https\://github.com/adk-decipher-id) | 2026-11-10 | Initial Working Group 3 Charter draft prepared for FG-TIDA consideration, based on `verifier-network-operator-use-case.md` and the SIDI-Hub / TIDA Trust Management corpus. |

&nbsp;
