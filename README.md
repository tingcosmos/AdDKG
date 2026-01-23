## AdDKG
This repository provides the process of the construction of the Alzheimer’s disease and Dementia Knowledge Graphs (AdDKG) along with all the datasets and query protocols used in the work. AdDKG is a literature-based biomedical knowledge graph designed for exploring the mechanism underlying astrocyte autophagy and pyroptosis in AD. This project is done by Gongli Hospital of Shanghai Pudong New Area and Shanghai Pudong New Area Mental Health Center, China. 

## Authors
Ting Liu (lt02174@glhospital.com), Zhisheng Huang (huang.zhisheng.nl@gmail.com) and Hongyun Qin (qinhongyun07@163.com)

## Datasets
The complete AdDKG integrates annotated triples from 172,283 articles, constituting a large-scale resource around 176 GB. Given the complexity of hosting and servicing such a graph-structured database on public platforms, the full knowledge base is maintained on our institutional servers via a secure access protocol. Here, to ensure the transparency and to facilitate the verification, we provide the following two access pathways:\
	- To enable the verification and reproduction of the key findings in our case study, we have publicly released all annotated data, entity mappings, and SNOMED CT alignments for the 12 analyzed articles. This complete validation package is available on at [mini-AdDKG release pag](https://github.com/tingcosmos/AdDKG/releases).\
	- For the complete AdDKG knowledge base, we provide the following two access pathways:\
		a) Query service: Interested parties can contact the corresponding author (H. Qin) with specific questions. Our team will design and execute the corresponding SPARQL queries against the full AdDKG knowledge base and return the results.\
		b) Collaborative access: For projects requiring broader or repeated access, researchers may contact the corresponding author (H. Qin) to establish a data-sharing agreement, which may include secure VPN connections to our institutional server.

### Knowledge Graph Construction in GraphDB

**1. Downloading and starting the GraphDB** \
Download GraphDB free edition from https://www.ontotext.com/products/graphdb/graphdb-free/. GraphDB is a Java application and requires Java 8. Make sure you have an up-to-date Java 8 installation. Please download Java from https://java.com/en/download/help/download_options.xml. Run the GraphDB script in the bin directory. To access the Workbench, open http://localhost:7200 in a browser. Please get more information on GraphDB for a [quick start guide](https://graphdb.ontotext.com/documentation/10.4/index.html).

**2. Creating Repositories in GraphDB** \
By default, the GraphDB will initialize a location but not create any repositories. \
Create a new repository from the menu `Setup` -> `Repositories` page in the GraphDB Workbench. \
To create a new repository in the location, click `Create new repository`. \
Fill in AdDKG at the `Repository ID*`, then click `creat`.

**3. Importing Databases in GraphDB** \
Import all databases from the menu `Import` -> `RDF page` -> `User data`. Click on `Upload RDF files` and select files to upload. \
Click on `Import`, and fill the Target graphs with a URL as Named graphs. \
If the database is too large to upload from the User data page, you can store the database in the local `graphdb-import` file and then import the database from the menu `Import` -> `RDF page` -> `Server files`. \
The databases are available at [mini-AdDKG release page](https://github.com/tingcosmos/AdDKG/releases).

**4. Accessing and Reasoning Data in GraphDB** \
The data in GraphDB can be accessed and reasoned by SPARQL query language. Start query from the menu `SPARQL`.

## More Information
Please contact T. Liu (tingliu0909@gmail.com) and/or H. Qin (qinhongyun07@163.com) if you have any questions about the construction process, the datasets and query protocols.
