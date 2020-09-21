# DRAFT NHS Wales Naming Conventions for FHIR Profiles

The following naming convention applies to FHIR Profiles. Please click [here](FHIR-NamingConventions.md) for definitions of the naming segments refered to in this document.

The filename of the Profile shall be in the form:  
**[OrganisationName]-[BusinessName1]-[ResourceTypeOfProfile]**  
*e.g. 'NHSWales-WCRS-DocumentReference'*

The logical id of the Profile shall be in the form:  
**[OrganisationName]-[BusinessName1]-[ResourceTypeOfProfile]**  
*e.g. 'NHSWales-WCRS-DocumentReference'*

The URL of the Profile shall be in the form:  
**[base URL]/[FHIRversion]/[ResourceType]/[OrganisationName]-[BusinessName1]-[ResourceTypeOfProfile]**  
*e.g. 'https://fhir.wales.nhs.uk/R4/StructureDefinition/NHSWales-WCRS-DocumentReference'*

The name of the Profile - specifically the name.value.element - shall be in the form:  
**[OrganisationName][BusinessName1][ResourceTypeOfProfile]**   
*e.g. 'NHSWalesWCRSDocumentReference*

The title of the Profile shall be in the form:  
**[Organisation Name] [Business Name 1] [ResourceTypeOfProfile]**   
*e.g. 'NHS Wales WCRS DocumentReference'*

An example showing metadata fields for an NHS Wales FHIR Profile is provided below:
```xml
<StructureDefinition xmlns="http://hl7.org/fhir">
    <id value="NHSWales-WCRS-DocumentReference" />
    <url value="https://fhir.nhs.uk/R4/StructureDefinition/NHSWales-WCRS-DocumentReference" />
    <version value="1.0.0" />
    <name value="NHSWalesWCRSDocumentReference" />
    <title value="NHS Wales WCRS DocumentReference" />
    <status value="draft" />
    <date value="2020-09-02" />
	<publisher value="NHS Wales Informatics Service"/>
	<contact>
		<name value="Data Standards"/>
		<telecom>
			<system value="email"/>
			<value value="data.standards@wales.nhs.uk"/>
			<use value="work"/>
		</telecom>
	</contact>
    <description value="Defines the Welsh Care Records Service constraints and extensions on the DocumentReference resource." />
    <copyright value="&#169; 2020 NHS Wales Informatics Service."/>
    <fhirVersion value="4.0.1" />
    <!-- Definition goes here... -->
</StructureDefinition>
```
