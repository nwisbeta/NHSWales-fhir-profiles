# DRAFT NHS Wales Naming Conventions for Nationally Defined FHIR Assets 

As a general principle NHS Wales will align with standards defined by the HL7 FHIR UK Core. The vision of the UK Core is to create a unified approach to interoperability across the four nations by creating a UK FHIR Core, which will enable information to flow across countries to improve health and care outcomes for all citizens.  

The [UK Core](https://simplifier.net/guide/ukcoredevelopment/home "HL7 FHIR® UK Core Implementation Guide R4 - July 2020") provides a set of FHIR profiles and implementation guides that define the use of HL7 FHIR in the UK. 

It will be neccessary, however, for NHS Wales to define its own standards for the use of FHIR in cases where NHS Wales information standards differ from those in use in the rest of the UK. In these cases NHS Wales will publish its own Conformance and Terminology FHIR resources to be referenced by HL7 FHIR UK Core profiles.

The following naming convention is provided to ensure that nationally defined FHIR assets are named in a consistent manner, and shall be applied to the following FHIR resources:

* StructureDefinition
* CodeSystem
* ValueSet
* ConceptMap

The naming convention includes the naming segments listed below, which are defined as follows:
* **BaseURL** for nationally defined assets is https://fhir.wales.nhs.uk
* **FHIRVersion** The FHIR version of the resource e.g. 'R4'
* **Resource**: The name of the FHIR resource e.g. 'CodeSystem', 'ValueSet', 'ConceptMap'. Mandatory
* **OrganisationName**: The owning organisation of the FHIR asset e.g. 'NHSWales', or 'SocialCareWales'.
* **BusinessName1**: The first business name of the CodeSystem. The code system MUST have at least one BusinessName segment, e.g. 'DataStandards', 'WCRS', WCCIS'. Where a CodeSystem may be used across several business domains, business names should reflect that.
* **BusinessName2** The second business name of the ValueSet. The ValueSet MAY have a second BusinessName segment. Where there is a second BusinessName, each one MUST be separated by a hyphen (-) character e.g. 'DataStandards-Ethnicity', 'WCRS-DocumentType'.

The filename of the FHIR resource shall be in the form:  
**[Resource]-[OrganisationName]-[BusinessName1]-[BusinessName1]**  
*e.g. 'CodeSystem-NHSWales-DataStandards-Ethnicity', 'ValueSet-NHSWales-WCRS-DocumentType'*

The logical id of the resource shall be in the form:  
**[OrganisationName]-[BusinessName1]-[BusinessName1]**  
*e.g. 'NHSWales-DataStandards-Ethnicity', 'NHSWales-WCRS-DocumentType'*

The URL of the resource shall be in the form:  
**[base URL]/FHIRVersion/[Resource]-[OrganisationName]-[BusinessName1]-[BusinessName1]**  
*e.g. 'https://fhir.wales.nhs.uk/R4/CodeSystem/NHSWales-DataStandards-MaritalStatus'*

The name of the resource - specifically the name.value.element of the resource shall be in the form:  
**[OrganisationName] [BusinessName1] [BusinessName1]**   
*e.g. 'NHSWalesDataStandardsEthnicity', 'NHSWalesDataStandardsGenderIdentity'*

The title of the resource shall be in the form:  
**[Organisation Name] [Business Name 1] [Business Name1 ]**   
*e.g. 'NHS Wales Data Standards Ethnicity'*

An example CodeSystem resource used to define the NHS Wales data standard for marital status is provided below:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<CodeSystem xmlns="http://hl7.org/fhir">
	<id value="NHSWales-DataStandards-MaritalStatus"/>
	<extension url="http://hl7.org/fhir/StructureDefinition/codesystem-sourceReference">
		<valueUri value="http://www.nwisinformationstandards.wales.nhs.uk/sitesplus/documents/299/20171222-DSCN%202017%2011-Core%20Ref%20Data%20Standards-v1.0.pdf"/>
	</extension>
	<url value="https://fhir.wales.nhs.uk/R4/CodeSystem/NHSWales-DataStandards-MaritalStatus"/>	
	<version value="1.0.0"/>
	<name value="NHSWalesDataStandardsMaritalStatus"/>
	<title value="NHS Wales Data Standards Marital Status"/>
	<status value="draft"/>
	<experimental value="true"/>
	<date value="2020-08-25T12:02:00+01:00"/>
	<publisher value="NHS Wales Informatics Service"/>
	<contact>
		<name value="Data Standards"/>	
		<telecom>
			<system value="email"/>
			<value value="data.standards@wales.nhs.uk"/>
			<use value="work"/>
		</telecom>
	</contact>	
	<description value="An indicator to identify the legal marital status of a person"/>
	<copyright value="&#169; 2020 NHS Wales Informatics Service."/>
	<caseSensitive value="true"/>
	<content value="complete"/>
	<concept>
		<code value="11"/>
		<display value="Single"/>
	</concept>
	<concept>
		<code value="12"/>
		<display value="Cohabiting"/>
	</concept>	
	<concept>
		<code value="21"/>
		<display value="Married"/>
	</concept>
	<concept>
		<code value="22"/>
		<display value="Civil Partner"/>
	</concept>
	<concept>
		<code value="31"/>
		<display value="Divorced"/>
	</concept>
	<concept>
		<code value="32"/>
		<display value="Person whose Civil Partnership has been dissolved"/>
	</concept>
	<concept>
		<code value="41"/>
		<display value="Widowed"/>
	</concept>
	<concept>
		<code value="42"/>
		<display value="Surviving Civil Partner"/>
	</concept>
	<concept>
		<code value="51"/>
		<display value="Separated"/>
	</concept>
	<concept>
		<code value="91"/>
		<display value="Not disclosed or unknown"/>
	</concept>	
</CodeSystem>
``` 