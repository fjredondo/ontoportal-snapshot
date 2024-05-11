# ontoportal-snapshot
Bioinformatics - Semantic interoperability: OntoPortal snapshot 

OntoPortal technology is a generic resource to build ontology repositories or, more broadly, semantic artefact catalogues that can simultaneously co-host and fully support resources that span from SKOS thesauri to OBO, RDF-S, and OWL ontologies. [[1]](#1).

OntoPortal provides endpoints for accessing its content: a REST web service API that returns JSON-LD;

In this work, a batch process has been developed to download a snapshot of the ontologies contained in each OntoPortal repository.

# Usage
## Command
`./ontoportal_download.sh ./repo_list.csv DOWNLOAD_FOLDER`

Where

<ul>
  <li>**ontoportal_download.sh**: script that makes use of the REST web services API in each OntoPortal repository to download the latest version of each ontology. The ontology is renamed using the repository metadata and the HTTP response data from the server.</li>
  <li>**repo_list.csv**</li>
  <li>**DOWNLOAD_FOLDER**: Destination directory of the outputs of the process.</li>
  <ul>
    <li>folders with the ontologies (latest versions) downloaded.</li>
    <li>ontology_err.csv: list of ontologies not downloaded indicating the error produced.</li>
    <li>ontology_list.csv: list of downloaded ontologies.</li>
    <li>output.log: allows you to track the process.</li>
  </ul>
</ul>

# References
<a id="1">[1]</a> 
Jonquet, C. et al. (2023). Ontology Repositories and Semantic Artefact Catalogues with the OntoPortal Technology. In: Payne, T.R., et al. The Semantic Web – ISWC 2023. ISWC 2023. Lecture Notes in Computer Science, vol 14266. Springer, Cham. https://doi.org/10.1007/978-3-031-47243-5_3
