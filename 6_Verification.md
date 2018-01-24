# Verification

The goal of identity verification is to confirm and establish a linkage between the claimed identity and the physical, live existence of the person actually presenting the evidence. This can be done by a physical or biometric comparison, or a KBV challenge, or by authenticating the applicant with methods and credentials that are appropriate for the level of assurance.

Table 4-3 in SP800-63A details the verification methods necessary to achieve successful verification at the appropriate levels of strength. The strength of an evidence verification system can be assessed using this information; to achieve proofing at IAL 2, at a minimum, the applicant must be verified by a process that is able to achieve a strength of STRONG. 

In the following sections we will discuss the identity verification methods listed in Table 4-3 in SP800-63A.

## KBV

This technique presents the applicant with a series of questions to help distinguish the applicant from other known identities. The information in KBV systems can be  obtained from publicly available databases to avoid the leakage of sensitive, non-public information.

KBV systems can also be used in the resolution stage of the identity proofing process. 

Detailed requirements for knowledge based verification have been specified in Section 5.3.2 in SP800-63A. 

The quality and availability of the data used in the KBV process results in varying degrees of confidence and CSP’s should consider the quality when when making decisions on the utilization and outcome of KBV. The CSP should follow a set of four fundamental principles in KBV design (The UK government’s [Identity Proofing and Verification (IPV) Operations Manual](https://www.gov.uk/government/uploads/system/uploads/attachment_data/file/383109/IPV_Operations_Manual_v2.3.1_Redacted.pdf) and [Good Practice Guide (GPG) 45](https://www.ncsc.gov.uk/content/files/guidance_files/GPG%2045%20%20-%20validating%20and%20Verifying%20the%20identity%20of%20an%20individual%20-%20issue%202.4%20-%20NCSC%20Web.pdf) have been used as a reference to build the baseline guidance presented in this document):
- Clarity –process must be clear so that applicant can understand and correctly respond
    - Relevant, sensible, proportionate
    - Carefully constructed, clear, obvious as to what is being asked of the applicant
    - Expectation that owner of claimed identity can reasonably complete process
- Breadth –process should cover a wide range of information
    - Based on a range of information and not one single source
    - Covering different evidence categories
    - Security –process must protect claimed identity from impersonation
    - Constructed so that loss or theft would not provide required information to pass
    - Must not be used where it is known or likely to be in the public domain
    - Multiple choice answers must be plausible and not easily guessed
    - Multiple questions should not be answering one another
    - Answers cannot be researched from public domain or social media
    - Must minimize risk of impersonation by close family member
    - Answers to multiple questions should not have been provided to applicant earlier in workflow
    - Must not reveal personal information that has not been provided by applicant
- Sources –process must use suitable sources
    - Organization that captures or generates original data, not intermediary
    - Data originating from separate acceptance and proofing processes within a source can be considered a separate source
    - Source used for KBV must be independent from applicant
    - Where source of KBV is the proofing organization method delivering to claimed identity and not applicant must be used

Three levels should be considered in evaluating quality of KBV data, as shown in Table 5.

| **KBV Quality** | **Properties of KBV Data** |
| --- | --- |
| Low | Pertinent to claimed identity<br/>Can be researched with little financial commitment and with ease<br/>Source of KBV data protects integrity of KBV data |
| Medium | Pertinent to claimed identity<br/>Can be researched with little financial commitment and with ease<br/>Source of KBV data protects integrity of KBV data<br/>Source of KBV data confirmed claimed identity through a proofing process<br/>KBV data not known or likely to be in public domain<br/>KBV data may be available to others or friends and relations, but not without a financial commitment that would be a deterrent or a time commitment that would noticeably delay the user’s ability to provide correct answer during KBV<br/>Source of KBV data protects confidentiality of KBV data<br/>Where KBV data is a shared secret delivery mechanism is confirmed as linked to claimed identity<br/>Where KBV data is a shared secret delivery mechanism for shared secret means it can reasonably be assumed to have been delivered into possession of claimed identity<br/>KBV data is dynamic |
| High | Pertinent to claimed identity<br/>Can be researched with little financial commitment and with ease<br/>Source of KBV data protects integrity of KBV data<br/>Source of KBV data confirmed claimed identity through a proofing process<br/>KBV data not known or likely to be in public domain<br/>KBV data may be available to others or friends and relations, but not without a financial commitment that would be a deterrent or a time commitment that would noticeably delay the user’s ability to provide correct answer during KBV<br/>Source of KBV data protects confidentiality of KBV data<br/>Where KBV data is a shared secret delivery mechanism is confirmed as linked to claimed identity<br/>Where KBV data is a shared secret delivery mechanism for shared secret means it can reasonably be assumed to have been delivered into possession of claimed identity<br/>KBV data is dynamic<br/>KBV data is no older than 45 days<br/>Where KBV data is a shared secret delivery mechanism for shared secret ensured it was delivered into possession of claimed identity<br/>Source of KBV data confirmed claimed identity in manner that complies with US AML regulations<br/>KBV data not in public domain including any public registers<br/>KBV data not known to others beside owner of claimed identity (and immediate family)<br/>Someone other than claimed identity cannot obtain KBV data without committing either a civil or a criminal offense<br/>Source of KBV data has security practices that prevent unauthorized access, modification or generation of KBV data by insiders, alone or with outside coercion<br/>Source of KBV data is subject to regulation by a statutory or independent body<br/>Source of KBV data is reliable and independent from service providing the proofing |

**Table 5:** KBV Data Quality

In general the distinction between static and dynamic knowledge-based verification is made based on whether the security questions are stored by the CSP for later access, or generated as applicable to the end user only using specific information, publicly available or otherwise. Static examples such as mother’s maiden name or previous address would not change over time.
While in a broad sense only dynamic KBV is considered for the purposes of identity proofing, it should be noted that there are risks associated with using publicly available data, as there is with secured data that has the risk of compromise. As a general rule of thumb, data used for KBV needs to be as “secret” as possible. Micro-deposits and transaction codes as a form of dynamic KBV are known to work efficiently.
As a guideline, the following can be adopted by CSP’s to perform KBV for resolution or verification.
If the CSP allows the applicant to suspend and resume the process the applicant should not be able to use this feature to gather information relating to the claimed identity.
If the applicant suspends and resumes the process they should either be presented the same questions as before or given new questions which neither have answers that can be deduced from information provided in the previous questions nor reveal answers to previously asked questions.
If the CSP allows the applicant to suspend and resume the process the CSP should not reveal whether the applicant correctly answered any of the previous questions.
The CSP should only allow the applicant to suspend and resume the process twice, totaling a maximum of three attempts. If the CSP presents the same set of questions upon resumption, further questions should be introduced to prevent attackers from using process to extract information and answer previously given questions.
If the applicant fails to return or fails to complete KBV upon return, KBV should be deemed failed.
To calculate the KBV score for the applicant’s answers to a series of questions, let us use the scoring table shown in Table 6.

<table><tbody>
<tr><th>KBV Quality</th><th colspan=2>Unprompted</th><th colspan=2>Prompted</th><tr>
<tr><td></td><td>Success</td><td>Failure</td><td>Success</td><td>Failure</td></tr>
<tr><td><strong>Low</strong></td><td>2</td><td>-5</td><td>1</td><td>-6</td></tr>
<tr><td><strong>Medium</strong></td><td>4</td><td>-4</td><td>3</td><td>-5</td></tr>
<tr><td><strong>High</strong></td><td>6</td><td>-3</td><td>5</td><td>-4</td></tr>
</tbody></table>

**Table 6:** KBV Scoring Profile

If the CSP keeps separate updated totals of all successful and all failed answers through the KBV process, they can use the following table to deem the user to pass KBV if they achieve a success total score for either of the three scenarios in Table 7 before achieving a failure score seen in the rightmost column of the table for the selected IAL. 

<table><tbody>
<tr><th>IAL</th><th colspan=3>Success Total</th><th>Failure Total</th><tr>
<tr><td></td><td>1st Attempt</td><td>1st Resume</td><td>2nd Resume</td><td></td></tr>
<tr><td><strong>2</strong></td><td>8</td><td>11</td><td>15</td><td>-8</td></tr>
<tr><td><strong>3</strong></td><td>18</td><td>21</td><td>24</td><td>-9</td></tr>
</tbody></table>

**Table 7:** KBV Pass/Fail Scoring

### Example: Resolution

After enrollment, the CSP will resolve all core attributes collected from the applicant into a single identity. In the case of paper/in-person applications some of the resolution steps may require human intervention.

In our IAL2 example, the CSP can leverage identity document image verification software to obtain the full name, address and DOB for an applicant from the image of their driver’s license or passport that they received via the app.

The 24-hour period given to the applicant enables the CSP to handle any exceptions (this could also accommodate the use of human operators where intervention is necessary but we assume for the sake of this example that automated verification software is not available). Once attribute information is produced from the document image, the CSP has two or more sets of attributes for the applicant –one from the application entries provided by the applicant, and one or more from the document(s).

The CSP can then run a matching algorithm, as depicted in the following figure, to obtain a similarity score that reflects the extent to which the different sets of identity attributes resolve, and, comparing this against a threshold, decide success or failure.

![Figure 6: Resolution](https://github.com/usnistgov/800-63A-ImplGuide/blob/master/media/workflow-4-resolution.png)

**Figure 6:** Resolution

## Biometric Capture

Biometrics can play a key role in identity proofing and verification of individuals. This utility can come in multiple stages of the identity proofing process.

In enrollment, CSP’s can capture biometrics in the form of fingerprints, face, iris images, etc. They can compare requirements with their options to identify which single or multi-modal biometric solution can best respond to their needs and implement the system accordingly.

It is important for CSP’s to note that biometrics collected for enrollment in one instance without any biometric verification for identity proofing should not later be used as a proofing source.

In many applications, the biometric samples collected upon enrollment automatically trigger open-set identification. Open-set identification is typically defined as the task to determine if someone is in a database and to find the record of the individual in the database. This “defensive” first-line measure upon enrollment performs de-duplication. In other words, the CSP’s database of identities is surveyed automatically to see if the applicant has an existing identity record. If the deduplication search returns a positive match, CSP’s should match the attributes in the existing identity and the applicant-provided information to determine and adjudicate any mismatches.

CSP’s can also leverage biometrics in the resolution and verification steps as another factor to contribute to the degree of confidence along with other methods such as the fuzzy matching of attributes or knowledge-based verification. Naturally, a CSP can only do this if biometric data exists for the applicant in the databases wherein the reference attributes for resolution and verification reside. As an example, if guidelines and regulations governing the use and sharing of biometric data allow it, the biometric samples collected as part of the enrollment of one CSP can be submitted for a 1:1 verification by another CSP wherein the applicant also has an identity record. In this process the biometrics become another factor, enabling the enrolling CSP to resolve and verify the identity with confidence.

Requirements and differences between collection methods such as in-person, virtual in-person or remote also concern the collection of biometric samples for applicants. Presentation attacks are a matter of concern for unproctored collection use cases. Ongoing work, such as [*SOFA-B: Strength of Authentication for Biometrics*](https://pages.nist.gov/SOFA/SOFA.html), provides guidelines for the strength of biometric authentication systems as a balanced function of presentation attack detection abilities, biometric match accuracy and effort (to attack system).

CSP’s should also note that different biometric modalities provide varying levels of accuracy, presentation attack vulnerability and ease of collection. Existing literature offers deep insight into the trade-off between accuracy, convenience and other factors of biometric authentication. NIST and other authorities have also conducted and orchestrated standardized tests in order to evaluate performances of biometric algorithms developed by participating vendors. CSP’s should use these resources as guidelines when considering the use of biometrics in their implementations.

For an IAL3 system, detection mechanisms should be in place to ensure security of the system against presentation attacks if collection is done remotely. Requirements for virtual in-person collection mitigate the risk of presentation attacks for an IAL3 system.  Requirements in 800-63A should be considered for IAL2 systems.

Limiting the number of consecutive unsuccessful verification attempts also helps to protect a system against presentation attacks. For a system without presentation attack detection, the limit can be set to 3 while for systems that employ presentation attack detection, a maximum of 10 consecutive unsuccessful attempts may be allowed.

## Address Confirmation

CSP’s may require applicants to confirm their address, as outlined in SP800-63A. This is done in the form of an enrollment code sent by the CSP, intended for the applicant to receive at their address of record. Successful provision of the correct code by the applicant to the CSP serves to confirm the address provided by the applicant: The address binds the identity to the applicant’s record.

An example is a scannable image or barcode that is unique to the enrollment, mailed to the applicant’s address of record. Successful scanning and verification of this image or barcode by a mobile application provided in the CSP’s workflow can be used for address confirmation.

### Example: Verification

The CSP completes the identity proofing process by verification. In this step, the identity of the actual individual applying is verified for a match against the individual whose identity information is built using resolution and validation of the documents provided in enrollment. A general outline for the verification process has been shown in the following figure. In our example, the CSP uses the mobile application to perform face verification of the individual which compares a face image submitted by the applicant in the final stage of identity proofing against face images in the background records of the applicant’s driver’s license or passport. For enhanced security, the CSP can in addition use the bank account information provided by the applicant to submit two micro deposits of less than $1 each, and then ask the applicant to complete the final verification step by providing the micro deposit amounts in cents, appended into a 4-digit sequence. Upon successful verification the CSP will issue credentials to the applicant, who can subsequently start using the service.

![Figure 7: Verification](https://github.com/usnistgov/800-63A-ImplGuide/blob/master/media/workflow-5-verification.png)

**Figure 7:** Verification
