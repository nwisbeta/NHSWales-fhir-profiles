# DRAFT NHS Wales Naming Conventions for FHIR CodeSystem Resources

The following naming convention applies to CodeSystem resources. Please click [here](FHIR-NamingConventions.md) for definitions of the naming segments refered to in this document.

The filename of the CodeSystem  shall be in the form:  
**[ResourceType]-[OrganisationName]-[BusinessName1]-[BusinessName2]**  
*e.g. 'CodeSystem-NHSWales-DataStandards-Ethnicity'*

The logical id of the CodeSystem shall be in the form:  
**[OrganisationName]-[BusinessName1]-[BusinessName2]**  
*e.g. 'NHSWales-DataStandards-Ethnicity', 'NHSWales-WCRS-DocumentType'*

The URL of the CodeSystem shall be in the form:  
**[base URL]/[ResourceType]/[OrganisationName]-[BusinessName1]-[BusinessName2]**  
*e.g. 'https://fhir.wales.nhs.uk/CodeSystem/NHSWales-DataStandards-MaritalStatus'*

The name of the CodeSystem - specifically the name.value.element - shall be in the form:  
**[OrganisationName][BusinessName1][BusinessName2]**   
*e.g. 'NHSWalesDataStandardsEthnicity', 'NHSWalesDataStandardsGenderIdentity'*

The title of the CodeSystem shall be in the form:  
**[Organisation Name] [Business Name 1] [Business Name 2]**   
*e.g. 'NHS Wales Data Standards Ethnicity'*

An example CodeSystem resource used to define the NHS Wales data standard for communication of marital status is provided below:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<CodeSystem xmlns="http://hl7.org/fhir">
	<id value="NHSWales-DataStandards-MaritalStatus"/>
	<extension url="http://hl7.org/fhir/StructureDefinition/codesystem-sourceReference">
		<valueUri value="http://www.nwisinformationstandards.wales.nhs.uk/sitesplus/documents/299/20171222-DSCN%202017%2011-Core%20Ref%20Data%20Standards-v1.0.pdf"/>
	</extension>
	<url value="https://fhir.wales.nhs.uk/CodeSystem/NHSWales-DataStandards-MaritalStatus"/>	
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