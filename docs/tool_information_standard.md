---
title: "Tool Information Standards"
layout: about
---

The **Tool Information Standards** are a stack of interrelated open, community-defined technologies and guidelines:

![technology_stack]({{site.url}}/assets/images/technology_stack.png){: .align-center}

- [biotoolsSchema](https://github.com/bio-tools/biotoolsschema) is a formalised XML schema (XSD) which defines a description model for bioinformatics software. It defines a **syntax** for over 50 important scientific, technical and administrative attributes that support cataloguing, discovery, use and interoperability of software. To enable concise information, standard identifiers are used where possible, including EDAM ontology for scientific aspects and internally-defined controlled vocabularies for technical aspects such as programming language and license.
- [EDAM ontology](https://github.com/edamontology/edamontology) is an ontology of well-established, familiar concepts that are prevalent within bioinformatics and computational biology. It defines the **semantics** - a controlled vocabulary - for describing software in terms of types of input and output *data* and data *identifiers*, supported data *formats*, *operations* and *topics*.
- [Tool Information Profiles](http://github.com/bio-tools/tool-information-profile) define lists of software attributes (from biotoolsSchema) that should be specified for different ypes of tools within a set of tool descriptions. A profile is JSON file conforming to toolInfoProfileSchema (JSON schema). It provides a practical **framework** and **metrics** for description of individual tools, and the curation of collections such as [bio.tools](https://bio.tools).
- [Curation Guidelines](http://biotools.readthedocs.io/en/latest/curators_guide.html) describe conventions for *how* each attribute should be specified when registering a tool in bio.tools.  These human-readable and user-friendly **guidelines** provide information that goes beyond syntax and semantics provided by biotoolsSchema and EDAM.
- [Software Best Practice](https://elixir-europe.org/about-us/commissioned-services/software-best-practices) can be abstracted from the Curation Guidelines, for example, **general recommendations** for the description / documentation of software in contexts other than bio.tools.


The standards are developed by and for the European Life Science community fostered with support from [ELIXIR](https://elixir-europe.org/).