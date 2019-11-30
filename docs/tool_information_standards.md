---
title: "Tool Information Standards"
layout: about
---

The **Tool Information Standards** are a stack of interrelated open, community-defined technologies and guidelines:

![technology_stack]({{site.url}}/assets/images/technology_stack.png){: .align-center}

- [biotoolsSchema](https://github.com/bio-tools/biotoolsschema) is a formalised XML schema (XSD) which defines a description model for bioinformatics software. It defines a **syntax** for over 50 important scientific, technical and administrative attributes that support cataloguing, discovery, use and interoperability of software. To enable concise information, standard identifiers are used where possible, including EDAM ontology for scientific aspects and internally-defined controlled vocabularies for technical aspects such as programming language and license. It defines the scope and content of [bio.tools](https://bio.tools) registry of life science software.
- [EDAM ontology](https://github.com/edamontology/edamontology) is an ontology of well-established, familiar concepts that are prevalent within bioinformatics and computational biology. It defines the **semantics** - a controlled vocabulary - for describing software functionality in terms of *operations*, types of input and output *data* and data *identifiers*, supported data *formats*, and common *topics*.
- [Tool Information Profiles](http://github.com/bio-tools/tool-information-profile) define lists of software attributes (from biotoolsSchema) that should be specified for different types of tools within a set of tool descriptions. It enables flexible definition of **information requirements** tailored to individual communities (national, scientific or technical). A profile thus provides a practical **curation framework** and **metrics** for description of a corpus of tools, such as *bio.tools*. An individual profile is JSON file conforming to toolInfoProfileSchema (JSON schema). 
- [Curation Guidelines](http://biotools.readthedocs.io/en/latest/curators_guide.html) describe conventions for *how* each attribute should be specified when describing a tool for registation in catalogues such as *bio.tools*.  These human-readable and user-friendly **guidelines** provide information that goes beyond syntax and semantics provided by biotoolsSchema and EDAM. Beyond the general purpose [Curators Guide](https://biotools.readthedocs.io/en/latest/curators_guide.html) a set of tutorials are being tailored to the specific requirements of national, scientific and technical community profiles. 
- [Software Best Practice](https://elixir-europe.org/about-us/commissioned-services/software-best-practices) can be abstracted from the Curation Guidelines, for example, **general recommendations** for the description / documentation of software in contexts other than bio.tools.


The standards are in support of the broader *bio.tools* initative, fostered with support from [ELIXIR](https://elixir-europe.org/), which aspires to provide comprehensive and consistent information for all European bioinformatics resources:

*Community curation of bioinformatics software and data resources* (2019), Briefings in Bioinformatics, [doi:10.1093/bib/bbz075](https://doi.org/10.1093/bib/bbz075)
*The bio.tools registry of software tools and data resources for the life sciences* (2019), Genome Biology, [doi:https://doi.org/10.1093/bioinformatics/btt113.](https://doi.org/10.1093/bioinformatics/btt113)
*Tools and data services registry: a community effort to document bioinformatics resources* (2016), Nucleic Acids Research [doi:10.1093/nar/gkv1116](https://doi.org/10.1093/nar/gkv1116)

