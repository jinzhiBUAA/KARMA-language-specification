# Title

Requirements Interchange Format (ReqIF)

# Version

Version 1.2

# OMG Document Number

formal/2016-07-01

# Standard document URL

http://www.omg.org/spec/ReqIF/1.2

# Machine Consumable Files

Normative: http://www.omg.org/spec/ReqIF/20101201/reqif.cmof
 http://www.omg.org/spec/ReqIF/20110401/reqif.xsd
 http://www.omg.org/spec/ReqIF/20110402/driver.xsd

# Scope
IMPORTANT NOTE: The following clauses describe the scope of the ReqIF standard. The ReqIF model itself, and the machine-readable documents generated from it (reqif.xsd, driver.xsd, reqif.cmof) are unchanged since ReqIF v1.0.1. 
1.1 Who should read this document? 
This document is created to inform: 
* Persons interested in exchanging requirements data between organizations that do not have a possibility to share the same repository (See Clause 4 for a definition of “repository”).
* Requirements authoring tool vendors who want to support the Requirements Interchange Format (ReqIF) with export and import interfaces for their requirements authoring tools. See Clause 4 for a definition of “requirements authoring tool.” 
* Tool vendors other than requirements authoring tool vendors who wish to interchange requirements for documentation or other purposes.
* Anyone interested in defining, interchanging, storing, etc., requirements in a standard interchange format. 
1.2 Objectives of the Requirements Interchange Format 
Requirements management has been an integral part of the development process in various industries (especially in the military, aeronautical, or the medical device industry) for years. Other industries have been adopting requirements management recently. 
The automotive industry for example introduced requirements management around 1999. As requirements management spread in the automotive industry over the years, more and more car manufacturers and suppliers have been applying requirements management and making use of dedicated requirements authoring tools. Large improvements have been made in these organizations and requirements management has been established as a key discipline in this collaborative engineering environment. Now with this established discipline in place, manufacturers and suppliers strive for collaborative requirements management where requirements management does not stop at company borders. 
For technical and organizational reasons, two companies in the manufacturing industry are rarely able to work on the same requirements repository and sometimes do not work with the same requirements authoring tools. A generic, non proprietary format for requirements information is required to cross the chasm and to satisfy the urgent industry need for exchanging requirement information between different companies without losing the advantage of requirements management at the organizations' borders. 
With the help of a dedicated interchange format for requirements specifications, it is possible to bridge the gap: 
* The collaboration between partner companies is improved by the benefits of applying requirements management methods across company borders.
* The partner companies do not have to use the same requirements authoring tool and suppliers do not need to have multiple requirements authoring tools to fulfill the need of their customers with regards to compatibility. 
* Within a company, requirement information can be exchanged even if various tools are used to author requirements.
The Requirements Interchange Format (ReqIF) described in this specification defines such an open, non-proprietary exchange format. Requirement information is exchanged by transferring XML documents that comply to the ReqIF format. 
See the following figure for an example scenario between two partners who are exchanging a Customer Requirements Specification and the corresponding System Requirements Specification.

Figure 1.1 represents a common scenario how requirements specifications are exchanged between partners. Both partners in the scenario use different requirements management (RM) tools to create, manage, and evolve their requirements specifications. The process is usually initiated by Partner 1. Customer requirements that are relevant for Partner 2 are consolidated in a snapshot document. The Partner 2 specific CRS snapshot is exported out of the RM-Tool A by means of the ReqIF-Exporter and transferred asynchronously to Partner 2 via existing data transfer mechanisms. The result of the export is a ReqIF compliant XML document representing the specific CRS snapshot. The data transfer mechanism is out of scope of ReqIF. Having received the exported CRS snapshot Partners 2 imports the information into RM-Tool B in order to analyze the customer requirements imposed by Partner 1. For traceability reasons Partner 2 links the received customer requirements with the corresponding system requirements. As an answer to the customer requirements Partner 2 creates a consolidated SRS snapshot that contains the system requirements realizing the imposed customer requirements of Partner 1. The SRS snapshot is fed back to Partner 1 as an exported ReqIF compliant XML document. Having imported the SRS snapshot Partner 1 can analyze within RM-Tool A how the customer requirements are fulfilled by the system requirements specified by Partner 2. As specifications evolve over time the exchange via ReqIF is an event driven, asynchronous data exchange.
