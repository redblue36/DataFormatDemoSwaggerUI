<p align="center">
  <img src="docs/bsc-logo.png">
</p>

<p align="center">
<b>Blockchain in Transport Alliance Standards Council (BiTAS)</b>
<br><br>
<i>BiTAS Std 120-2019: LOCATION COMPONENT SPECIFICATION</i>
</br></br>
</p>


> **Note:  this is just to demonstrate an option....dummy format.**

### Revision History

Version | Date | Author
---------|----------|---------
 BiTAS Std 120-2019 v1.0 | February 27, 2019 | Pratik Soni, BiTAS Tracking Data WG Chair

### Copyright

The *BiTAS Std 120-2019: Location Component Specification* is owned by the Blockchain in Transport Alliance Standards Council. Any attempt to copy this document and use it in whole or in part by any other organization without the express written consent of the Blockchain in Transport Alliance Standards Council will be viewed as copyright infringement.

### Conventions

Figures and charts included in this specification are drafted using Unified Modelling Language (UML) class diagrams and charts. For more information on how to read the charts and diagrams in this Specification, please refer to Section 5: Component Model.

### Contents

- [Forward](#forward)
- [Introduction](#introduction)
- [Component Definition](#location-component)
  - [Diagram](#diagram) 
  - [Data Format Specification](#spec)

#### Forward

As the BiTAS Data Formats Technical Committee has set defining the Location Component a priority for the BiTA Standards Council, the BiTAS Location Component Work Group charter has empowered the group to establish and define a Location Component. In the course of developing the Specification and evaluating objectives, the Location Components Work Group considered deliverables, definitions, coordination/collaboration, milestones and timelines, priorities, future versions, technology agnosticism and Work Group and Technical Committee feedback.

#### Introduction

The Location Component is a data structure used whenever a geographic location needs to be recorded on the Blockchain. The Location Component, without any other information, contains all the information needed to determine a geographic location.  The Location Component is used to define the location of any type of object or entity regardless of whether it is fixed (e.g. a building, port, rail station, etc) or mobile (e.g. a vehicle or shipping container, etc).

![figure2](location-figure2.png)

A Location Component is a data structure that is always embedded within another data structure (the Parent Component). In other words, a Location Component can never exist in isolation on the blockchain. This is because the other data structure(s) define the accompanying data depending on the purpose of the Location Component. Examples of purposes are:
1. To track the location of a shipping container
2. To record the destination address of a shipment
3. To record the billing address of a customer for a shipment
4. To dispatch a driver to a location

#### Location Component

</br>

##### Diagram

![BSC Logo](location.png)
</br>
</br>

##### Data Format Specification

</br>
</br>
