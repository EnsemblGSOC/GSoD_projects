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


## Sample task

Anyone interested in the project should complete this short task and send a report on it.

[This page of documentation](https://www.ensembl.org/info/docs/api/api_git.html) describes the installation of the Ensembl Perl API that is the first step in setting up a working environment before running any of our pipelines.

1. Do you see any weaknesses or strengths in this document in its current form?

2. How would you re-structure or re-write this set of instructions so that someone unfamiliar with this task could successfully run these steps?

3. This step is the first in running many of the subsequent pipelines needed to produce  Ensembl (each one with its own set of instructions). In some cases, all the pipelines need to be run and in others only a handful are relevant.
   1. What would your suggestions be on how to lay out all these different manuals into a whole so that users could either follow the entire process step-by-step or pick and choose different steps and paths to go through depending on their requirements?

   1. What tools and platform would you choose to place the pipeline documentation in?
