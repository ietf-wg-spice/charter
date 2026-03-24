# SPICE Working Group Charter

## Introduction

A digital credential expresses claims about a subject and links them with cryptographic keys. Some sets of claim names have already been defined by the IETF and other standards development groups (e.g., OpenID Foundation).

Digital credentials typically involve at least three entities: issuer, holder, and verifier. An issuer constructs and secures a digital credential for a holder. Holders may be willing either to partially disclose some values of their attributes or to demonstrate some properties about their attributes without disclosing their values. Holders disclose credentials, attributes, or proofs regarding attributes in what is called a "digital presentation" to a verifier.

Some holders may wish to carry more than one digital credential. These credentials, together with associated key material, can be stored in an identity digital wallet.

## Goal

The SPICE WG will analyze existing and emerging IETF technologies and address any remaining gaps to facilitate their application in digital credentials and presentations.

- The JOSE WG is currently standardizing a token format for unlinkability and selective disclosure as specified in JWP/CWP (draft-ietf-jose-json-web-proof). The SPICE WG will profile these token formats for application in digital credentials.

- The OAUTH WG is currently standardizing a token format for unlinkability and selective disclosure in the form of SD-JWT/SD-JWT-VC (draft-ietf-oauth-selective-disclosure-jwt and draft-ietf-oauth-sd-jwt-vc). The SPICE WG will define SD-CWT/SD-CWT-VC, which are analogous to these JWT-based tokens, but based on CWT.

The SPICE WG will coordinate with RATS, OAuth, JOSE, COSE, and SCITT working groups that are working on documents pertinent to the identity and credential space. The SPICE WG will build upon existing cryptographic primitives and will not create new cryptographic primitives.

The SPICE WG will develop digital credential profiles that support various use cases. Requirements for proposed standards in the program of work will be established in coordination with the aforementioned working groups. The profiles developed by the SPICE WG will enable digital credentials to leverage existing IETF technologies.

Privacy by design, confidentiality, and consent will be considered, and implementation guidance will be given for each proposed standard in the program of work.

Privacy and security considerations related to the use of confidential computing, remote attestation, trusted execution environments (TEE), and hardware security modules (HSM) on digital credentials will be developed in coordination with relevant IETF WGs (e.g., TEEP) and incorporate feedback from experts on the mailing list.

Privacy and security considerations regarding redaction, linkability and selective disclosure will be developed for proposed standards in the program of work.

SPICE will be inspired by the conceptual data model of the W3C VC but will not work on the Resource Description Framework (RDF) data models.

## Out of Scope

- General Key discovery is out of scope for this WG. There are several mechanisms for distributing or discovering key material (e.g., https://openid.net/specs/openid-connect-discovery-1_0.html).

## Program of Work

- An informational Architecture that defines the terminology (e.g., Issuer, Holder, Verifier, Claims, Credentials, Presentations) and the essential communication patterns between roles, such as credential issuance, where an issuer delivers a credential to a holder, and presentation, where a holder delivers a presentation to a verifier.

- A Proposed Standard document defining SD-CWT, a profile of CWT inspired by SD-JWT (from OAuth) that enables digital credentials with unlinkability and selective disclosure.

- A Proposed Standard Metadata & Capability Discovery protocol will be developed for JWT, CWT, SD-JWT, SD-CWT, CWP and JWP using HTTPS/CoAP. This protocol, intended for CBOR-based digital credentials will enable the three roles —issuers, holders and verifiers— to discover supported capabilities, protocols, and formats for keys, claims, credential types and proofs. The design will be inspired by the OAuth "vc-jwt-issuer" metadata work (draft-ietf-oauth-sd-jwt-vc), which supports ecosystems using JSON serialization.
