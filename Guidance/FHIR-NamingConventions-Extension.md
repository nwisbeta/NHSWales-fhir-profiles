# DRAFT NHS Wales Naming Conventions for FHIR Extension Resources

The following naming convention applies to Extension resources. Please click [here](FHIR-NamingConventions.md) for definitions of the naming segments refered to in this document.

The filename of the Extension  shall be in the form:  
**Extension-[OrganisationName]-[BusinessName1]-[BusinessName1]**  
*e.g. 'Extension-NHSWales-DataStandards-AlliedHealthProfessionalCode'*

The logical id of the Extension shall be in the form:  
**Extension-[OrganisationName]-[BusinessName1]-[BusinessName1]**  
*e.g. 'Extension-NHSWales-DataStandards-AlliedHealthProfessionalCode'*

The URL of the Extension shall be in the form:  
**[base URL]/[ResourceType]/[OrganisationName]-[BusinessName1]-[BusinessName2]**  
*e.g. 'https://fhir.wales.nhs.uk/StructureDefinition/Extension-NHSWales-DataStandards-AlliedHealthProfessionalCode'*

The name of the Extension - specifically the name.value.element - shall be in the form:  
**Extension[OrganisationName][BusinessName1][BusinessName2]**   
*e.g. 'ExtensionNHSWalesDataStandardsAlliedHealthProfessionalCode*

The title of the Extension shall be in the form:  
**Extension - [Organisation Name] [Business Name 1] [Business Name 2]**   
*e.g. 'Extension - NHS Wales Data Standards Allied Health Professional Code'*

An example showing metadata fields for an NHS Wales FHIR Extension is provided below:
```xml
<StructureDefinition xmlns="http://hl7.org/fhir">
	<id value="Extension-NHSWales-DataStandards-AlliedHealthProfessionalCode"/>
	<meta>
		<lastUpdated value="2020-09-02T00:00:01+00"/>
	</meta>
	<text>
		<status value="generated"/>
	</text>
	<url value="https://fhir.wales.nhs.uk/StructureDefinition/Extension-NHSWales-DataStandards-AlliedHealthProfessionalCode"/>
	<version value="1.0.0"/>
	<name value="ExtensionNHSWalesDataStandardsAlliedHealthProfessionalCode"/>
	<title value="Extension - NHS Wales Data Standards Allied Health Professional Code"/>
	<status value="draft"/>
	<date value="2020-09-02T00:00:01+00"/>
	<publisher value="NHS Wales Informatics Service"/>
	<contact>
		<name value="Data Standards"/>
		<telecom>
			<system value="email"/>
			<value value="data.standards@wales.nhs.uk"/>
			<use value="work"/>
		</telecom>
	</contact>
	<description value="To allow a code indicating the role of the allied health professional to be included in PractitionerRole and DocumentReference.context."/>
	<copyright value="&#169; 2020 NHS Wales Informatics Service."/>
	<fhirVersion value="4.0.1"/>
	<kind value="complex-type"/>
	<abstract value="false"/>
	<contextType value="resource"/>
	<context value="PractitionerRole"/>
	<context value="DocumentReference.context"/>
	<type value="Extension"/>
	<baseDefinition value="http://hl7.org/fhir/StructureDefinition/Extension"/>
	<derivation value="constraint"/>
	<!-- Definition of the Extension... -->
</StructureDefinition>
``` 