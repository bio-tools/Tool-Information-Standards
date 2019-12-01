---
title: "Tool Information Standards"
layout: about
---

The **Tool Information Standards** are a stack of community-defined, open and integrated technologies, technical standards and guidelines:

![technology_stack]({{site.url}}/assets/images/technology_stack.png){: .align-center}

- **biotoolsCore** is a flat list of over 50 important scientific, technical and administrative **software attributes** that support cataloguing, discovery, use and interoperability of software. It will soon be made available in JSON format. {[repo](https://github.com/bio-tools/Tool-Information-Standards/blob/master/docs/tool_attributes.md/), [learn more]({site.url}}/tool_attributes.html)}
- **EDAM** is an ontology of well-established, familiar concepts that are prevalent within bioinformatics and computational biology. It defines the **semantics** - a controlled vocabulary - to describe software functionality in terms of *operations*, types of input and output *data* and data *identifiers*, supported data *formats*, and common *topics*. {[repo](https://github.com/edamontology/edamontology), [readthedocs](https://edamontologydocs.readthedocs.io/en/latest/)}
- **biotoolsSchema** is a formalised XML schema (XSD) which defines a description model for bioinformatics software. It defines a **structure** and **syntax** for the 50 attributes listed in biotoolsCore. To enable concise information, standard identifiers are used where possible, including EDAM ontology for scientific aspects and internally-defined controlled vocabularies for technical aspects such as programming language and license. It defines the scope and content of the [bio.tools](https://bio.tools) registry of life science software. {[repo](https://github.com/bio-tools/biotoolsschema), [readthedocs](https://biotoolsschema.readthedocs.io/en/latest/)}
- **Tool information profiles** define lists of software attributes (from biotoolsCore) that can, should or must be specified for different types of tools within a set of tool descriptions. An individual profile - a JSON file conforming to toolInfoProfileSchema (JSON schema) - defines an **information requirements** that is tailored to an individual communities (national, scientific or technical).  Tool information profiles provide a practical **curation framework** and **metrics** for any corpus of tools. {[repo](http://github.com/bio-tools/tool-information-profile)}
- **Curation Guidelines** describe conventions for *how* each attribute should be specified when describing a tool for registation in catalogues such as *bio.tools*.  These human-readable **user-friendly guidelines** provide information that goes beyond syntax and semantics provided by biotoolsSchema and EDAM. Beyond the general purpose [Curators Guide](https://biotools.readthedocs.io/en/latest/curators_guide.html) a set of [tutorials](https://biotools.readthedocs.io/en/latest/community_specific_guidelines.html) are being tailored to the specific requirements of national, scientific and technical community profiles. {[repo](https://github.com/bio-tools/biotoolsdocs)}
- [Software Best Practice](https://elixir-europe.org/about-us/commissioned-services/software-best-practices) can be abstracted from the Curation Guidelines, for example, **general recommendations** for the provision and documentation of software in contexts other than *bio.tools*.


The standards support the broader *bio.tools* initative - fostered with support from [ELIXIR](https://elixir-europe.org/) - which aspires to provide comprehensive and consistent information for all European bioinformatics resources:

* *Community curation of bioinformatics software and data resources* (2019), Briefings in Bioinformatics, [doi:10.1093/bib/bbz075](https://doi.org/10.1093/bib/bbz075)
* *The bio.tools registry of software tools and data resources for the life sciences* (2019), Genome Biology, [doi:https://doi.org/10.1093/bioinformatics/btt113.](https://doi.org/10.1093/bioinformatics/btt113)
* *Tools and data services registry: a community effort to document bioinformatics resources* (2016), Nucleic Acids Research [doi:10.1093/nar/gkv1116](https://doi.org/10.1093/nar/gkv1116)

