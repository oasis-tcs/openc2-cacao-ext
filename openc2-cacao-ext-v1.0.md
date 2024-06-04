
![OASIS Logo](https://docs.oasis-open.org/templates/OASISLogo-v3.0.png)

-------

# OpenC2 Extension for CACAO Version 1.0

## Committee Specification Draft 01

## 08 May 2024

&nbsp;

<!-- URI list start (commented out except during publication by OASIS TC Admin)

#### This stage:
https://docs.oasis-open.org/openc2/openc2-cacao-ext/v1.0/csd01/openc2-cacao-ext-v1.0-csd01.md (Authoritative) \
https://docs.oasis-open.org/openc2/openc2-cacao-ext/v1.0/csd01/openc2-cacao-ext-v1.0-csd01.html \
https://docs.oasis-open.org/openc2/openc2-cacao-ext/v1.0/csd01/openc2-cacao-ext-v1.0-csd01.pdf

#### Previous stage:
N/A

#### Latest stage:
https://docs.oasis-open.org/openc2/openc2-cacao-ext/v1.0/openc2-cacao-ext-v1.0.md (Authoritative) \
https://docs.oasis-open.org/openc2/openc2-cacao-ext/v1.0/openc2-cacao-ext-v1.0.html \
https://docs.oasis-open.org/openc2/openc2-cacao-ext/v1.0/openc2-cacao-ext-v1.0.pdf

URI list end (commented out except during publication by OASIS TC Admin) -->

#### Technical Committee:
[OASIS Open Command and Control (OpenC2) TC](https://www.oasis-open.org/committees/openc2/)

#### Chairs:
Duncan Sparrell (duncan@sfractal.com), [sFractal Consulting LLC](https://www.sfractal.com/) \
Michael Rosa (mjrosa@nsa.gov), [National Security Agency](https://www.nsa.gov/)

#### Editor:
David Lemire (david.lemire@hii-tsd.com), [National Security Agency](https://www.nsa.gov/)

#### Additional artifacts:
This prose specification is one component of a Work Product that also includes:
* XML schemas: (list file names or directory name)
* Other parts (list titles and/or file names)
* `(Note: Any normative computer language definitions that are part of the Work Product, such as XML instances, schemas and Java(TM) code, including fragments of such, must be (a) well formed and valid, (b) provided in separate plain text files, (c) referenced from the Work Product; and (d) where any definition in these separate files disagrees with the definition found in the specification, the definition in the separate file prevails. Remove this note before submitting for publication.)`

#### Related work:
This specification is related to:
* _Open Command and Control (OpenC2) Language Specification Version 2.0_. Edited by Toby Considine and Duncan Sparrell. Latest stage: https://docs.oasis-open.org/openc2/oc2ls/v2.0/oc2ls-v2.0.html.
* _CACAO-Security-Playbooks-v2.0_. Edited by Bret Jordan and Allan Thomson. Latest stage: https://docs.oasis-open.org/cacao/security-playbooks/v2.0/security-playbooks-v2.0.html.

#### Abstract:
Collaborative Automated Course of Action Operations (CACAO) is a schema and taxonomy for cyber security playbooks. The CACAO specification describes how these playbooks can be created, documented, and shared in a structured and standardized way across organizational boundaries and technological solutions. This extension builds on existing CACAO v2.0 OpenC2 features to improve modularity and utilize the current OpenC2 Transfer Specifications for MQTT (v1.0) and HTTPS (v1.1).

#### Status:
This document was last revised or approved by the OASIS Open Command and Control (OpenC2) TC on the above date. The level of approval is also listed above. Check the "Latest stage" location noted above for possible later revisions of this document. Any other numbered Versions and other technical work produced by the Technical Committee (TC) are listed at https://groups.oasis-open.org/communities/tc-community-home2?CommunityKey=a34c9baf-48b2-44c5-a567-018dc7d32296#technical.

TC members should send comments on this specification to the TC's email list. Others should send comments to the TC's public comment list, after subscribing to it by following the instructions at the "[Send A Comment](https://www.oasis-open.org/committees/comments/index.php?wg_abbrev=)" button on the TC's web page at https://www.oasis-open.org/committees/openc2/.

This specification is provided under the [Non-Assertion](https://www.oasis-open.org/policies-guidelines/ipr/#Non-Assertion-Mode) Mode of the OASIS IPR Policy, the mode chosen when the Technical Committee was established. For information on whether any patents have been disclosed that may be essential to implementing this specification, and any offers of patent licensing terms, please refer to the Intellectual Property Rights section of the TC's web page (https://www.oasis-open.org/committees/openc2/ipr.php).

Note that any machine-readable content ([Computer Language Definitions](https://www.oasis-open.org/policies-guidelines/tc-process-2017-05-26/#wpComponentsCompLang)) declared Normative for this Work Product is provided in separate plain text files. In the event of a discrepancy between any such plain text file and display content in the Work Product's prose narrative document(s), the content in the separate plain text file prevails.

#### Key words:
The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "NOT RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in BCP 14 [[RFC2119](#rfc2119)] and [[RFC8174](#rfc8174)] when, and only when, they appear in all capitals, as shown here.

#### Citation format:
When referencing this specification the following citation format should be used:

**[OpenC2-CACAO-ext-v1.0]**

_CACAO OpenC2 Extension Version 1.0_. Edited by Duncan Sparrell. 08 May 2024. OASIS Committee Specification Draft 01. https://docs.oasis-open.org/openc2/openc2-cacao-ext/v1.0/csd01/openc2-cacao-ext-v1.0-csd01.html. Latest stage: https://docs.oasis-open.org/openc2/openc2-cacao-ext/v1.0/openc2-cacao-ext-v1.0.html.

#### Notices
Copyright © OASIS Open 2024. All Rights Reserved.

Distributed under the terms of the OASIS [IPR Policy](https://www.oasis-open.org/policies-guidelines/ipr/).

The name "OASIS" is a trademark of [OASIS](https://www.oasis-open.org/), the owner and developer of this specification, and should be used only to refer to the organization and its official outputs.

For complete copyright information please see the full Notices section in an Appendix below.

-------

# Table of Contents

- [1 Introduction](#1-introduction)
  - [1.1 Glossary](#11-glossary)
    - [1.1.1 Definitions of terms](#111-definitions-of-terms)
    - [1.1.2 Acronyms and abbreviations](#112-acronyms-and-abbreviations)
    - [1.1.3 Document conventions](#113-document-conventions)
- [2 Key Concepts \& Vocabularies](#2-key-concepts--vocabularies)
  - [2.1 Key Concepts](#21-key-concepts)
  - [2.2 CACAO Vocabulary Modifications](#22-cacao-vocabulary-modifications)
- [3 OpenC2 Commands In CACAO](#3-openc2-commands-in-cacao)
  - [3.1 OpenC2 Command Action Step](#31-openc2-command-action-step)
  - [3.2 Base64 Encoding and Decoding](#32-base64-encoding-and-decoding)
  - [3.3 Invoking OpenC2 via Playbook Action Step](#33-invoking-openc2-via-playbook-action-step)
- [4 OpenC2 CACAO Agents and Targets](#4-openc2-cacao-agents-and-targets)
  - [4.1 OpenC2 CACAO Agents](#41-openc2-cacao-agents)
    - [4.1.1 MQTT Agents](#411-mqtt-agents)
    - [4.1.2 HTTPS Agents](#412-https-agents)
  - [4.2 OpenC2 CACAO Targets](#42-openc2-cacao-targets)
- [5 Conformance](#5-conformance)
- [Appendix A. References](#appendix-a-references)
  - [A.1 Normative References](#a1-normative-references)
  - [A.2 Informative References](#a2-informative-references)
- [Appendix B. Safety, Security and Privacy Considerations](#appendix-b-safety-security-and-privacy-considerations)
- [Appendix C. Acknowledgments](#appendix-c-acknowledgments)
  - [C.1 Special Thanks](#c1-special-thanks)
  - [C.2 Participants](#c2-participants)
- [Appendix D. Revision History](#appendix-d-revision-history)
- [Appendix E. Use Cases and Examples](#appendix-e-use-cases-and-examples)
  - [E.1 Use Cases](#e1-use-cases)
    - [E.1.1 Multiple OpenC2 Consumers With Common Profile](#e11-multiple-openc2-consumers-with-common-profile)
    - [E.1.2 OpenC2 Command With Response Requested](#e12-openc2-command-with-response-requested)
    - [E.1.3 OpenC2 Message Transfer via MQTT](#e13-openc2-message-transfer-via-mqtt)
    - [E.1.4 Extended OpenC2 Consumer Execution Times](#e14-extended-openc2-consumer-execution-times)
  - [E.2 Examples](#e2-examples)
    - [E.2.1 OpenC2 Single Consumer Command / Response via MQTT](#e21-openc2-single-consumer-command--response-via-mqtt)
    - [E.2.2 OpenC2 Multiple Consumer Command / Response via MQTT](#e22-openc2-multiple-consumer-command--response-via-mqtt)
    - [E.2.3 OpenC2 Command / Response via HTTPS](#e23-openc2-command--response-via-https)
- [Appendix F. Notices](#appendix-f-notices)


-------

# 1 Introduction

<!-- All text is normative unless otherwise labeled -->

Introductory text.


## 1.1 Glossary

<!-- Optional section with suggested subsections -->

### 1.1.1 Definitions of terms

### 1.1.2 Acronyms and abbreviations

### 1.1.3 Document conventions

- Naming conventions
- Font colors and styles
- Typographic conventions

---

# 2 Key Concepts & Vocabularies

## 2.1 Key Concepts

- OpenC2 Command
-	OpenC2 Response
-	OpenC2 Actuator Profile
-	OpenC2 Transfer Specification
- CACAO Action Step
- CACAO Agent
- CACAO Target


## 2.2 CACAO Vocabulary Modifications

- `command-type-ov` is extended with the type `openc2`.
- Command type `openc2-http` is deprecated in favor of the non-transport specific `openc2` command type
- `agent-target-type-ov` "Devices and Equipment" vocabulary is extended with the following types:
  -  `openc2-mqtt` agent type for message transfer via MQTT
  -  `openc2-https` agent type for message transfer via HTTPS


---

# 3 OpenC2 Commands In CACAO

This section describes the implementation of OpenC2 commands under CACAO,
including the format and processing of an `openc2 ` command object, the handling
of base64 encoding and decoding, and the invocation of OpenC2 via `openc2`
command objects in a subordinate playbook.

This specification recommends deprecating CACAO's `openc2-http` command type in
favor of the transport-neutral `openc2` command type defined here, in keeping
with OpenC2's intent for the language to be defined in a transport-independent
manner.


## 3.1 OpenC2 Command Action Step

> NOTE: Copying in the `openc2-http` command from the CACAO v2.0 spec as a
> starting point

The `openc2` command represents a command that is intended to be processed via
an OpenC2 Consumer. The delivery of the command and specification of transfer
mechanism and desired OpenC2 AP are handled by defining appropriate CACAO agents
and targets. In addition to the inherited properties of a command object defined
in Section 5.1 of [[CACAO v2.0](#cacao-security-playbooks-v20)], this section
defines the following additional properties that are valid for this type.

The command type open vocabulary (`command-type-ov`) defined in Section 5.2 of
[[CACAO v2.0](#cacao-security-playbooks-v20)] is extended with the new value
`openc2`.

| **Property Name** | **Data Type** | **Details** |
|---|---|---|
| **type** (required) | `string` | The value of this property **must** be `openc2` |
| **command** (required) | `string` |  |
| **content_b64** (required) | `string` | An OpenC2 command that is base64 encoded (see Section 4 of [RFC 4649]). |
| **headers** (optional) | `dictionary` | This property contains headers to be passed to the OpenC2 agent providing message transfer functions. The key for each entry **MUST** be a `string` that uniquely identifies this header. The value for each key **MUST** be a `list` of `string`. |


**Example 3.1 (OpenC2 Command)**

```json
{
  "type": "openc2-http",
  "command": "POST /api1/newObjects/ HTTP/1.1",
  "content_b64": "ewogICJoZWFkZXJzIjogewogICAgInJlcXVlc3RfaWQiOiAiZDFhYzA0ODktZWQ1MS00MzQ1LTkxNzUtZjMwNzhmMzBhZmU1IiwKICAgICJjcmVhdGVkIjogMTU0NTI1NzcwMDAwMCwKICAgICJmcm9tIjogIm9jMnByb2R1Y2VyLmNvbXBhbnkubmV0IiwKICAgICJ0byI6IFsKICAgICAgIm9jMmNvbnN1bWVyLmNvbXBhbnkubmV0IgogICAgXQogIH0sCiAgImJvZHkiOiB7CiAgICAib3BlbmMyIjogewogICAgICAicmVxdWVzdCI6IHsKICAgICAgICAiYWN0aW9uIjogImRlbnkiLAogICAgICAgICJ0YXJnZXQiOiB7CiAgICAgICAgICAiaXB2NF9jb25uZWN0aW9uIjogewogICAgICAgICAgICAicHJvdG9jb2wiOiAidGNwIiwKICAgICAgICAgICAgInNyY19hZGRyIjogIjEuMi4zLjQiLAogICAgICAgICAgICAic3JjX3BvcnQiOiAxMDk5NiwKICAgICAgICAgICAgImRzdF9hZGRyIjogIjE5OC4yLjMuNCIsCiAgICAgICAgICAgICJkc3RfcG9ydCI6IDgwCiAgICAgICAgICB9CiAgICAgICAgfSwKICAgICAgICAiYXJncyI6IHsKICAgICAgICAgICJzdGFydF90aW1lIjogMTUzNDc3NTQ2MDAwMCwKICAgICAgICAgICJkdXJhdGlvbiI6IDUwMCwKICAgICAgICAgICJyZXNwb25zZV9yZXF1ZXN0ZWQiOiAiYWNrIiwKICAgICAgICAgICJzbHBmIjogewogICAgICAgICAgICAiZHJvcF9wcm9jZXNzIjogIm5vbmUiCiAgICAgICAgICB9CiAgICAgICAgfSwKICAgICAgICAicHJvZmlsZSI6ICJzbHBmIgogICAgICB9CiAgICB9CiAgfQp9",
  "headers": {
    "Content-Type": [
      "application/openc2+json;version=1.0"
    ]
  }
}
```

The content of the above base64 command (**command\_b64**) is the encoded
version of the openc2-http content that is shown below (decoded version). The
command content is shown as text for illustration purposes only.

```json
{
  "headers": {
    "request_id": "d1ac0489-ed51-4345-9175-f3078f30afe5",
    "created": 1545257700000,
    "from": "oc2producer.company.net",
    "to": [
      "oc2consumer.company.net"
    ]
  },
  "body": {
    "openc2": {
      "request": {
        "action": "deny",
        "target": {
          "ipv4_connection": {
            "protocol": "tcp",
            "src_addr": "1.2.3.4",
            "src_port": 10996,
            "dst_addr": "198.2.3.4",
            "dst_port": 80
          }
        },
        "args": {
          "start_time": 1534775460000,
          "duration": 500,
          "response_requested": "ack",
          "slpf": {
            "drop_process": "none"
          }
        },
        "profile": "slpf"
      }
    }
  }
}
```

## 3.2 Base64 Encoding and Decoding

## 3.3 Invoking OpenC2 via Playbook Action Step

---

# 4 OpenC2 CACAO Agents and Targets

## 4.1 OpenC2 CACAO Agents

CACAO agents for OpenC2 correspond to OpenC2 transfer specifications. Each type of OpenC2 CACAO agent supports the use of one transfer protocol for sending OpenC2 commands and receiving OpenC2 responses.

### 4.1.1 MQTT Agents

### 4.1.2 HTTPS Agents

## 4.2 OpenC2 CACAO Targets

OpenC2 CACAO Targets correspond to OpenC2 Actuator Specifications.

> NOTE: determine what, if anything, needs to be defined beyond the correlation of APs and CACAO Targets.

> NOTE: provide examples of CACAO targets for OpenC2 APs

-------

# 5 Conformance
<!-- Required section -->

(Note: The [OASIS TC Process](https://www.oasis-open.org/policies-guidelines/tc-process#wpComponentsConfClause) requires that a specification approved by the TC at the Committee Specification Public Review Draft, Committee Specification or OASIS Standard level must include a separate section, listing a set of numbered conformance clauses, to which any implementation of the specification must adhere in order to claim conformance to the specification (or any optional portion thereof). This is done by listing the conformance clauses here.
For the definition of "conformance clause," see [OASIS Defined Terms](https://www.oasis-open.org/policies-guidelines/oasis-defined-terms-2017-05-26#dConformanceClause).

See "Guidelines to Writing Conformance Clauses":  
http://docs.oasis-open.org/templates/TCHandbook/ConformanceGuidelines.html.

Remove this note before submitting for publication.)


-------

# Appendix A. References

<!-- Required section -->

This appendix contains the normative and informative references that are used in this document.

While any hyperlinks included in this appendix were valid at the time of publication, OASIS cannot guarantee their long-term validity.

## A.1 Normative References

The following documents are referenced in such a way that some or all of their content constitutes requirements of this document.

(Reference sources:
For references to IETF RFCs, use the approved citation formats at:  
http://docs.oasis-open.org/templates/ietf-rfc-list/ietf-rfc-list.html.  
For references to W3C Recommendations, use the approved citation formats at:  
http://docs.oasis-open.org/templates/w3c-recommendations-list/w3c-recommendations-list.html.  
Remove this note before submitting for publication.)


###### [CACAO-Security-Playbooks-v2.0]

CACAO Security Playbooks Version 2.0. Edited by Bret Jordan and Allan Thomson. 27 November 2023. OASIS Committee Specification 01. https://docs.oasis-open.org/cacao/security-playbooks/v2.0/cs01/security-playbooks-v2.0-cs01.html. Latest version: https://docs.oasis-open.org/cacao/security-playbooks/v2.0/security-playbooks-v2.0.html.

###### [OpenC2-Lang-v1.1]

_Open Command and Control (OpenC2) Language Specification Version 1.1_. Edited by Duncan Sparrell and Toby Considine. Latest stage: https://docs.oasis-open.org/openc2/oc2ls/v1.1/oc2ls-v1.1.html

###### [OpenC2-MQTT-v1.0]

Specification for Transfer of OpenC2 Messages via MQTT Version 1.0. Edited by David Lemire. 19 November 2021. OASIS Committee Specification 01. https://docs.oasis-open.org/openc2/transf-mqtt/v1.0/cs01/transf-mqtt-v1.0-cs01.html. Latest stage: https://docs.oasis-open.org/openc2/transf-mqtt/v1.0/transf-mqtt-v1.0.html

###### [OpenC2-HTTPS-v1.1]

_Specification for Transfer of OpenC2 Messages via HTTPS Version 1.1_. Edited by David Lemire. Latest stage: https://docs.oasis-open.org/openc2/open-impl-https/v1.1/open-impl-https-v1.1.html

###### [OpenC2-SLPF-v1.1]

_Open Command and Control (OpenC2) Profile for Stateless Packet Filtering Version 1.1_. Edited by Joe Brule, Duncan Sparrell, and Alex Everett. Latest stage: https://docs.oasis-open.org/openc2/oc2slpf/v1.1/oc2slpf-v1.1.html

###### [RFC2119]

Bradner, S., "Key words for use in RFCs to Indicate Requirement Levels", BCP 14, RFC 2119, DOI 10.17487/RFC2119, March 1997, http://www.rfc-editor.org/info/rfc2119.

###### [RFC8174]

Leiba, B., "Ambiguity of Uppercase vs Lowercase in RFC 2119 Key Words", BCP 14, RFC 8174, DOI 10.17487/RFC8174, May 2017, http://www.rfc-editor.org/info/rfc8174.

## A.2 Informative References

###### [OpenC2-Arch-v1.0]

Open Command and Control (OpenC2) Architecture Specification Version 1.0. Edited by Duncan Sparrell. 30 September 2022. OASIS Committee Specification 01. https://docs.oasis-open.org/openc2/oc2arch/v1.0/cs01/oc2arch-v1.0-cs01.html. Latest stage: https://docs.oasis-open.org/openc2/oc2arch/v1.0/oc2arch-v1.0.html.

###### [RFC3552]
Rescorla, E. and B. Korver, "Guidelines for Writing RFC Text on Security Considerations", BCP 72, RFC 3552, DOI 10.17487/RFC3552, July 2003, https://www.rfc-editor.org/info/rfc3552.

-------

# Appendix B. Safety, Security and Privacy Considerations

> NOTE: Reference the related sections in the OpenC2 Architecture Specification and CACAO v2.0 Playbook Specification


-------

# Appendix C. Acknowledgments

<!-- Required section -->

Note: A Work Product approved by the TC must include a list of people who participated in the development of the Work Product. This is generally done by collecting the list of names in this appendix. This list shall be initially compiled by the Chair, and any Member of the TC may add or remove their names from the list by request. Remove this note before submitting for publication.

## C.1 Special Thanks

<!-- This is an optional subsection to call out contributions from TC members. If a TC wants to thank non-TC members then they should avoid using the term "contribution" and instead thank them for their "expertise" or "assistance". -->

Substantial contributions to this document from the following individuals are gratefully acknowledged:

Participant Name, Affiliation or "Individual Member"

## C.2 Participants

<!-- A TC can determine who they list here, however, TC Observers must not be listed. It is common practice for TCs to list everyone that was part of the TC during the creation of the document, but this is ultimately a TC decision on who they want to list and not list. -->

The following individuals have participated in the creation of this specification and are gratefully acknowledged:

**OpenC2 TC Members:**

| First Name | Last Name | Company |
| :--- | :--- | :--- |
Philippe | Alman | Something Networks
Alex | Amirnovman | Company B
Kris | Anderman | Mini Micro
Darren | Anstman | Big Networks

-------

# Appendix D. Revision History

<!-- Optional section -->

| Revision | Date | Editor | Changes Made |
| :--- | :--- | :--- | :--- |
| specname-v1.0-wd01 | yyyy-mm-dd | Editor Name | Initial working draft |

-------

# Appendix E. Use Cases and Examples

## E.1 Use Cases

### E.1.1 Multiple OpenC2 Consumers With Common Profile

### E.1.2 OpenC2 Command With Response Requested

### E.1.3 OpenC2 Message Transfer via MQTT

### E.1.4 Extended OpenC2 Consumer Execution Times

## E.2 Examples

### E.2.1 OpenC2 Single Consumer Command / Response via MQTT

### E.2.2 OpenC2 Multiple Consumer Command / Response via MQTT

### E.2.3 OpenC2 Command / Response via HTTPS

-------

# Appendix F. Notices

<!-- Required section. Do not modify. -->

Copyright © OASIS Open 2024. All Rights Reserved.

All capitalized terms in the following text have the meanings assigned to them in the OASIS Intellectual Property Rights Policy (the "OASIS IPR Policy"). The full [Policy](https://www.oasis-open.org/policies-guidelines/ipr/) may be found at the OASIS website.

This document and translations of it may be copied and furnished to others, and derivative works that comment on or otherwise explain it or assist in its implementation may be prepared, copied, published, and distributed, in whole or in part, without restriction of any kind, provided that the above copyright notice and this section are included on all such copies and derivative works. However, this document itself may not be modified in any way, including by removing the copyright notice or references to OASIS, except as needed for the purpose of developing any document or deliverable produced by an OASIS Technical Committee (in which case the rules applicable to copyrights, as set forth in the OASIS IPR Policy, must be followed) or as required to translate it into languages other than English.

The limited permissions granted above are perpetual and will not be revoked by OASIS or its successors or assigns.

This document and the information contained herein is provided on an "AS IS" basis and OASIS DISCLAIMS ALL WARRANTIES, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO ANY WARRANTY THAT THE USE OF THE INFORMATION HEREIN WILL NOT INFRINGE ANY OWNERSHIP RIGHTS OR ANY IMPLIED WARRANTIES OF MERCHANTABILITY OR FITNESS FOR A PARTICULAR PURPOSE.

As stated in the OASIS IPR Policy, the following three paragraphs in brackets apply to OASIS Standards Final Deliverable documents (Committee Specification, OASIS Standard, or Approved Errata).

[OASIS requests that any OASIS Party or any other party that believes it has patent claims that would necessarily be infringed by implementations of this OASIS Standards Final Deliverable, to notify OASIS TC Administrator and provide an indication of its willingness to grant patent licenses to such patent claims in a manner consistent with the IPR Mode of the OASIS Technical Committee that produced this deliverable.]

[OASIS invites any party to contact the OASIS TC Administrator if it is aware of a claim of ownership of any patent claims that would necessarily be infringed by implementations of this OASIS Standards Final Deliverable by a patent holder that is not willing to provide a license to such patent claims in a manner consistent with the IPR Mode of the OASIS Technical Committee that produced this OASIS Standards Final Deliverable. OASIS may include such claims on its website, but disclaims any obligation to do so.]

[OASIS takes no position regarding the validity or scope of any intellectual property or other rights that might be claimed to pertain to the implementation or use of the technology described in this OASIS Standards Final Deliverable or the extent to which any license under such rights might or might not be available; neither does it represent that it has made any effort to identify any such rights. Information on OASIS' procedures with respect to rights in any document or deliverable produced by an OASIS Technical Committee can be found on the OASIS website. Copies of claims of rights made available for publication and any assurances of licenses to be made available, or the result of an attempt made to obtain a general license or permission for the use of such proprietary rights by implementers or users of this OASIS Standards Final Deliverable, can be obtained from the OASIS TC Administrator. OASIS makes no representation that any information or list of intellectual property rights will at any time be complete, or that any claims in such list are, in fact, Essential Claims.]

The name "OASIS" is a trademark of [OASIS](https://www.oasis-open.org/), the owner and developer of this specification, and should be used only to refer to the organization and its official outputs. OASIS welcomes reference to, and implementation and use of, specifications, while reserving the right to enforce its marks against misleading uses. Please see https://www.oasis-open.org/policies-guidelines/trademark/ for above guidance.
