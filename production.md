# Ensembl production manual
## Brief explanation

The Ensembl teams have developed many automated pipelines to process and analyse genomics data; including our gene annotation, gene tree, regulatory build and variation annotation pipelines. These are used to produce the Ensembl databases that power the Ensembl site and form the backend for our APIs. Many people who work with species not included in Ensembl or with confidential data, would like to run our pipelines on their own data and produce their own Ensembl-like	databases.

All of the code needed to run an Ensembl pipeline is Open Source, either from a public provider or written by us and distributed on GitHub. However, getting started with this involves setting up a complex production environment and getting familiar with the behaviour and requirements for the required pipeline. Several pipelines require domain-specific knowledge. There is detailed internal documentation to run these pieces of software. However, they are not all consistent (similar format, style) and may seem cryptic to someone attempting to use our pipelines outside of Ensembl. In order for our software to be used successfully both within and outside the Ensembl team, we are looking to refactor these existing pieces of documentation. 

## Expected results

* A manual detailing how to set up the production environment and run an Ensembl pipeline.
* A framework to host and document pipeline-specific information.
* A manual for each pipeline, written with the help and knowledge from the relevant teams

## Commitment

Full-time

## Mentors

Helen Schuilenburg and Nishadi De Silva
