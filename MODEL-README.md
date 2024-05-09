## README

![Work Product ReadMe Logo](images/cacao-ext-logo-header.png)

## ![oasis-avatar](https://avatars.githubusercontent.com/u/47402065?s=24&v=4) An OASIS [Work Product](https://www.oasis-open.org/policies-guidelines/oasis-defined-terms-2018-05-22/#dWorkProduct) Repository ![oasis-avatar](https://avatars.githubusercontent.com/u/47402065?s=24&v=4) 

Members of the OASIS [Open Command and Control (OpenC2) Technical
Committee](https://groups.oasis-open.org/communities/tc-community-home2?CommunityKey=a34c9baf-48b2-44c5-a567-018dc7d32296)
use this GitHub repository as part of the [TC's chartered
work](https://www.oasis-open.org/committees/openc2/charter.php).
Contributors must be Members of the TC. Work is governed by the
OASIS policies and is not done under typical open source
licensing. For more details, see the
[Contributions](#writing_hand-contributions-writing_hand) and
[Licensing](#scroll-licensing-scroll) sections below. 

## :blue_book: _OpenC2 Extension for CACAO_ :blue_book:

The [Collaborative Automated Course of Action Operations (CACAO) specification](https://docs.oasis-open.org/cacao/security-playbooks/v2.0/security-playbooks-v2.0.html)
describes how cybersecurity automation playbooks can be created, documented, and
shared in a structured and standardized way across organizational boundaries and
technological solutions. This extension builds on existing [CACAO
v2.0](https://docs.oasis-open.org/cacao/security-playbooks/v2.security-playbooks-v2.0.html)
OpenC2 features to improve modularity and utilize the current OpenC2 Transfer
Specifications for 
[MQTT (v1.0)](https://docs.oasis-open.org/openc2/transf-mqtt/v1.0/transf-mqtt-v1.0.html)
and [HTTPS (v1.1)](https://docs.oasis-open.org/openc2/open-impl-https/v1.1/cs01/open-impl-https-v1.1-cs01.html).

### :twisted_rightwards_arrows: Repository Organization :twisted_rightwards_arrows:

![branches](images/repo-branches.png)

OpenC2 work product repositories are organized a bit differently
than typical open source software project repositories:

* The **Published** (default) branch represents the current,
  stable, approved version of the work product. If the product
  hasn't progressed past an [OASIS Committee Specification Draft
  (CSD)](https://www.oasis-open.org/policies-guidelines/tc-process-2017-05-26/#committeeDraft),
  this branch is essentially empty.
* The **Working** branch is where all work-in-progress content is
  captured, and is the place to go for the [current working
  version]() of this work product.

> In the above bullet about the Working branch edit the `READMD.md` source to insert a link to the working version markdown file in the `working` branch of the repo.

More information about the TC's repository organizing conventions
and branching strategy can be found in our [Documentation
Norms](https://github.com/oasis-tcs/openc2-tc-ops/blob/main/Documentation-Norms.md#433-configure-repository).


### :left_speech_bubble: Description :left_speech_bubble:

The *OpenC2 Extension for CACAO* will provide guidance for specifying the use of
OpenC2 commands and transfer mechanisms in CACAO playbooks in order to
facilitate standardization of OpenC2 use in that contexts.  Specific goals for
this specification include:
- Defining an updated CACAO OpenC2 Command Type not bound to a specific transfer
mechanism (extending/replacing the command-type-ov defined in section 5.2 of the
CACAO v2.0 spec).
- Defining standardized CACAO MQTT and HTTPS Agents for OpenC2 message
transfers.
- Identifying CACAO control flow capabilities needed for OpenC2 (e.g., await
Consumer response) that may be missing from CACAO v2.0 spec.

### :writing_hand: Contributions :writing_hand:
<div>
<p>As stated in this repository's <a href="CONTRIBUTING.md">CONTRIBUTING file</a>, contributors to this repository are expected to be Members of the OASIS OpenC2 TC, for any substantive change requests.  Anyone wishing to contribute to this GitHub project and <a href="https://www.oasis-open.org/join/participation-instructions" target="_blank">participate</a> in the TC's technical activity is invited to join as an OASIS TC Member.  Public feedback is also accepted, subject to the terms of the <a href="https://www.oasis-open.org/policies-guidelines/ipr#appendixa" target="_blank">OASIS Feedback License</a>.</p>
</div>


### :scroll: Licensing :scroll:

<div>
<p>Please see the <a href="LICENSE.md">LICENSE</a> file for description of the license terms and OASIS policies applicable to the TC's work in this GitHub project. Content in this repository is intended to be part of the OpenC2 TC's permanent record of activity, visible and freely available for all to use, subject to applicable OASIS policies, as presented in the repository <a href="LICENSE.md">LICENSE</a> file.</p>
</div>

### :left_speech_bubble:   Further Description of this Repository :left_speech_bubble: 

This repository is designed to support TC members' work on a
formal specification that describes _identify work product_. This
GitHub repository supports development of the content and change
tracking for the _identify work product_ as new working draft
level revisions are created and the associated CSDs mature.

<div>

<p>Members of the <a href="https://groups.oasis-open.org/communities/tc-community-home2?CommunityKey=a34c9baf-48b2-44c5-a567-018dc7d32296" target="_blank">OASIS Open Command and Control (OpenC2) TC</a> create and manage technical content in this TC GitHub repository ( <a href="https://github.com/oasis-tcs/openc2-cacao-ext" target="_blank">https://github.com/oasis-tcs/openc2-cacao-ext</a> ) as part of the TC's chartered work (<i>i.e.</i>, the program of work and deliverables described in its <a href="https://www.oasis-open.org/committees/openc2/charter.php" target="_blank">charter</a>).</p>

<p>OASIS TC GitHub repositories, as described in <a href="https://www.oasis-open.org/resources/tcadmin/github-repositories-for-oasis-tc-members-chartered-work">GitHub Repositories for OASIS TC Members' Chartered Work</a>, are governed by the OASIS <a href="https://www.oasis-open.org/policies-guidelines/tc-process">TC Process</a>, <a href="https://www.oasis-open.org/policies-guidelines/ipr">IPR Policy</a>, and other policies, similar to TC Wikis, TC JIRA issues tracking instances, TC SVN/Subversion repositories, etc.  While they make use of public GitHub repositories, these TC GitHub repositories are distinct from <a href="https://www.oasis-open.org/resources/open-repositories">OASIS Open Repositories</a>, which are used for development of open source <a href="https://www.oasis-open.org/resources/open-repositories/licenses">licensed</a> content.</p>
</div>


###  :envelope_with_arrow: Contact :envelope_with_arrow:
<div>
<p>Please send questions or comments about <a href="https://www.oasis-open.org/resources/tcadmin/github-repositories-for-oasis-tc-members-chartered-work">OASIS TC GitHub repositories</a> to the <a href="mailto:tc-admin@oasis-open.org">OASIS TC Administrator</a>.  For questions about content in this repository, please contact the TC Chair or Co-Chairs as listed on the the <a href="https://groups.oasis-open.org/communities/tc-community-home2?CommunityKey=a34c9baf-48b2-44c5-a567-018dc7d32296">OpenC2 TC's OASIS home page</a>.</p>
</div>


