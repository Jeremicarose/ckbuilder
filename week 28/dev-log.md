# Builder Track Weekly Report — Week 28

## Focus

Pilot preparation, external receiver-operator recruitment, MLAT validation, and preparing the Receiver Registry for broader testing and potential grant support.

## Completed This Week

- Continued researching and identifying potential ADS-B receiver operators for the Receiver Registry pilot.
- Identified several recent and relevant receiver operators with experience in:
  - readsb
  - SDR/1090 MHz receivers
  - Raspberry Pi receiver setups
  - multiple ADS-B networks
  - receiver relocation and configuration
  - feeder troubleshooting and hardware failures
- Identified several particularly relevant pilot candidates, including operators experiencing:
  - receiver relocation and station identity/location synchronization issues;
  - multi-network feeding from the same receiver;
  - mobile receiver configuration;
  - receiver hardware/feed failures.
- Refined the pilot recruitment approach to focus on genuine receiver operators and their existing workflows, rather than relying primarily on general aviation communities or old MLAT discussions.
- Encountered recruitment restrictions in some communities. After a recruitment post was removed by FlightAware's community moderation for violating its self-promotion policy, shifted toward individual, permission-based outreach and researching active operators before contacting them.
- Refined the validation questions to investigate practical problems around:
  - receiver identity;
  - receiver ownership;
  - receiver relocation;
  - configuration management;
  - multiple-network feeding;
  - receiver downtime and recovery;
  - observation/data provenance.
- Conducted initial testing and feedback sessions with several Web3 developers from the labs in Nairobi. Their feedback was positive and helped identify areas for improving the application before wider external testing.
- Continued evaluating how to position the Receiver Registry as a structured pilot programme rather than only as a technical project.
- Discussed the possibility of creating clearer branding, a defined pilot programme, and potentially a paid tester/operator programme supported by the CKB community.

## Pilot Recruitment Findings

Several recent operators were identified as potentially useful participants:

- Ratty Nz8r — reported moving a receiver and experiencing delays/mismatches involving receiver coordinates, UID, and station name.
- HappyPAPI82 — operates readsb on a Raspberry Pi while feeding multiple aviation networks.
- Lothar_of_the_Hill_People — operates a mobile feeder and actively configures readsb for changing operating locations.
- Railfan-Eric — recently investigated a readsb/tar1090 feeder failure.
- aerspeed — operates a 1090 MHz receiver using a Nooelec SDR, readsb, and tar1090.
- Toumal — experienced a Raspberry Pi hardware failure that interrupted feeding.

These candidates are being treated as potential pilot participants, not confirmed participants.

## Product Validation Direction

The main research question is becoming more focused:

> Does a persistent, owner-controlled, cross-network receiver identity provide enough practical value that receiver operators would actually use or integrate it?

The pilot is therefore being designed to understand the operator's existing workflow before presenting the Receiver Registry as the proposed solution.

The investigation is focusing on:

1. What receiver operators currently do.
2. Problems they encounter with receiver identity and configuration.
3. What happens when a receiver is moved, replaced, transferred, or goes offline.
4. How operators manage the same receiver across multiple networks.
5. How receiver ownership and contribution history are represented.
6. Whether operators would benefit from a portable receiver identity and lifecycle system.
7. What would prevent an operator from adopting such a system.

## Current Status
CKB infrastructure: Validated  
MLAT technical foundation: Validated  
MLAT baseline/data-source research: Completed with conditional GO  
Internal/Web3 testing: Completed  
External operator recruitment: In progress  
Confirmed external pilot participants: Not yet secured  
Receiver Registry pilot: Preparing  
Productisation/branding: Under consideration  
Paid operator programme: Being explored  
Grant proposal: Being strengthened around live pilot validation and potential partnerships

## Next Steps

- Continue identifying active ADS-B receiver operators through recent technical discussions and direct outreach.
- Begin permission-based conversations with the strongest candidates.
- Conduct short operator interviews focused on current workflows and real operational problems.
- Convert suitable operators into a small controlled Receiver Registry pilot.
- Define the pilot programme clearly, including:
  - project positioning;
  - operator requirements;
  - participation process;
  - expected time commitment;
  - privacy and data boundaries;
  - compensation/incentive structure.
- Explore whether the CKB community can support a paid operator testing programme.
- Continue improving the application based on internal tester feedback.
- Use real operator feedback to determine whether the Receiver Registry addresses a meaningful problem before expanding the scope or seeking broader adoption.

## Key Outcome

The focus has shifted from primarily building and validating the technical system toward proving real-world operator demand and usability.

The main remaining challenge is no longer identifying whether the infrastructure can work technically, but getting genuine ADS-B receiver operators to participate and determining whether the Receiver Registry solves a problem important enough for them to adopt.