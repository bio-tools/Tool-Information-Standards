---
title: "About"
layout: about
---

An **information standard** for the desription of bioinformatics software tools, that lists software attributes that must be specified within a 5-tier scale of description completeness and quality.  It is based on [biotoolsSchema](https://github.com/bio-tools/biotoolsschema) and the [EDAM ontology](https://github.com/edamontology/edamontology). The standard is being adopted by [bio.tools](https://bio.tools) - the ELIXIR Tools and Data Services Registry.

- [Broadly applicable to diverse types of tool](#tooltypes) including application software, workflows and APIs. 
- Uses software attributes defined in [biotoolsSchema](https://github.com/bio-tools/biotoolsschema)
- Makes heavy use of controlled vocabularies including the [EDAM ontology](https://github.com/edamontology/edamontology) for types of data, data formats, operations and common topics.
- It is an [open community-driven project](#community)

This site is based on a [Jekyll theme](https://jekyllrb.com/docs/themes/) which you can can find at: {% include icon-github.html username="mmistakes" %}/[jekyll-theme-basically-basic](https://github.com/mmistakes/jekyll-theme-basically-basic)

# Overview
The **Tool Information Standard** is one component of a stack of interrelated technologies and guidelines:

![technology_stack]({{site.url}}/assets/images/technology_stack.png){: .align-center}

- [biotoolsSchema](https://github.com/bio-tools/biotoolsschema) is a formalised XML schema (XSD) which defines a description model for bioinformatics software. It defines a **syntax** for over 50 important scientific, technical and administrative attributes that support cataloguing, discovery, use and interoperability of software. To enable concise information, standard identifiers are used where possible, including EDAM ontology for scientific aspects and internally-defined controlled vocabularies for technical aspects such as programming language and license.
- [EDAM ontology](https://github.com/edamontology/edamontology) is an ontology of well-established, familiar concepts that are prevalent within bioinformatics and computational biology. It defines the **semantics** - a controlled vocabulary - for describing software in terms of types of input and output *data* and data *identifiers*, supported data *formats*, *operations* and *topics*.
- [Tool Information Standard](http://github.com/bio-tools/tool-Information-Standard) lists software attributes (from biotoolsSchema) that must be specified within a 5-tier scale of description completeness and quality. It provides a practical **framework** and **metrics** for description of individual tools, and the curation of collections such as [bio.tools](https://bio.tools).
- [Curation Guidelines](http://biotools.readthedocs.io/en/latest/curators_guide.html) describe conventions for *how* each attribute should be specified when registering a tool in bio.tools.  These human-readable and user-friendly **guidelines** provide information that goes beyond syntax and semantics provided by biotoolsSchema and EDAM.
- [Software Best Practice](https://todo) can be abstracted from the Curation Guidelines, for example, **general recommendations** for the description / documentation of software in contexts other than bio.tools.


# Tool Information Standard
The Tool Information Standard is five lists of tool attributes (see Table below) that must be specified for an entry to be assigned in a 5 tier ratings of *entry completeness*.  Some attributes are grouped (see tables on right) for purposes of determining adherance to the standard.

![infographic_attributes]({{site.url}}/assets/images/infographic_attributes.png){: .align-center}

# Attributes

## General attributes


Attribute | Description | Format | biotoolsSchema | Guideline
--------- | ----------- | ------ | -------------- | ---------   
**Name** | Canonical software name assigned by the software developer or service provider | Text | [``<name>``](http://bio-tools.github.io/biotoolsSchema/#Link1D) | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#id18)
**Description** | Short and concise textual description of the software function | Text | [``<description>``](http://bio-tools.github.io/biotoolsSchema/#Link1E) | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#description)
**Homepage** | Homepage of the software, or some URL that best serves this purpose | URL | [``<homepage>``](http://bio-tools.github.io/biotoolsSchema/#Link1F) | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#homepage)
**Unique ID** | Unique ID of the tool that is assigned upon registration of the software in bio.tools | Text (URL-safe version of tool name) | [``<toolID>``](http://bio-tools.github.io/biotoolsSchema/#Link20) | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#id121)
**Tool type** | The type of application software: a discrete software entity can have more than one type. | [enum](http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#tool-type) (from biotoolsSchema) | [``<toolType>``](http://bio-tools.github.io/biotoolsSchema/#Link39) | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#tool-type)
**Scientific topics** | General scientific domain the software serves or other general category, *e.g.* 'Proteomics' | Term and / or URI of [EDAM Topic](http://edamontology.org/topic_0004) concept(s) | [``<topic>``](http://bio-tools.github.io/biotoolsSchema/#Link3A) | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#topic)
**Publications** | Publications about the software | DOI, PMID or PMCID | [``<publication>``](http://bio-tools.github.io/biotoolsSchema/#Link16) | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#publications-group)
**Scientific operations** | The basic operation(s) performed by the software, *e.g.* 'Multiple sequence alignment' | Term and / or URI of [EDAM Operation](http://edamontology.org/operation_0004) concept(s) | [``<function><operation>``](http://bio-tools.github.io/biotoolsSchema/#Link27) | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#operation)
**Operating system** | The operating system supported by a downloadable software package. | [enum](http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#operating-system) (from biotoolsSchema) | [``<labels><OperatingSystem>``](http://bio-tools.github.io/biotoolsSchema/#Link3B) | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#operating-system)
**Language** | Name of programming language the software source code was written in, *e.g.* 'C'. | [enum](http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#programming-language) (from biotoolsSchema) | [``<language>``](http://bio-tools.github.io/biotoolsSchema/#Link3C) | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#programming-language)
**License** | Software or data usage license | [enum](http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#license) (from biotoolsSchema) | [``<labels><license>``](http://bio-tools.github.io/biotoolsSchema/#Link3D) | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#license)
**Type of input & output data** | Type of primary input / output data (if any), *e.g.* 'Protein sequences' | Term and / or URI of [EDAM Data](http://edamontology.org/data_0006) concept(s) | [``<function><input>/<output><data>``](http://bio-tools.github.io/biotoolsSchema/#Link18) | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#data-type-input-and-output-data)
**Supported data formats** | Allowed format(s) of primary inputs/outputs, *e.g.* 'FASTA' | Term and / or URI of [EDAM Format](http://edamontology.org/format_1915) concept(s) | [``<function><input>/<output><format>``](http://bio-tools.github.io/biotoolsSchema/#Link18) | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#data-format-input-and-output-data)
**Scientific benchmark** | Scientific benchmarking results. | URL | [``<link><type>Scientific benchmark</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1A) | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#links-group)
**Technical monitoring** | Technical monitoring results. | URL | [``<link><type>Technical monitoring</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1A) | [link](http://biotools.readthedocs.io/en/latest/curators_guide.html#links-group)



## "Documentation" group

Attribute | Description | Format | element
--------- | ----------- | ------ | -------   
**General documentation** | General documentation | URL | [``<documentation><type>General</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C)
**Manual** | Information on how to use the software. | URL | [``<documentation><type>Manual</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C)
**API documentation** | Human-readable API documentation. | URL | [``<documentation><type>API documentation</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C)
**API specification** | File providing an API specification for the software, e.g. Swagger/OpenAPI, WSDL or RAML file. | URL | [``<download><type>API specification</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B)

## "Code availability" group

Attribute | Description | Format | element
--------- | ----------- | ------ | -------   
**Repository** | Link to repository where source code, data and other files may be downloaded | URL | [``<link><type>Repository</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1C)
**Source code** | Software source code. | URL | [``<download><type>Source code</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B)
**Source package** | Source package (of various types) for the software. | URL | [``<download><type>Source package</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B)

## "Accessibility" group

Attribute | Description | Format | element
--------- | ----------- | ------ | -------   
**Terms of use** | Rules that one must agree to abide by in order to use a service. | URL | [``<link><type>Terms of use</type>``]()
**Accessibility** | Whether the software is freely available for use. | [enum](http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#accessibility) (from biotoolsSchema) | [``<labels><Accessibility>``](http://bio-tools.github.io/biotoolsSchema/#Link41)
**Cost** | Monetary cost of acquiring the software. | [enum](http://biotoolsschema.readthedocs.io/en/latest/controlled_vocabularies.html#cost) (from biotoolsSchema) | [``<labels><Cost>``](http://bio-tools.github.io/biotoolsSchema/#Link40)

## "Support" group

Attribute | Description | Format | element
--------- | ----------- | ------ | -------   
**Helpdesk** | Helpdesk providing support in using the software. | URL | [``<link><type>Helpdesk</type>``]()
**Issue tracker** | Link to tracker for software issues, bug reports, feature requests etc. | URL | [``<link><type>Issue tracker</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1A)
**Mailing list** | Link to mailing list for software announcements, discussions, support etc. | URL | [``<link><type>Mailing list</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1A)
**Contact person** | Primary contact, *e.g.* a person, helpdesk or mailing list | Name, email, URL and/or ORCID iD | [``<credit><typeRole>Primary contact</typeRole>``](http://bio-tools.github.io/biotoolsSchema/#Link15)
   
## "Downloads" group

Attribute | Description | Format | element
--------- | ----------- | ------ | -------   
**Biological data** | Biological data, or a web page on a database portal where such data may be downloaded. | URL | [``<download><type>Biological data</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B)
**Binaries** | Binaries for the software. | URL | [``<download><type>Binaries</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B)
**Binary package** | Binary package for the software. | URL | [``<download><type>Binary package</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B)
**Container file** | Container file including the software. | URL | [``<download><type>Container file</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B)
**CWL file** | Common Workflow Language (CWL) file for the software. | URL | [``<download><type>CWL file</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B)
**Ontology** | A file containing an ontology, controlled vocabulary, terminology etc. | URL | [``<download><type>Ontology</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B)
**VM image** | Virtual machine (VM) image for the software. | URL | [``<download><type>VM image</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B)
**Tool wrapper (galaxy)** | Galaxy tool configuration file (wrapper) for the software. | URL | [``<download><type>Tool wrapper (galaxy)</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B)
**Tool wrapper (taverna)** | Taverna configuration file for the software. | URL | [``<download><type>Tool wrapper (taverna)</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B)
**Tool wrapper (other)** | Workbench configuration file (other than taverna, galaxy or CWL wrapper) for the software. | URL | [``<download><type>Tool wrapper (other)</type>``](http://bio-tools.github.io/biotoolsSchema/#Link1B)


# Application to bio.tools

The "SPARSE" tier defines the minimum information requirement for new bio.tools entries.  It is [under discussion](https://github.com/bio-tools/biotoolsRegistry/issues/338) to allow a user to filter entries according to tiers in the standard.  The standard also provides a basis to monitor bio.tools content and label entries in various ways:

* *entry completeness* ("SPARSE" through to "COMPREHENSIVE")
* whether an entry was manually inspected
* whether an entry is verified, *i.e.* conforms to the Curation Guidelines
* overall *entry quality* ("NEEDS TO IMPROVE" through to "EXCELLENT") - conflating the notions above

![infographic_quality_metrics]({{site.url}}/assets/images/infographic_quality_metrics.png){: .align-center}

If and how to use such labels is currently [under discussion](https://github.com/bio-tools/Tool-Information-Standard/issues/1).

