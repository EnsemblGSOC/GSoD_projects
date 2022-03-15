# Accessing Ensembl data with Presto and AWS Athena

## Project outline
The project aim is to develop a prototype system which allows for the custom exploration and querying of Ensembl data held in denormalised tabular representations. Ensembl and other genome annotation providers have built similar systems (see prior art) which you should be aware of to be successful.

Due to the nature of the project there are no existing issues to build upon or process. Instead the initial period before plan submission is about building a knowledge of the technologies and domain Ensembl operates within. Understanding both of these is essential to a successful project.

We have chosen the following technologies to build upon:

 - Presto: a SQL engine which can query multiple storage engines/layers
 - AWS Athena: a data warehouse tool built on Presto which scans S3 flat-files when running queries
 - Parquet: a column based storage format which is very good at holding onto tabular data representations
 - Python: a language which integrates with the above technologies well

## Reading
### The Ensembl project
The Ensembl project was setup is 1999 and has been providing access to genomes and their annotation since its first release. Ensembl covers all domains of life from humans (our most popular species), through to plants, insects, bacteria, fungi amongst others. This means there is a huge interest in the human genome and its annotation but also a very long tail of other genomes to support  with far less access than any other genome (across all of our sites we host over 50,000 genomes).

To learn more about the Ensembl project I would recommend the following reading items

- The Ensembl websites 
	- The Ensembl blog: https://www.ensembl.info
	- Our vertebrates site https://www.ensembl.org
	- Ensembl plants https://plants.ensembl.org
	- Our fast release site https://rapid.ensembl.org
	- Our COVID-19 portal https://covid-19.ensembl.org
- Our last papers
	- Ensembl 2022: https://academic.oup.com/nar/article/50/D1/D988/6430486
	- Ensembl Genomes 2022: https://academic.oup.com/nar/article/50/D1/D996/6427344

This should give you a good grounding in what the project is currently doing.

### BioMart

This is the tool which provides the most similar functionality within Ensembl. We have more information below but I encourage trying to use BioMart. Our training event with [Noblekinmat](https://training.ensembl.org/events/2022/2022-02-24-Noblekinmat) has a training unit on BioMart (see the bottom of the screen). Try doing this exercise to see how BioMart works.

## Prior art

### BioMart

**[www.ensembl.org/biomart](http://www.ensembl.org/biomart)**

The original Ensembl “data miner” tool to convert data models into a [reverse star schema](https://en.wikipedia.org/wiki/Reverse_star_schema) where the majority of data is moved into dimension tables allowing for lean central concept tables. Only one data set (e.g. GRCh38 genes) can be queried at once, but the same query can be run on multiple compatible data sets. BioMart is built using SQL transformation statements (insert/select in the same statement) to transform a normalised schema into the reverse star schema. Tables can have indexes added to them to aid query performance, but not all are optimal (e.g. position queries are incorrectly formed). Attributes and filters are configured using an XML schema, which is configured via a specialised Java application called MartConfigurator. BioMart is extensively used by non-programmers and R developers since the natural representation of queries is a 2D matrix similar to a spreadsheet or data table. BioMart is built to take advantage of and work within MySQL’s limitations. It also scales to the number of attributes available per dataset and therefore scales poorly with elements such as orthology.

This [article gives an idea about BioMart](https://bmcgenomics.biomedcentral.com/articles/10.1186/1471-2164-10-22) from the original authors of the tool.

### Intermine

**[http://intermine.org/](http://intermine.org/)**

A data mining toolkit developed at the University of Cambridge and built around a core data model which uses the sequence ontology. Multiple data sources (in standard bioinformatics formats) can be combined together into a single infrastructure to enable powerful cross platform queries. Much of which is inserted into a PostgreSQL database. Intermine allows you to build complex queries which intersect multiple data sets. Queries use the object dot notation system to access/refer to attributes e.g. to access a gene’s stable id, and appropriate call would be “Gene.stableId” assuming the content was held under an accessor of the same name. You can use template queries, which have custom input for a few terms. This allows a user to quickly execute a query without needing to understand how the query builder works, and reducing the barrier to entry. Intermine has been deployed to multiple species, with tools available to execute and aggregate across multiple instances.

### NCBI Dataset

**[https://www.ncbi.nlm.nih.gov/datasets/tables/genes/](https://www.ncbi.nlm.nih.gov/datasets/tables/genes/)**

A tabular search engine developed by NCBI to search through their gene records. Part of the datasets work. Columns can be brought in/removed to customise output. The views are pre-generated and search is possible by gene id (without species), gene symbol (with species) and accession number e.g. NM. Response is fast and there is an API associated with it.

A number of ideas involved in this project share ideas with the way NCBI dataset behaves.

### Ensembl Genes

**https://github.com/related-sciences/ensembl-genes/tree/output/homo_sapiens_core_104_38**

A third party collection of files which were developed due to the sometimes hard to parse/collate nature of the denormalised Ensembl storage layer. These are available in a variety of formats and gives a good idea about how another group went about generating tabular representations of Ensembl data by directly querying our databases.

## Next steps

- Read the materials above to prepare for the project
- Put together a project plan
	- Any additional questions can result in more materials being made available here for transparency reasons
