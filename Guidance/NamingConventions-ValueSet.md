# DRAFT NHS Wales Naming Conventions for FHIR ValueSet Resources

The following naming convention applies to ValueSet resources. Please click [here](NamingConventions.md) for definitions of the naming segments refered to in this document.

The filename of the ValueSet  shall be in the form:  
**[ResourceType]-[OrganisationName]-[BusinessName1]-[BusinessName1]**  
*e.g. 'ValueSet-NHSWales-DataStandards-Ethnicity'*

The logical id of the ValueSet shall be in the form:  
**[OrganisationName]-[BusinessName1]-[BusinessName1]**  
*e.g. 'NHSWales-DataStandards-Ethnicity', 'NHSWales-WCRS-DocumentType'*

The URL of the ValueSet shall be in the form:  
**[base URL]/[ResourceType]/[OrganisationName]-[BusinessName1]-[BusinessName1]**  
*e.g. 'https://fhir.wales.nhs.uk/ValueSet/NHSWales-DataStandards-MaritalStatus'*

The name of the ValueSet - specifically the name.value.element - shall be in the form:  
**[OrganisationName][BusinessName1][BusinessName1]**   
*e.g. 'NHSWalesDataStandardsEthnicity', 'NHSWalesDataStandardsGenderIdentity'*

The title of the ValueSet shall be in the form:  
**[Organisation Name] [Business Name 1] [Business Name 2]**   
*e.g. 'NHS Wales Data Standards Ethnicity'*

An example ValueSet resource used to define the NHS Wales data standard for communication of marital status is provided below:
```xml
<ValueSet xmlns="http://hl7.org/fhir">
	<id value="NHSWales-DataStandards-Ethnicity"/>
	<extension url="http://hl7.org/fhir/StructureDefinition/valueset-sourceReference">
		<valueUri value="http://www.nwisinformationstandards.wales.nhs.uk/sitesplus/documents/299/20171222-DSCN%202017%2011-Core%20Ref%20Data%20Standards-v1.0.pdf"/>
	</extension>
	<url value="https://fhir.wales.nhs.uk/ValueSet/NHSWales-DataStandards-Ethnicity"/>>
	<version value="1.0.1"/>
    <name value="NHSWalesDataStandardsEthnicity"/>
	<title value="NHS Wales Data Standards Ethnicity"/>
	<status value="draft"/>
	<date value="2020-09-02T00:00:00+01:00"/>
	<publisher value="NHS Wales Informatics Service"/>
	<contact>
		<name value="Data Standards"/>
		<telecom>
			<system value="email"/>
			<value value="data.standards@wales.nhs.uk"/>
			<use value="work"/>
		</telecom>
	</contact>
	<description value="The ethnicity of a person, as specified by the person, as per the Office of National Statistics (ONS) 2011 Census Categories"/>
	<copyright value="© 2030 NHS Wales Informatics Service."/>
	<compose>
		<include>
			<system value="https://fhir.wales.nhs.uk/CodeSystem/NHSWales-DataStandards-Ethnicity"/>
		</include>
	</compose>
</ValueSet>``` 