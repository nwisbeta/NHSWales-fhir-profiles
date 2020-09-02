# DRAFT NHS Wales Naming Conventions for Nationally Defined FHIR Assets 

As a general principle NHS Wales will align with standards defined by the HL7 FHIR UK Core. The vision of the UK Core is to create a unified approach to interoperability across the four nations by creating a UK FHIR Core, which will enable information to flow across countries to improve health and care outcomes for all citizens.  

The [UK Core](https://simplifier.net/guide/ukcoredevelopment/home "HL7 FHIR® UK Core Implementation Guide R4 - July 2020") provides a set of FHIR profiles and implementation guides that define the use of HL7 FHIR in the UK. 

It will be neccessary, however, for NHS Wales to define its own standards for the use of FHIR in cases where NHS Wales information standards differ from those in use in the rest of the UK. In these cases NHS Wales will publish its own Conformance and Terminology FHIR resources to be referenced by HL7 FHIR UK Core profiles.

The following naming convention is provided to ensure that nationally defined FHIR assets are named in a consistent manner, and shall be applied to the following FHIR resources:

* StructureDefinition (Profile and Extension)
* [CodeSystem](NamingConventions-CodeSystem.md)
* [ValueSet](NamingConventions-ValueSet.md)
* [ConceptMap](NamingConventions-ConceptMap.md)

The naming convention includes the naming segments listed below, which are defined as follows:
* **BaseURL** for nationally defined assets is https://fhir.wales.nhs.uk
* **ResourceType**: The name or type of the FHIR resource e.g. 'CodeSystem', 'ValueSet', 'ConceptMap'
* **OrganisationName**: The owning organisation of the FHIR asset e.g. 'NHSWales', or 'SocialCareWales'.
* **BusinessName1**: The first business name of the CodeSystem. The code system MUST have at least one BusinessName segment, e.g. 'DataStandards', 'WCRS', WCCIS'. Where a CodeSystem may be used across several business domains, business names should reflect that.
* **BusinessName2** The second business name of the ValueSet. The ValueSet MAY have a second BusinessName segment. Where there is a second BusinessName, each one MUST be separated by a hyphen (-) character e.g. 'DataStandards-Ethnicity', 'WCRS-DocumentType'.

## Naming Conventions for CodeSystem, ValueSet and Profiles
