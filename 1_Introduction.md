# Introduction

## Purpose

NIST Special Publication 800-63-A Digital Authentication Guideline: Enrollment and Identity Proofing (SP 800-63 or NIST SP 800-63A) provides detailed requirements for enrollment and identity proofing of individuals with which federal identity management systems are expected to comply.

This document provides non-normative guidance to agencies and service providers on possible techniques to implement identity management systems which are aligned with the requirements contained in NIST SP 800-63A. This guide leverages real world examples and illustrative cases to provide practical and actionable guidance to readers. It is complemented by the following additional implementation guides, which, taken in their entirety, provide an end-to-end vision for Federal Identity and Access Management Solutions:

>Paul: The documents are more than the above paragraph. They provide a level of detail on how to achieve the requirements in the SPs. And we should have a warning that these guides may result in future normative requirements in the SP suite.

1. Digital Identity Risk Management Implementation Guidance
2. Authentication and Lifecycle Management Implementation Guidance
1. Federation Implementation Guidance

Ultimately, these documents support the overall vision of NIST SP 800-63-3 by enabling a more comprehensive understanding of what compliant identity solutions could look like in the wild.

> **The material contained in this document is intended to be illustrative rather than prescriptive, and does not supersede the requirements stated in the core NIST SP 800-63-3 Digital Authentication Guideline.** 

## Identity Proofing

Identity proofing is the process by which a Credential Service Provider (CSP) collects and verifies information about a person for the purpose of issuing credentials to that person. Processes implemented, illustrated in Figure 1 and consistent with the requirements in NIST SP 800-63-3, are intended to help agencies achieve the following objectives:

- **Resolve** a claimed identity to a single, unique identity within the context of the population of users served by the CSP.
- **Validate**
	- that all evidence that is supplied is valid (correct) and genuine (not counterfeit or misappropriated); and
	- that the claimed identity exists in the real world.
- **Verify** that the claimed identity is associated with the real person supplying the identity evidence.

>Paul: Please make sure to properly link to the diagram. You can check out the SP suite for examples.
  
![Figure 1: Individual Identity Proofing Journey](media/figure-1-individual-identity-proofing-journey.png)

**Figure 1:** Individual Identity Proofing Journey

>Paul: need a closing statement rather than a hanging graphic.
