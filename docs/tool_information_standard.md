---
title: "Tool Information Standard"
layout: about
---

The **Tool Information Standard** is one component of a stack of interrelated technologies and guidelines:

![technology_stack]({{site.url}}/assets/images/technology_stack.png){: .align-center}

- [biotoolsSchema](https://github.com/bio-tools/biotoolsschema) is a formalised XML schema (XSD) which defines a description model for bioinformatics software. It defines a **syntax** for over 50 important scientific, technical and administrative attributes that support cataloguing, discovery, use and interoperability of software. To enable concise information, standard identifiers are used where possible, including EDAM ontology for scientific aspects and internally-defined controlled vocabularies for technical aspects such as programming language and license.
- [EDAM ontology](https://github.com/edamontology/edamontology) is an ontology of well-established, familiar concepts that are prevalent within bioinformatics and computational biology. It defines the **semantics** - a controlled vocabulary - for describing software in terms of types of input and output *data* and data *identifiers*, supported data *formats*, *operations* and *topics*.
- [Tool Information Standard](http://github.com/bio-tools/tool-Information-Standard) lists software attributes (from biotoolsSchema) that must be specified within a 5-tier scale of description completeness and quality. It provides a practical **framework** and **metrics** for description of individual tools, and the curation of collections such as [bio.tools](https://bio.tools).
- [Curation Guidelines](http://biotools.readthedocs.io/en/latest/curators_guide.html) describe conventions for *how* each attribute should be specified when registering a tool in bio.tools.  These human-readable and user-friendly **guidelines** provide information that goes beyond syntax and semantics provided by biotoolsSchema and EDAM.
- [Software Best Practice](https://todo) can be abstracted from the Curation Guidelines, for example, **general recommendations** for the description / documentation of software in contexts other than bio.tools.


# Tiers in the standard
The Tool Information Standard is five lists of tool attributes (see Table below) that must be specified for a software description (*e.g.* a bio.tools entry) to be assigned in a 5 tier ratings of *description completeness*.  Some attributes are grouped (see tables on right) for purposes of determining adherence to the standard. For example "Documentation" is satisfied if at least one of "General" documentation", "API documentation" or "API specification" is specified.


![infographic_attributes]({{site.url}}/assets/images/infographic_attributes.png){: .align-center}

# Attributes

## General attributes


Attribute | Description | Format | biotoolsSchema | | toolInfoProfileSchema | Guideline
--------- | ----------- | ------ | -------------- | | --------------------- | ---------  
**Name** | Canonical software name assigned by the software developer or service provider | Text | [``<name>``](http://bio-tools.github.io/biotoolsSchema/#Link1D) | name | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#name-tool)
**Description** | Short and concise textual description of the software function | Text | [``<description>``](http://bio-tools.github.io/biotoolsSchema/#Link1E) | description | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#description)
**Homepage** | Homepage of the software, or some URL that best serves this purpose | URL | [``<homepage>``](http://bio-tools.github.io/biotoolsSchema/#Link1F) | homepage | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#homepage)
**bio.tools ID** | Unique ID (case insensitive) of the tool that is assigned upon registration of the software in bio.tools, normally identical to tool name. | Text (URL-safe version of tool name) | [``<biotoolsID>``](http://bio-tools.github.io/biotoolsSchema/#Link20) | biotoolsID | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#summary-biotoolsid)
**bio.tools CURIE** | bio.tools CURIE (compact URI) based on the bio.tools tool ID. | Text | [``<biotoolsCURIE>``](http://bio-tools.github.io/biotoolsSchema/#Link21) | biotoolsCURIE | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#summary-biotoolscurie)
**version** | Version information (typically a version number) of the software. | Text | [``<version>``](http://bio-tools.github.io/biotoolsSchema/#Link22) | version | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#version-tool)
**otherID** | A unique identifier of the software, typically assigned by an ID-assignment authority other than bio.tools. |  Text | [``<otherID>``](http://bio-tools.github.io/biotoolsSchema/#Link23) | otherID | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#other-ids)
**Tool type** | The type of application software: a discrete software entity can have more than one type. | [enum](http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#tool-type) (from biotoolsSchema) | [``<toolType>``](http://bio-tools.github.io/biotoolsSchema/#Link39) | toolType | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#tool-type)



## Scientific attributes
Attribute | Description | Format | biotoolsSchema | | toolInfoProfileSchema | Guideline
--------- | ----------- | ------ | -------------- | | --------------------- | ---------  
**Scientific topics** | General scientific domain the software serves or other general category, *e.g.* 'Proteomics' | Term and / or URI of [EDAM Topic](http://edamontology.org/topic_0004) concept(s) | [``<topic>``](http://bio-tools.github.io/biotoolsSchema/#Link3A) | topic | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#topic)
**Scientific operations** | The basic operation(s) performed by the software, *e.g.* 'Multiple sequence alignment' | Term and / or URI of [EDAM Operation](http://edamontology.org/operation_0004) concept(s) | [``<function><operation>``](http://bio-tools.github.io/biotoolsSchema/#Link27) | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#operation)
**Type of input data** | Type of primary input data (if any), *e.g.* 'Protein sequences' | Term and / or URI of [EDAM Data](http://edamontology.org/data_0006) concept(s) | [``<function><input><data>``](http://bio-tools.github.io/biotoolsSchema/#Link18) | inputData | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#data-type-input-and-output-data)
**Type of output data** | Type of primary output data (if any), *e.g.* 'Sequence alignment' | Term and / or URI of [EDAM Data](http://edamontology.org/data_0006) concept(s) | [``<function><input>/<output><data>``](http://bio-tools.github.io/biotoolsSchema/#Link18) | outputData | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#data-type-input-and-output-data)
**Supported input data formats** | Allowed format(s) of primary inputs, *e.g.* 'FASTA' | Term and / or URI of [EDAM Format](http://edamontology.org/format_1915) concept(s) | [``<function><input><format>``](http://bio-tools.github.io/biotoolsSchema/#Link18) | inputFormat | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#data-format-input-and-output-data)
**Supported output data formats** | Allowed format(s) of primary outputs, *e.g.* 'Clustal' | Term and / or URI of [EDAM Format](http://edamontology.org/format_1915) concept(s) | [``<function><input>/<output><format>``](http://bio-tools.github.io/biotoolsSchema/#Link18) | outputFormat | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#data-format-input-and-output-data)
**Function note** | Concise comment about a tool function, if not apparent from the software description and EDAM annotations. | Text| [``<function><note>``](http://bio-tools.github.io/biotoolsSchema/#Link2A) | functionNote | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#note-function)
**Function command** | Relevant command, command-line fragment or option for executing this function / running the tool in this mode. | Text| [``<function><note>``](http://bio-tools.github.io/biotoolsSchema/#Link2B) | functionCmd | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#command)



## Technical attributes
Attribute | Description | Format | biotoolsSchema | | toolInfoProfileSchema | Guideline
--------- | ----------- | ------ | -------------- | | --------------------- | ---------  
**Operating system** | The operating system supported by a downloadable software package. | [enum](http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#operating-system) (from biotoolsSchema) | [``<labels><OperatingSystem>``](http://bio-tools.github.io/biotoolsSchema/#Link3B) | operatingSystem | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#operating-system)
**Language** | Name of programming language the software source code was written in, *e.g.* 'C'. | [enum](http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#programming-language) (from biotoolsSchema) | [``<language>``](http://bio-tools.github.io/biotoolsSchema/#Link3C) | language | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#programming-language)
**License** | Software or data usage license | [enum](http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#license) (from biotoolsSchema) | [``<labels><license>``](http://bio-tools.github.io/biotoolsSchema/#Link3D) | license | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#license)
**Collection** | Tag for a collection that the software has been assigned to within bio.tools. | Text | [``<labels><collectionID>``](http://bio-tools.github.io/biotoolsSchema/#Link3E) | collectionID | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#collection)
**Maturity** | How mature the software product is. | [enum](http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#maturity) (from biotoolsSchema) | [``<labels><maturity>``](http://bio-tools.github.io/biotoolsSchema/#Link3F) | maturity | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#maturity)
**Cost** | Monetary cost of acquiring the software. | [enum](http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#cost) (from biotoolsSchema) | [``<labels><Cost>``](http://bio-tools.github.io/biotoolsSchema/#Link40) | cost | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#cost)
**Accessibility** | Whether an online service is freely available for use. | [enum](http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#accessibility) (from biotoolsSchema) | [``<labels><Accessibility>``](http://bio-tools.github.io/biotoolsSchema/#Link41) | accessibility | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#accessibility)


## Link attributes
Attribute | Description | Format | biotoolsSchema | | toolInfoProfileSchema | Guideline
--------- | ----------- | ------ | -------------- | | --------------------- | ---------  
**Discussion forum** | Online forum for user discussions about the software. | URL | [``<link><type>Discussion forum</type>``]() | discussionForum | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#link-group)
**Helpdesk** | Helpdesk providing support in using the software. | URL | [``<link><type>Helpdesk</type>``]() | helpdesk | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#link-group)
**Issue tracker** | Link to tracker for software issues, bug reports, feature requests etc. | URL | [``<link><type>Issue tracker</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1A) | issueTracker | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#link-group)
**Mailing list** | Link to mailing list for software announcements, discussions, support etc. | URL | [``<link><type>Mailing list</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1A) | mailingList | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#link-group)
**Mirror** | Mirror of an (identical) online service. | URL | [``<link><type>Mirror</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1A) | mirror | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#link-group)
**Software catalogue** | Some registry, catalogue etc. other than bio.tools where the tool is also described. | URL | [``<link><type>Software catalogue</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1A) | softwareCatalogue | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#link-group)
**Repository** | A place where source code, data and other files can be retrieved from, typically via platforms like GitHub which provide version control and other features, or something simpler, e.g. an FTP site. | URL | [``<link><type>Repository</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1A) | repository | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#link-group)
**Social media* | A website used by the software community including social networking sites, discussion and support fora, WIKIs etc. | URL | [``<link><type>Social media</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1A) | socialMedia | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#link-group)
**Service* | An online service (other than Galaxy) that provides access (an interface) to the software. | URL | [``<link><type>Service</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1A) | service | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#link-group)
**Galaxy service* | An online service providing the tool through the Galaxy platform. | URL | [``<link><type>Galaxy service</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1A) | galaxyService | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#link-group)
**Technical monitoring** | Information about the technical status of a tool. | URL | [``<link><type>Technical monitoring</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1A) | technicalMonitoring | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#link-group)
**Misc link* | Other type of link for software - the default if a more specific type is not available. | URL | [``<link><type>Other</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1A) | linkOther | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#link-group)


## Download attributes
Attribute | Description | Format | biotoolsSchema | | toolInfoProfileSchema | Guideline
--------- | ----------- | ------ | -------------- | | --------------------- | ---------  
**API specification** | File providing an API specification for the software, e.g. Swagger/OpenAPI, WSDL or RAML file. | URL | [``<download><type>API specification</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | apiSpecification | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#download-group)
**Biological data** | Biological data, or a web page on a database portal where such data may be downloaded. | URL | [``<download><type>Biological data</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | biologicalData | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#download-group)
**Binaries** | Binaries for the software. | URL | [``<download><type>Binaries</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | binaries | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#download-group)
**Command-line specification** | File providing a command line specification for the software. | URL | [``<download><type>Command-line specification</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | commandlineSpecification | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#download-group)
**Container file** | Container file including the software. | URL | [``<download><type>Container file</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | containerFile | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#download-group)
**Icon** | Icon of the software. | URL | [``<download><type>Icon</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | icon | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#download-group)
**Screenshot** | Screenshot of the software. | URL | [``<download><type>Screenshot</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | screenshot | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#download-group)
**Source code** | Software source code. | URL | [``<download><type>Source code</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | sourceCode | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)
**Software package** | A software package; a bundle of files and information about those files, typically including source code and / or binaries. | URL | [``<download><type>Software package</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | softwarePackage | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)
**Test data** | Data for testing the software is working correctly. | URL | [``<download><type>Test data</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | testData | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)
**Test script** | Script used for testing testing whether the software is working correctly. | URL | [``<download><type>Test data</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | testScript | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)
**Tool wrapper (CWL)** |  | URL | [``<download><type>Tool wrapper (CWL)</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | toolWrapperCWL | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#download-group)
**Tool wrapper (galaxy)** | Galaxy tool configuration file (wrapper) for the software. | URL | [``<download><type>Tool wrapper (galaxy)</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | toolWrapperGalaxy | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#download-group)
**Tool wrapper (taverna)** | Taverna configuration file for the software. | URL | [``<download><type>Tool wrapper (taverna)</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | toolWrapperTaverna | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#download-group)
**Tool wrapper (other)** | Workbench configuration file (other than taverna, galaxy or CWL wrapper) for the software. | URL | [``<download><type>Tool wrapper (other)</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | toolWrapperOther | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#download-group)
**VM image** | Virtual machine (VM) image for the software. | URL | [``<download><type>VM image</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | vmImage | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#download-group)
**Downloads page** | Web page summarising general downloads available for the software. | URL | [``<download><type>Downloads page</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | downloadsPage | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#download-group)
**Misc download** | Other type of download for software - the default if a more specific type is not available. | URL | [``<download><type>Other</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B) | downloadsOther | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#download-group)


## Documentation attributes
Attribute | Description | Format | biotoolsSchema | | toolInfoProfileSchema | Guideline
--------- | ----------- | ------ | -------------- | | --------------------- | ---------  
**API documentation** | Human-readable API documentation. | URL | [``<documentation><type>API documentation</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C) | apiDocumentation | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)
**Citation instructions** | Human-readable API documentation. | URL | [``<documentation><type>Citation instructions</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C) | citationInstructions | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)
**Command-line options** | Information about the command-line interface to a tool. | URL | [``<documentation><type>Command-line options</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C) | commandlineOptions | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)
**Contributions policy** | Information about policy for making contributions to the software project. | URL | [``<documentation><type>Contributions policy</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C) | contributionsPolicy | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)
**General documentation** | General documentation | URL | [``<documentation><type>General</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C) | generalDocumentation | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)
**FAQ** | Frequently Asked Questions (and answers) about the software. | URL | [``<documentation><type>FAQ</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C) | faq | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)
**Governance** | Information about the software governance model. | URL | [``<documentation><type>Governance</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C) | governance | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)
**Installation instructions** | Instructions how to install the software. | URL | [``<documentation><type>Installation instructions</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C) | installationInstructions | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)
**User manual** | Information on how to use the software, tailored to the end-user. | URL | [``<documentation><type>User manual</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C) | userManual | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)
**Release notes** | Notes about a software release or changes to the software; a change log. | URL | [``<documentation><type>Release notes</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C) | releaseNotes | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)
**Terms of use** | Rules that one must agree to abide by in order to use a service. | URL | [``<documentation><type>Terms of use</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C) | termsOfUse | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)
**Training material** | Online training material such as text on a Web page, a presentation, video, tutorial etc. | URL | [``<documentation><type>Training material</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C) | trainingMaterial | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)
**Misc. documentation** | Some other type of documentation not listed in biotoolsSchema. | URL | [``<documentation><type>Other</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C) | documentationOther | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#documentation-group)


## Publication attributes
Attribute | Description | Format | biotoolsSchema | | toolInfoProfileSchema | Guideline
--------- | ----------- | ------ | -------------- | | --------------------- | ---------  
**Primary publication** | The principal publication about the tool itself; the article to cite when acknowledging use of the tool.  | DOI, PMID or PMCID | [``<publication>``](http://bio-tools.github.io/biotoolsSchema/#Link16) | publicationPrimary | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#publication-group)
**Method publication** | A publication describing a scientific method or algorithm implemented by the tool. | DOI, PMID or PMCID | [``<publication>``](http://bio-tools.github.io/biotoolsSchema/#Link16) | publicationMethod | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#publication-group)
**Usage publication** | A publication describing the application of the tool to scientific research, a particular task or dataset. | DOI, PMID or PMCID | [``<publication>``](http://bio-tools.github.io/biotoolsSchema/#Link16) | publicationUsage | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#publication-group)
**Benchmarking study publication** | A publication which assessed the performance of the tool. | DOI, PMID or PMCID | [``<publication>``](http://bio-tools.github.io/biotoolsSchema/#Link16) | publicationBenchmarkingStudy | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#publication-group)
**Review publication** | A publication where the tool was reviewed. | DOI, PMID or PMCID | [``<publication>``](http://bio-tools.github.io/biotoolsSchema/#Link16) | publicationReview | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#publication-group)


## Relation attributes
Attribute | Description | Format | biotoolsSchema | | toolInfoProfileSchema | Guideline
--------- | ----------- | ------ | -------------- | | --------------------- | ---------  
**isNewVersionOf** | The software is a new version of an existing software, typically providing new or improved functionality. | URL | [``<relation><type>isNewVersionOf</type>``](http://bio-tools.github.io/biotoolsSchema/#) | relationIsNewVersionOf | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#relation-group)
**hasNewVersion** | (inverse of above) | URL | [``<relation><type>hasNewVersion</type>``](http://bio-tools.github.io/biotoolsSchema/#) | relationHasNewVersion | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#relation-group)
**uses** | The software provides an interface to or in some other way uses the functions of other software under the hood, e.g. invoking a command-line tool or calling a Web API, Web service or SPARQL endpoint to perform its function. | URL | [``<relation><type>uses</type>``](http://bio-tools.github.io/biotoolsSchema/#) | relationUses | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#relation-group)
**usedBy** | (inverse of above) | URL | [``<relation><type>usedBy</type>``](http://bio-tools.github.io/biotoolsSchema/#) | relationUsedBy | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#relation-group)
**includes** | A workbench, toolkit or workflow includes some other, independently available, software. | URL | [``<relation><type>includes</type>``](http://bio-tools.github.io/biotoolsSchema/#) | relationIncludes | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#relation-group)
**includedIn** | (inverse of above) | URL | [``<relation><type>includedIn</type>``](http://bio-tools.github.io/biotoolsSchema/#) | relationIncludedIn | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#relation-group)


## Credit / contact attributes
Attribute | Description | Format | biotoolsSchema | | toolInfoProfileSchema | Guideline
--------- | ----------- | ------ | -------------- | | --------------------- | ---------  
**Primary contact** | The primary point of contact for the software. | Name, email, URL and/or ORCID iD | [``<credit><typeRole>Primary contact</typeRole>``](http://bio-tools.github.io/biotoolsSchema/#Link15) | creditprimaryContact | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#credit-group)
**Person credit** | Credit of an individual. | Name, email, URL and/or ORCID iD | [``<credit><typeRole>Primary contact</typeRole>``](http://bio-tools.github.io/biotoolsSchema/#Link15) | creditPerson | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#credit-group)
**Project credit** | Credit of a community software project not formally associated with any single institute. | Name, email, URL and/or ORCID iD | [``<credit><typeRole>Primary contact</typeRole>``](http://bio-tools.github.io/biotoolsSchema/#Link15) | creditProject | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#credit-group)
**Division credit** | Credit of or a formal part of an institutional organisation, e.g. a department, research group, team, etc. | Name, email, URL and/or ORCID iD | [``<credit><typeRole>Primary contact</typeRole>``](http://bio-tools.github.io/biotoolsSchema/#Link15) | creditDivision | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#credit-group)
**Institute credit** | Credit of an organisation such as a university, hospital, research institute, service center, unit etc. | Name, email, URL and/or ORCID iD | [``<credit><typeRole>Primary contact</typeRole>``](http://bio-tools.github.io/biotoolsSchema/#Link15) | creditInstitute | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#credit-group)
**Consortium credit** | Credit of an association of two or more institutes or other legal entities which have joined forces for some common purpose. Includes Research Infrastructures (RIs) such as ELIXIR, parts of an RI such as an ELIXIR node etc. | Name, email, URL and/or ORCID iD | [``<credit><typeRole>Primary contact</typeRole>``](http://bio-tools.github.io/biotoolsSchema/#Link15) | creditConsortium | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#credit-group)
**Funding agency credit** | Credit of a legal entity providing funding for development of the software or provision of an online service. | Name, email, URL and/or ORCID iD | [``<credit><typeRole>Primary contact</typeRole>``](http://bio-tools.github.io/biotoolsSchema/#Link15) | creditFundingAgency | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#credit-group)
**Developer credit** | Author of the original software source code. | Name, email, URL and/or ORCID iD | [``<credit><typeRole>Primary contact</typeRole>``](http://bio-tools.github.io/biotoolsSchema/#Link15) | creditDeveloper | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#credit-group)
**Maintainer credit** | Maintainer of a mature software providing packaging, patching, distribution etc. | Name, email, URL and/or ORCID iD | [``<credit><typeRole>Primary contact</typeRole>``](http://bio-tools.github.io/biotoolsSchema/#Link15) | creditMaintainer | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#credit-group)
**Provider credit** | Institutional provider of an online service. | Name, email, URL and/or ORCID iD | [``<credit><typeRole>Primary contact</typeRole>``](http://bio-tools.github.io/biotoolsSchema/#Link15) | creditProvider | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#credit-group)
**Documentor credit** | Author of software documentation including making edits to a bio.tools entry. | Name, email, URL and/or ORCID iD | [``<credit><typeRole>Primary contact</typeRole>``](http://bio-tools.github.io/biotoolsSchema/#Link15) | creditDocumentor | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#credit-group)
**Contributor credit** | Some other role in software production or service delivery including design, deployment, system administration, evaluation, testing, documentation, training, user support etc. | Name, email, URL and/or ORCID iD | [``<credit><typeRole>Primary contact</typeRole>``](http://bio-tools.github.io/biotoolsSchema/#Link15) | creditContributor | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#credit-group)
**Support credit** | Provider of support in using the software. | Name, email, URL and/or ORCID iD | [``<credit><typeRole>Primary contact</typeRole>``](http://bio-tools.github.io/biotoolsSchema/#Link15) | creditSupport | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#credit-group)
**ELIXIR Node** | Name of the ELIXIR Node that is credited. | [enum](http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#elixir-node) (from biotoolsSchema) | [``<elixirNode>``](http://bio-tools.github.io/biotoolsSchema/#Link43) | elixirNode | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#elixir-node)
**ELIXIR Platform** | Name of the ELIXIR Platform that is credited. | [enum](http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#elixir-platform) (from biotoolsSchema) | [``<elixirPlatform>``](http://bio-tools.github.io/biotoolsSchema/#Link43) | elixirPlatform | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#elixir-platform)





