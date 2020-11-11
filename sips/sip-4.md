---
sip: 4
title: Change Default Vote Delegate Address to self address when not set delegate address
status: WIP
author: Ivan (@Ivan25640306)
discussions-to: https://t.me/SymbloxSIP
created: 2020-11-11
---

<!--You can leave these HTML comments in your merged SIP and delete the visible duplicate text guides, they will not appear and may be helpful to refer to if you edit it again. This is the suggested template for new SIPs. Note that an SIP number will be assigned by an editor. When opening a pull request to submit your SIP, please use an abbreviated title in the filename, `sip-draft_title_abbrev.md`. The title should be 44 characters or less.-->

## Simple Summary

This SIP proposes to change default vote delegate address to self address when not set delegate address

## Abstract
<!--A short (~200 word) description of the technical issue being addressed.-->
In the first vote, many people had votes, but no delegation address was set before the proposal was established, which resulted in some valid votes that could not be voted.


## Motivation
<!--The motivation is critical for SIPs that want to change Symlox. It should clearly explain why the existing protocol specification is inadequate to address the problem that the SIP solves. SIP submissions without sufficient motivation may be rejected outright.-->

Because the voting steps will become simpler to allow more people to participate, it is a reasonable setting to delegate to yourself without setting a delegation address.

## Specification
<!--The technical specification should describe the syntax and semantics of any new feature.-->

### Solidity

## Rationale
<!--The rationale fleshes out the specification by describing what motivated the design and why particular design decisions were made. It should describe alternate designs that were considered and related work, e.g. how the feature is supported in other languages. The rationale may also provide evidence of consensus within the community, and should discuss important objections or concerns raised during discussion.-->

## Test Cases
<!--Test cases for an implementation are mandatory for SIPs but can be included with the implementation..-->

## Implementation
<!--The implementations must be completed before any SIP is given status "Implemented", but it need not be completed before the SIP is "Approved". While there is merit to the approach of reaching consensus on the specification and rationale before writing code, the principle of "rough consensus and running code" is still useful when it comes to resolving many discussions of API details.-->


## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
