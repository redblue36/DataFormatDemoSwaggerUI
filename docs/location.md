<p align="center">
<img src="https://redblue36.github.io/DataFormatDemoSwaggerUI/docs/bsc_logo.png">
<br>
<br>
<br>
<br>
<br>
</p>

> **Remove this set of instructions before publishing this deliverable.** The title below should carry the “COMPONENT” or “DOCUMENT” qualifier for the specification per the charter.

<p align="center">
<i>BSC Std 120-2019: LOCATION COMPONENT SPECIFICATION</i>
<br>
<br>
<br>
</p>

> **GENERAL INSTRUCTIONS FOR THIS TEMPLATE**
> 
> **Remove this set of instructions before publishing this deliverable.**
>
> **Usage guidelines**
>
> 1. Read the text at the beginning of each section for guidance for additional information for completing this document.  Remove these diretions before publication.
> 1. Ensure to keep the same format for headers and content.  If there is a need to add a new section, please insert new ones sparingly and refresh the content table, as needed.  Rather than add new top level headings, it's preferable to add a subsection within one of the standard headings to maintain a standard flow.
> 1. Keep a line break after headers. 
> 1. *Italicized text* is standard boilerplate text for all released specifications and should remain in the document.
>
> **General style**
>
> 1. Position and language of the document should read like a requirements specification document.
> 1. Internal accounting of the working group is not appropriate to include in this document (e.g. cut-paste of the charter, coordination across WGs, timelines, milestones, reviews conducted, and other items not germane to a specification).  These items should be maintained by the WG separately.
> 1. Summarizing charter language to help frame certain sections of the specification such as the Objectives, Introduction, and Scope Sections is appropriate.  Reframe the wording keeping in mind the target audience is the ITC.
> 1. The primary audience for this document is the BSC Implementation TC (ITC).  If there is additional information helpful to convey to the DFTC Directors and/or the ITC, please attach separately in memorandum form.
> 1. Please don't refer to implementation specifics in this requirements specfication.  These details will be outlined by the ITC in a subsequent activity.
>     * Any reference to the term blockchain is a general loose reference.  
>     * References to APIs is an implementation detail that is not germane to this specification.
>     * Noting JSON as being the stored on the blockchain is another example of an implementation detail that is NOT germane to this specification. 
> 1. Representing data requirements in 3rd normal form isn't necessary.  Past specifications have done so alluding somewhat to implementation (e.g. use of surrogate keys for linkage for instance) leading to confusion.
>
> **Template Version History**
>
> Version | Date | Author
> ---------|----------|---------
> BSC Std TBD | May 9, 2020 | BSC DFTC Directors
>
> This template version section is not part of the officially released specification.  The version history for the Working Group’s deliverable is in a later section of this document.

### Work-in-progress / open items

> **Remove this entire section, including the section header, before publishing this deliverable.**
> Resolve all open issues prior to publishing this document.  Coordinate with other Working Groups as needed.  Raise questions with DFTC Directors as it is possible items could be directed to the "out of scope" section of this document.

1. The nesting is only 2 levels deep in the original published Location Component specification and this OAS spec.  Need to reconcile/clarify the verbiage here vs. the specs.
1. There is a special qualifier called "multiple".  It is unclear how this is used in relation to the nesting that is noted.  For example -- multiple at level 2 does not allow for sub-postions at level 3 in this structure -- but maybe it should not.
1. Warehouse zone, bin, shelf in in the text above  (that was in the original document) and it is in the OAS spec -- but there are no requirments definition in the published spec.  Need to reconcile all this to ensure the data elements are properly defined, reviewed, and published.  Suggests there might be an unpublished revision of location out there somewhere with this detail.
1. It seems like we need to clarify (1) a bin or shelf or row or sector cannot stand lone.  It's container such as the address of the warehouse would always apply.  And (2) a location can have multiple references.  It can have a street address and/or a geocode and/or others.
1. Provide specific detail on the Meta/ID field and how it is to be populated and what the intention here is for Location.  Is this an implementation specific detail to defer to the ITC??

### Foreword

*BSC Data Format Technical Committee develops and publishes requirements specifications for solving specific transportation related business problems using blockchain technology.*

*These specifications are primarily used by the BSC Implementation Technical Committee (ITC) to produce implementation-level technical guidance for how data shall be written to and retrieved from blockchain.  It is this ITC end-deliverable that is the primary consumable artifact by BSC membership and industry at large.*

*There are two types of data format specifications.*
* **Component specifications** *outline a grouping of individual data objects and other components that make up a logical grouping of information.  Examples include location or party.  Components do not standalone but are reusable building blocks used in forming a Document.*  
* **Document specifications** *may include a grouping of components used to describe the data elements supporting a specific business process.  An example might be a status tracking event.*

### Copyright or Similar Language TBD

> TODO:  Review copyright section with BSC counsel.

*BSC Std XXX-20XX: X Component Specification is an open sourced specification owned by the Blockchain in Transport Alliance Standards Council (BSC). Any licensing or usage verbiage should be inserted here.*

### Contents

- [Versions](#versions)
- [Acknowledgements](#ackowledgements)
- [Objective](#objective)
- [Introduction](#introduction)
- [Scope](#scope)
- [Glossary](#glossary)
- [References](#references)
- [Requirements](#requirements)
  - [Intentions](#intentions)
  - [Diagram](#diagram)
  - [Examples](#examples)
  - [Specification](#specification) 

### Versions

> **Remove this text before publishing this deliverable.**
> Update the name of the person and the authorized WG under which this update was performed. For naming convention use “BSC Std XXX-year vX: BSC Standard for…”]

Version | Date | Author
---------|----------|---------
BSC Std 120-2019 v1.0 | February 27, 2019 | Pratik Soni, BiTAS Tracking Data WG Chair
Work in progress | May 9, 2020 | BSC DFTC Directors reformat existing spec to new style guide

### Ackowledgements

  &nbsp; |   &nbsp; | &nbsp;
---------|----------|---------
**BiTA Standard Council Board** |
Participant1 | Participant2 | Participant3
**Data Format Data Technical Committee** |
Participant4 | Participant5 | Participant6
**Working Group** |
Participant7 | Participant8 | Participant9
Participant10 | Participant11 | Participant12

### Objective

> **Remove this text before publishing this deliverable.**
> Replace with a clear statement of the objective of the specification and what the specification is trying to achieve. Intention of the Specification.
>
> Clearly identify in **bold** text this specification outlines a **Component** or a **Document**.

Define a **Location Component specification** to provide a common structure to represent where an activity happens or where someone or something is located.  This construct is fundamental to transportation and logistics operations.  It is also fundamental to supporting business operations such as account management, pricing, and billing.  The structure can represent multiple, necessary forms of geographic identification.

### Introduction

> **Remove this text before publishing this deliverable.**
> Replace with a short background descriptor on the need for the objective and how this specification can be used in different applications. Include core tenants and other guiding principles and other things you were trying to accomplish that ultimately led to this specification being the optimal solution.]

The Location Component is a data structure used whenever a geographic location needs to be represented within a *** Document*** such one that supports shipment tracking, invoicing, etc.  The Location Component, as a self-contained structure, contains all the information needed to determine a geographic location.

The Location Component is used to define the location of any type of object or entity regardless of whether it is fixed (e.g. a building, port, rail station, etc) or mobile (e.g. a vehicle or shipping container, etc.).

![figure2](location-figure2.png)

A Location Component is a data structure that is always embedded a Document.  In other words, a Location Component can never exist in isolation on the blockchain. This is because the other data structure(s) define the accompanying data depending on the purpose of the Location Component. 

Examples:
-	Track the location of a shipping container
-	Record the destination address of a shipment
-	Record the billing address of a customer for a shipment
-	Dispatch a driver to a location

### Scope

> **Remove this text before publishing this deliverable.**
> Replace with a clear delineation of the boundary lines drawn for what is included in the specification and what is excluded.

-	Identify where an item is or has been within a journey 
-	Identify where an item is planned to be within an itinerary
-	Transportation and logistics use cases involving tracking and tracing.  As such airline, railway, roadway, ocean, and fixed warehousing and related custodial operations  such as pickup, delivery, drayage, customs, etc. are in scope.
-	Identify standard data elements & attributes known across multiple industries to form a starting data structure with the ability to add custom and/or unique Position attributes that provide greater position accuracy.

### Glossary

> **Remove this text before publishing this deliverable.**
> Replace with a table to introduce glossary terms/abbreviations specific to this specification. At a future date we will provide a link to the Glossary of BSC Terms.

*New terms and abbreviations introduced by this specification are listed in this section.  These items will be added to the BSC Glossary [linked here](url).*  **TODO need url.**

Term or Abbreviation | Definition
---------|----------
AAR | Association of American Railroads
FRA | Federal Railroad Administration
SPLC | Standard Point Location Code
FSAC | Freight Station Accounting Code

### References

> **Remove this text before publishing this deliverable.**
> In this section, list the references to the Standards document and/or other resources used or referenced in the Specification in this section. 
> * Reference Name:  Provide the URL to the specific page within the exact Standards or other document referenced. Do not simply add a link to wikipedia.org, ieee.org or gs1.org -- a link this generalized is not helpful.
> * Reference Organization:  Name of the organization with hyperlink if applicable

Reference Name | Reference Organization
---------|----------
ISO 3166: [Codes for the representation of names of countries and their subdivisions Part 1: Country codes](https://www.iso.org/iso-3166-country-codes.html) | ISO
[Standard Point Location Code](https://www.railinc.com/rportal/standard-point-location-code)| RAILINC

### Requirements

#### Intentions

> **Remove this text before publishing this deliverable.**
> It is very imoprtant to capture the intention and rationale for "why" the requirements are formulated the way they are in the "requirements" section.  Include this detail in this section.

A location may have a nested relationship with aliases or alternate references for the same location.  When the position array contains more than 1 structure, each structure is meant to represent the same location but using a different method such as latitude/longitude, postal address etc.

The intention of supporting multiple methods is to: a) Make the Location Component suitable for multiple use cases b) Support the expansion of the Location Component specification in a backwards-compatible way in the future

By doing so, the desire is to improve the adoption rates of this Specification. For example, the rail industry has an industry-specific method of specifying locations called the SPLC. Third parties may not have the ability to interpret this data so railway operators publishing locations in SPLC formats have the ability to publish a second more widely-known method such as latitude/longitude.

Position structure can contain nested structures including optional nested structures to handle scenarios where a method for specifying a location may have instances where a detailed location is needed and others where a detailed location description is not needed (or possible). For example, a location at a Warehouse would have as the root location structure (the root implements Position) specifying the postal address of the warehouse. Within that structure could be nested a warehouse zone identifying an area that the warehouse is sub-divided into. And within the Warehouse Zone structure could be nested a bin or shelf that might identify the specific location needed for a warehouse picker to locate an item

#### Diagram

*This diagram was auto-generated from the formal specification to provide a high-level view of data relationships and data attributes.*

![Location diagram](location.png)

#### Examples

> **Remove this text before publishing this deliverable.**  This section is optional.  Only provide examples if it helps with clarity.

*Examples in this form are provided to simply illustrate the general structure of the Specification that follows.*

1. Location as a simple address; no relevant position information is required 

```json
{
  "ID": "1234",
  "name": "SERVPROV-5_413-426",
  "qualifier": "Address",
  "address1": "2 ALPINE DR",
  "address2": "",
  "city": "CLOSTER",
  "stateProvince": "NJ",
  "zipPostal": "07624",
  "country": "USA"
}
```

2. Location plus position based on precedence

```json
{
  "ID": "1234",
  "name": "SERVPROV-5_413-426",
  "qualifier": "Mulitple",
  "positions": [
    {
      "position": 1,
      "qualifier": "Address",
      "Address1": "10 Alpine Dr",
      "Address2": "",
      "City": "Closter",
      "stateProvince": "NJ",
      "zipPostal": "07627",
      "country": "USA"
    },
    {
      "position": 2,
      "qualifier": "GeoCoord",
      "lattitude": 40.03657,
      "longitude": -75.38013,
      "accuracyMeters": 10,
      "altitudeMeters": 5
    },
    {
      "position": 3,
      "qualifier": "SPLC",
      "SPLC": "NYK",
      "stationName": "Newark"
    },
    {
      "position": 4,
      "qualifier": "City",
      "City": "Closter",
      "stateProvince": "NJ",
      "country": "USA"
    }
  ]
}
```

#### Specification

*Requirements are captured using Open API Specification (OAS) as a means to streamline capturing:*
-	*Standard data element names following standard naming conventions*
-	*Data relationships (e.g. associative, hierarchical)*
-	*Multiplicity/cardinality*
-	*Valid values including enumerations*
-	*Required vs. optional*

*This is a logical requirements specification and does not consider a specific technology or implementation.  The primary consumer of this section is the BSC Implementation Technical Committee (ITC).*

*It is anticipated the ITC can and will choose a different data organization that is optimal for storage and retrieval given implementation specifics and interoperability considerations.  The use of OAS and associated JSON-based examples by DFTC in this specification is solely a means to capture requirements for human consumption.  It does not specify or imply a physical API or JSON-oriented storage structure.*
<br>