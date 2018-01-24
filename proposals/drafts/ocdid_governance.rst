
==============
OCDEP: Division Identifier Governance
==============

:Created: 2017-10-26
:Author: Donny Bridges
:Status: Proposed

Overview
========

A formalized governance model for the creation, acceptance, and upkeep of Open Civic Data Division Identifiers (OCDIDs).

Rationale
=========

Recently, a number of civic data organizations, tech companies, and US state governments have expressed interest in taking a greater role in the creation, upkeep, and wider adoption of OCDIDs. Currently, the governance structure for division IDs  as defined in OCDEP2 is "informal... led by the project’s early contributors and informed by the Open Civic Data Google Group." Increased adoption and interest makes this informality untenable for reasons including:

* Bottlenecks arising when large amounts of new identifiers are proposed but only a few people have permission to review and approve pull requests.
* Subject-matter experts and organizations that have extensive experience working with OCDIDs are willing to take greater responsibility, but currently do not have a formal path for doing so.
* Government entities and other local experts who may wish to contribute to the OCDID repository do not have a clear idea of how the process for contribution works, making it more difficult for them to justify contributing.

We propose to formalize this structure in order to relieve some of the burden on those currently responsible for maintaining the repository, as well as allowing those whose work depends on OCDIDs to have more direct control on their upkeep.


Implementation
==============

Roles & Responsibilities
------------------------
``User``
~~~~~~~~
Anyone using OCDIDs may contribute through group discussion, reporting issues, or assisting with subject-matter expertise.
The agreed upon communication channels for each country's community will be publicly displayed in the Open Civic Data documentation.

``Contributor``
~~~~~~~~~~~~~~~
Any individual or organization ``user`` may become a ``contributor`` by submitting a pull request adding, correcting, or aliasing jurisdictional OCDIDs.
First time ``contributors`` will be advised via a CONTRIBUTING.RST to consult with an existing ``committer`` from their country before submitting their first PR.

``Committer`` 
~~~~~~~~~~~~~
``Committers`` have the ability to approve and commit pull requests from ``contributors`` and other ``committers`` within their geographic scope.

* Unless otherwise specified, ``committers`` will be approved for and by their country of residence/expertise. All responsibilities and privileges associated with being a ``committer`` are limited to issues within that country's community.
* A small subset of global ``committers`` will be established, for the sake of international coordination, whose participation may be requested in all votes, regardless of country. These global ``committers`` will not be subject to the responsibilities of communities outside their own country unless otherwise specified.
* Government officials from sub-country jurisdictions who wish to become ``committers`` may choose to limit their scope to their particular jurisdiction, and thus would not be expected to participate in wider conversations or actions.
* Having ``committer`` authority in a country does not entitle an individual to any authority outside that country. Any ``committer`` wishing to contribute outside of their geographic scope MUST adhere to the processes and procedures of that country's community. Failure to do so may result in the revocation of ``committer`` status.
* Country-based communities may, through consent of their community's ``committers``, choose to adapt this governance model and its processes to better suit their needs.

An initial cohort of ``committers`` will be determined by current project contributors. A public list of ``committers`` will be maintained in a separate OCDEP.

A separate ``committers`` communication channel for each country-based community will be established. A list of each country's ``committer`` email addresses will be maintained and email will be used to conduct official actions unless otherwise specified. 

Any individual who is a ``contributor`` and who agrees to the responsibilities listed here may request to become a ``committer``via a country's agreed upon communication channel. That request will then be shared with the group of that country's current ``committers`` for approval. 

* There will be a two month period where existing ``committers`` may raise objections to a request, otherwise the request will be considered approved.
* In the case that an objection is raised, a discussion and vote will be had amongst the country's existing ``committers``, with a simple majority necessary for approval.
* A majority of a country's ``committers`` participation is necessary for a quorum on all voting matters.

``Committers`` will be approved on an individual basis. Multiple ``committers`` from the same organization are permitted, though should be limited to a reasonably small set of individuals. Organizations should work with the current ``committer`` cohort to ensure that new members are approved in a timely manner and to transition departing members out of the community if necessary. 

``Committers`` are expected to participate in good faith in approval, support, maintenance, and other community related activities or may have their ``committer`` status revoked. A ``committer`` who believes the behavior of another ``committer`` is detrimental to the project should take the following steps:

* Discuss the behavior of concern with the individual privately, expressing why you believe the behavior is detrimental.
* If the behavior is still not resolved, bring the behavior to the attention of the country's group of ``committers`` via the country's agreed upon communication channel. This group should include the party whose behavior is in question, and should again describe the behavior and why it is detrimental to the project.
* If this discussion does not resolve the behavior, start a thread with all the country's ``committers`` except the source of the behavior requesting a vote on revocation. 
* Each ``committer`` may then vote yes, no, or abstain, with non-response implying abstention. "No" votes should provide their reasoning for voting as such.
* After all votes are received or, after a reasonable amount of time (a few days) has passed and a quorum is reached, the votes are then evaluated.
* For the request to revoke commit access to pass it must receive "Yes" votes from two thirds of the country's existing committers.
* The original person to propose revocation summarizes the result of the vote in an email to all existing ``committers`` excepting the candidate for removal.
* If the vote to revoke commit access passes access is removed, the candidate for revocation is informed of that fact, and given the reasons for revocation as documented in the message requesting the vote.
* If the revoked ``committer`` continues to publicly advocate for their point of view in the community after having access revoked, the reasoning for removing commit access as described in the request for a vote will be published to the community.
* (This process is heavly borrowed from the Open vSwitch revocation policy: http://docs.openvswitch.org/en/latest/internals/committer-grant-revocation/)


Contribution Process
--------------------
General contributions
~~~~~~~~~~~~~~~~~~~~~
Any ``contributor`` may create a pull request for generative IDs, corrections, aliases, etc. 

* A pull request from a ``contributor`` will be considered accepted when reviewed by and approved by two of the country's ``committers`.
* If the contribution is from a current ``committer`` in good standing with the country's community, only one additional ``committer`` review is necessary.
* No two members of the same organization may be involved in the acceptance of a pull request.

Commits should be reviewed within 2 weeks of a pull request. Accelerated timeline needs should be communicated via the country's communication channels.

Some local division identifiers, such as those for special districts in the US, may be difficult to verify for anyone besides the pull request submitter. ``Committers`` should consider the both the source as well as the scope of the change requested in determining the level of scrutiny necessary for approving a pull request.

If pull requests are languishing due to ``committer`` inaction, a country's ``committers`` may implement a mechanism for automatically approving a pull request after a certain time. 

* Ex: "If, after two months there is neither a formal approval or an ongoing conversation around a request, that request will be sent to all the country's committers for a final opportunity to object or approve. If no objection is made within a reasonable amount of time (a few days), the request will be considered approved."
* This mechanism may be restricted to specific types of identifiers, or prohibit automatic approval for high-level types.
* Such a mechanism may be considered adopted if upon proposal it receives a majority vote from the country's ``committers``.
* No such mechanism may be added for the top level OCDID hierarchy (``ocd-division/country:``) or for countries who would otherwise not have any identifiers.

If a conversation around a request cannot reach consensus, after two months the person who made the pull request may request a final vote from the country's ``committers``.

Approval will be handled on a per-file, rather than a per-commit, basis.

New commits should include well-formed explanations, especially if generating new IDs or types.

Formalized guidelines for approval will be created for use by ``committers``. These guidelines will include:

* Syntax check guidelines
* Type check guidelines and a glossary of existing types
* Dupe check guidelines
* Instructions for including and checking for correct sameAs aliasing
* Differentiating standards of review between generative/corrective requests

Government contributions
~~~~~~~~~~~~~~~~~~~~~~~~
Should a government entity wish to contribute to the repository, they will initially be asked to work directly with an existing ``committer`` to prepare to integrate their identifier set.

* A second ``committer`` is still required for approving government contributions, even if a government contributor becomes a ``committer`` themselves.
* Even so, government contributors should be given wide deference within their geographic area.
* If, because of naming conventions, geographic edge cases, etc. a government contributor requests a deviation from existing OCDID nomenclature, the community will attempt to reasonably accommodate that request (e.g. using “police_jury” as a type in lieu of “county_council” for Louisiana's county legislative body)

Government entities (and the ``committers`` they work with) will be expected to reconcile and appropriately alias these cases with existing OCDIDs in order to ensure maximum compatibility.

Identifiers created by government officials that are used in official data will be marked as such in the repository, so that developers can quickly identify the preferred identifier in case of conflict. Caution should be used, and the original submitter consulted with if possible, before changing government submitted identifiers.

A section of documentation specifically aimed at government staff will be created, where they can learn more about the project and how to get involved, as well as how to reach out to the community to get help.

Support
--------
``Committers`` will be expected to participate in a quarterly review of their country's new OCDIDs in order to ensure quality on-going.
``Committers`` will be requested to contribute and maintain an ongoing style guide for creating new district types.
``Committers`` will be required to participate in > 60% of their country's formal votes/actions as announced.


Copyright
=========

This document has been placed in the public domain per the Creative Commons
CC0 1.0 Universal license (http://creativecommons.org/publicdomain/zero/1.0/deed).


