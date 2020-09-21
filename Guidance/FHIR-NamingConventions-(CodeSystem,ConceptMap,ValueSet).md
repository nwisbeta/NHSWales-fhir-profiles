# NHS Wales Naming Conventions for FHIR CodeSystem, ValueSet and ConceptMap Resources
## Naming segments
The naming conventions defined here are based on the following naming segments:

**[base URL]:** the base URL  is https://fhir.standards.cymru/

**[ResourceType]:** The FHIR resource type e.g. 'CodeSystem', 'ValueSet' or 'ConceptMap'.  

**[BusinessName]:** For CodeSystem and ValueSet, the business name shall reflect the name given to the data set as published in the relevant Data Standards Change Notice (DSCN). For ConceptMap resources, the business name shall reflect the name given to the value set that is being mapped from. 

*Note that in some cases the HL7 FHIR standard mandates value sets that do not match the equivalent Wales data standards e.g. [AdministrativeGender](https://hl7.org/fhir/R4/valueset-administrative-gender.html). In this case a concept map is required to map from the HL7 standard to the Welsh standard.*

## Naming conventions for CodeSystem, ValueSet and ConceptMap resources
The following naming convention applies to FHIR CodeSystem, ConceptMap and ValueSet resources:

The **URL** of the resource shall be in the form
**[base URL]/[ResourceType]/[BusinessName]** e.g. 
* https&#58;//fhir.standards.cymru/CodeSystem/Ethnicity
* https&#58;//fhir.standards.cymru/ValueSet/GenderIdentity
* https&#58;//fhir.standards.cymru/ConceptMap/AdministrativeGender


The **logical id** of the CodeSystem shall be in the form **DataStandardsCymru-[BusinessName]** e.g.
* DataStandardsCymru-Ethnicity,
* DataStandardsCymru-MaritalStatus

The **name** of the resource - specifically the name.value.element - shall be in the form **DataStandardsCymru[BusinessName]** e.g. 
* DataStandardsCymruEthnicity
* DataStandardsCymruMaritalStatus

The **title** of the resource shall follow the name.value.element, using title case e.g.
* Data Standards Cymru Ethnicity
* Data Standards Cymru Marital Status

The **filename** of the CodeSystem shall be in the form **[ResourceType]-DataStandardsCymru-[BusinessName]** e.g. 
* CodeSystem-DataStandardsCymru-Ethnicity
* ConceptMap-DataStandardsCymru-AdministrativeGender

An example CodeSystem resource used to define the NHS Wales data standard for communication of marital status is provided below:
```xml
<?xml version="1.0" encoding="UTF-8"?>
<CodeSystem xmlns="http://hl7.org/fhir">
	<id value="DataStandardsCymru-MaritalStatus"/>
	<extension url="http://hl7.org/fhir/StructureDefinition/codesystem-sourceReference">
		<valueUri value="http://www.nwisinformationstandards.wales.nhs.uk/sitesplus/documents/299/20171222-DSCN%202017%2011-Core%20Ref%20Data%20Standards-v1.0.pdf"/>
	</extension>
	<url value="https://fhir.standards.cymru/CodeSystem/MaritalStatus"/>	
	<version value="1.0.0"/>
	<name value="DataStandardsCymruMaritalStatus"/>
	<title value="Data Standards Cymru Marital Status"/>
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