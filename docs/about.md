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
<div class="datatable-begin"></div>

Food    | Description                           | Category | Sample type
------- | ------------------------------------- | -------- | -----------
Apples  | A small, somewhat round ...           | Fruit    | Fuji
Bananas | A long and curved, often-yellow ...   | Fruit    | Snow
Kiwis   | A small, hairy-skinned sweet ...      | Fruit    | Golden
Oranges | A spherical, orange-colored sweet ... | Fruit    | Navel

<div class="datatable-end"></div>

# Application to bio.tools

The "SPARSE" tier defines the minimum information requirement for new bio.tools entries.  It is [under discussion](https://github.com/bio-tools/biotoolsRegistry/issues/338) to allow a user to filter entries according to tiers in the standard.  The standard also provides a basis to monitor bio.tools content and label entries in various ways:

* *entry completeness* ("SPARSE" through to "COMPREHENSIVE")
* whether an entry was manually inspected
* whether an entry is verified, *i.e.* conforms to the Curation Guidelines
* overall *entry quality* ("NEEDS TO IMPROVE" through to "EXCELLENT") - conflating the notions above

![infographic_quality_metrics]({{site.url}}/assets/images/infographic_quality_metrics.png){: .align-center}

If and how to use such labels is currently [under discussion](https://github.com/bio-tools/Tool-Information-Standard/issues/1).

