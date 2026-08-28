# Tools and Libraries

This section contains tools and libraries that can support citation verification, scholarly metadata retrieval, reference extraction, bibliography processing, and evaluation of evidence-grounded language-model systems.

## 1. Crossref REST API

- **Type:** Scholarly metadata API
- **Purpose:** Crossref provides bibliographic metadata for scholarly publications, including titles, authors, journals, publication information, DOI records, ORCID information, and other identifiers.
- **Use in this project:** Can be used to verify whether a DOI belongs to the claimed paper and to cross-check title, authors, journal, and publication metadata.
- **Official documentation:** https://www.crossref.org/documentation/retrieve-metadata/rest-api/
- **Why it is relevant:** DOI and bibliographic verification are central to detecting fabricated or incorrect references.

## 2. OpenAlex

- **Type:** Open scholarly metadata database and API
- **Purpose:** OpenAlex provides a large interconnected catalog of scholarly works, authors, sources, institutions, topics, and citation relationships.
- **Use in this project:** Can be used to search for papers, compare publication metadata, identify authors and venues, and examine citation relationships.
- **Official documentation:** https://developers.openalex.org/
- **Why it is relevant:** Provides an independent scholarly metadata source for cross-checking LLM-generated references.

## 3. Semantic Scholar Academic Graph API

- **Type:** Scholarly literature API
- **Purpose:** Semantic Scholar provides programmatic access to information about scientific papers, authors, citations, venues, abstracts, and related scholarly metadata.
- **Use in this project:** Can be used to search for candidate papers, verify author and paper metadata, and inspect citation relationships.
- **Official documentation:** https://www.semanticscholar.org/product/api
- **Why it is relevant:** A second independent scholarly source is useful when checking whether an LLM-generated citation corresponds to a real publication.

## 4. GROBID

- **Type:** Open-source machine-learning library for scholarly-document processing
- **Purpose:** GROBID extracts structured information from scholarly PDFs, including document metadata, bibliographic references, citation markers, and full-text structure.
- **Use in this project:** Can be used to extract reference lists from research papers and convert bibliographic information into structured formats such as TEI or BibTeX.
- **Official repository:** https://github.com/kermitt2/grobid
- **Why it is relevant:** It can automate extraction of the references that need to be checked for citation integrity.

## 5. Citation.js

- **Type:** JavaScript bibliography and citation-processing library
- **Purpose:** Citation.js converts and processes bibliographic formats including BibTeX, DOI, BibJSON, Wikidata, CSL-JSON, and RIS.
- **Use in this project:** Can be used to normalize, convert, and format bibliographic records after citation metadata has been collected.
- **Official website:** https://citation.js.org/
- **Official repository:** https://github.com/citation-js/citation-js
- **Why it is relevant:** Standardized citation parsing and formatting can reduce metadata and formatting errors during citation auditing.

## How These Tools Fit Together

A citation-verification workflow can use these tools at different stages:

1. **Crossref** — verify DOI and publisher metadata.
2. **OpenAlex** — independently cross-check scholarly metadata and citation relationships.
3. **Semantic Scholar** — perform another independent paper and author lookup.
4. **GROBID** — extract references and citation information from research PDFs.
5. **Citation.js** — normalize and convert the resulting bibliographic records.

Using multiple independent metadata sources is useful when evaluating citation fabrication because a reference should not be considered valid merely because one search system returns a superficially similar record.
