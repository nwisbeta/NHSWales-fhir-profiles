# DRAFT NHS Wales Naming Conventions for FHIR ConceptMap Resources

The following naming convention applies to ConceptMap resources. Please click [here](FHIR-NamingConventions.md) for definitions of the naming segments refered to in this document.

The filename of the ValueSet  shall be in the form:  
**[ResourceType]-[OrganisationName]-[BusinessName1]-[BusinessName2]**  
*e.g. 'ConceptMap-NHSWales-DataStandards-AdministrativeGender'*

The logical id of the ConceptMap shall be in the form:  
**[OrganisationName]-[BusinessName1]-[BusinessName2]**  
*e.g. 'NHSWales-DataStandards-AdministrativeGender'*

The URL of the ConceptMap shall be in the form:  
**[base URL]/[ResourceType]/[ResourceType]-[OrganisationName]-[BusinessName1]-[BusinessName2]**  
*e.g. 'https://fhir.nhs.uk/ConceptMap/ConceptMap-NHSWales-DataStandards-AdministrativeGender'*

The name of the ConceptMap - specifically the name.value.element - shall be in the form:  
**[ResourceType][OrganisationName][BusinessName1][BusinessName2]**   
*e.g. 'ConceptMapNHSWalesDataStandardsAdministrativeGender'*

The title of the ConceptMap shall be in the form:  
**[Resource Type] - [Organisation Name] [Business Name 1] [Business Name 2]**   
*e.g. 'Concept Map - NHS Wales Data Standards Administrative Gender'*

An example ConceptMap resource used to map HL7 gender codes to NHS Wales data standards gender identity is provided below:
```xml
<ConceptMap xmlns="http://hl7.org/fhir">
    <id value="NHSWales-DataStandards-AdministrativeGender" />
    <url value="https://fhir.nhs.uk/ConceptMap/ConceptMap-NHSWales-DataStandards-AdministrativeGender" />
    <version value="1.0.0" />
    <name value="ConceptMapNHSWalesDataStandardsAdministrativeGender" />
    <title value="Concept Map - NHS Wales Data Standards Administrative Gender" />
    <status value="draft" />
    <date value="2020-08-26T00:00:00+01:00" />
    <publisher value="NHS Wales Informatics Service"/>
	<contact>
		<name value="Data Standards"/>	
		<telecom>
			<system value="email"/>
			<value value="data.standards@wales.nhs.uk"/>
			<use value="work"/>
		</telecom>
	</contact>
    <description value="A Concept Map from ValueSet Administrative Gender to NHS Wales Data Standards Gender Identity code to aid interpretation." />
    <copyright value="&#169; 2020 NHS Wales Informatics Service."/>
    <sourceUri value="http://hl7.org/fhir/ValueSet/administrative-gender" />
    <targetUri value="https://fhir.wales.nhs.uk/ValueSet/NHSWales-DataStandards-GenderIdentity" />
    <group>
        <source value="http://hl7.org/fhir/administrative-gender" />
        <target value="https://fhir.wales.nhs.uk/CodeSystem/NHSWales-DataStandards-GenderIdentity" />
        <element>
            <code value="male" />
            <display value="Male" />
            <target>
                <code value="M" />
                <display value="Male" />
                <equivalence value="equivalent" />
            </target>
        </element>
        <element>
            <code value="female" />
            <display value="Female" />
            <target>
                <code value="F" />
                <display value="Female" />
                <equivalence value="equivalent" />
            </target>
        </element>
        <element>
            <code value="other" />
            <display value="Other" />
            <target>
                <code value="N" />
                <display value="Non-binary" />
                <equivalence value="inexact" />
				<comment value="Implementers should be careful when using these mappings operationally" />
            </target>
        </element>
        <element>
            <code value="unknown" />
            <display value="Unknown" />
            <target>
                <code value="Z" />
                <display value="Not disclosed or unknown, e.g. for unborn baby" />
                <equivalence value="equivalent" />
            </target>
        </element>
    </group>
</ConceptMap>
``` 
