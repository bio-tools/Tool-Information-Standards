---
title: "About"
layout: about
---

An **information standard** for the desription of bioinformatics software tools, that lists software attributes that must be specified within a 5-tier scale of description completeness and quality.  It is based on [biotoolsSchema](https://github.com/bio-tools/biotoolsschema) and the [EDAM ontology](https://github.com/edamontology/edamontology). The standard is being adopted by [bio.tools](https://bio.tools) - the ELIXIR Tools and Data Services Registry.

- [Broadly applicable to diverse types of tool](#tooltypes) including application software, workflows and APIs. 
- Uses software attributes defined in [biotoolsSchema](https://github.com/bio-tools/biotoolsschema)
- Uses a controlled vocabulary for types of data, data formats, operations and common topics defined in the [EDAM ontology](https://github.com/edamontology/edamontology)
- It is an [open community-driven project](#community)

This site is based on a [Jekyll theme](https://jekyllrb.com/docs/themes/) which you can can find at: {% include icon-github.html username="mmistakes" %}/[jekyll-theme-basically-basic](https://github.com/mmistakes/jekyll-theme-basically-basic)

# Overview
The Tool Information Standard is one component of a stack of interrelated technologies and guidelines:

![technology-stack]({{site.url}}/assets/images/technology_stack.png){: .align-center}

- [biotoolsSchema](https://github.com/bio-tools/biotoolsschema) is a formalised XML schema (XSD) which defines a description model for bioinformatics software. It defines a **syntax** for over 50 important scientific, technical and administrative attributes that support cataloguing, discovery, use and interoperability of software. To enable concise information, standard identifiers are used where possible, including EDAM ontology concept IDs for scientific aspects. biotoolsSchema defines 15 controlled vocabularies for technical tool aspects such as programming language and license.
- [EDAM ontology](https://github.com/edamontology/edamontology) is a comprehensive ontology of well-established, familiar concepts that are prevalent within bioinformatics and computational biology. It defines the **semantics** - a controlled vocabulary - for describing software in terms of types of input and output *data* and data *identifiers*, supported data *formats*, *operations* and *topics*.
- [Tool Information Standard](http://github.com/bio-tools/tool-Information-Standard) lists software attributes that must be specified within a 5-tier scale of description completeness and quality. It provides a practical framework and metrics for description of individual tools, and the curation of collections such as [bio.tools](https://bio.tools).
- [Curation Guidelines](http://biotools.readthedocs.io/en/latest/curators_guide.html) describe conventions for *how* each attribute should be specified when registering a tool in bio.tools.  These human-readable and user-friendly guidelines provide information that goes beyond syntax and semantics provided by biotoolsSchema and EDAM.
- *Software Best Practice* can be abstracted from the Curation Guidelines, for example, general recommndations for software description / documentation in contexts other than bio.tools.

