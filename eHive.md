# eHive manual update

## Brief explanation

eHive is a system to define and execute workflows. It operates by spawning autonomous workers which carry out parallel tasks in order to complete the larger pipeline. It was originally created for running in-house Ensembl workflows, but is now shipped separately and can be used to run any computational workflows. It is widely used in Ensembl and by other projects: we are aware of several hundreds active workflows, totalling thousands of CPU years on several compute clusters. eHive is written in Perl, with Python and Java plugins. It supports various job schedulers and has beta support for Docker clouds.

The [existing eHive manual](http://ensembl-hive.readthedocs.io/en/master/) is hosted on Readthedocs, however there are improvements we wish to make to the documentation, including the addition of a cheat sheet. The overall goal is to make eHive more accessible: make the first steps easier for new users, whilst allowing users to reach intermediate and advanced levels quicker.

## Expected results

* Better documentation of advanced features.
* Cheat sheet.
* Other miscellaneous improvements to the existing documentation.

## Commitment

Part-time

## Mentors

Matthieu Muffato and Brandon Walts

# What do you need to do ?

You will find in this section information about what we see as the best candidate and proposal.

## Selection process

* Always contact us at helpdesk@ensembl.org to introduce yourself and discuss your ideas. The discussion is an integral part of your assessment and it is very unlikely we will accept a proposal from someone that has not contacted us. Our experience from [GSoC](https://github.com/EnsemblGSOC/EnsemblProjects) is that half of the people just send an introduction email (e.g. "Hi, I want to work with you. What do I need to do to be selected ?") and we never hear from them again. You fill find that information on the [Season of Docs](https://developers.google.com/season-of-docs/) website and this page here. Honestly, don't bother sending that email if you are not going to engage in a proper discussion.
* helpdesk@ensembl.org is using Request Tracker (RT) to manage the emails. After sending us an email, you will get a confirmation that that it has been received and you will be assigned a ticket number, e.g. `Ensembl #340668`. Keep that string (the one you got, not the one I gave here as an example) in the subject of all the further emails. Please always send your email to helpdesk@ensembl.org only. Internally, RT will route your email to the relevant people. You do not need to cc anyone else.
* The email discussion will by default be private between you, the Outreach team (who manages helpdesk@ensembl.org) and the mentors, unlike other organizations where all communications go through a public mailing-list. If you have a killer idea, it will remain yours. We will *not* share it with other candidates.
* Share your proposal early over email and ask for a review. It would be a shame to misunderstand important parts of the project.
* You will be asked to demonstrate excellent communication skills, through our discussion and examples of documentation you (will) have written.

## Cheat-sheet

This is a major goal of this project. The cheat-sheet should be a one- or two-sided document with the most important commands of eHive.
Importantly, we expect you to propose a technical solution to host and build the cheat-sheet. Here are our requirements:
* We want to be able to update the content easily and quickly.
* We would like the source document to be text only.
* The cheat-sheet will have to be built automatically with the rest of the documentation on ReadTheDocs. It doesn't have to be built with Sphynx itself, e.g. we run Doxygen and other things on ReadTheDocs. We already have [a few modules that add functionality to ReadTheDocs' build system](https://github.com/Ensembl/ensembl-hive/tree/version/2.5/docs/xhive).
* It needs to be accessible through the existing manual, if not embedded in it.

Please, come and discuss your idea, even if it doesn't address all those points. We can work together on improving those, and we may also be able to relax some of the constraints if the proposed solution has other benefits.

## A better user manual

The manual needs to cater for users with vastly different levels of experience with eHive: from new starters who will discover the concepts of workflow to seasoned programmers who want to go beyond the traditional use-cases.

First of all, it would be great if you are able to install eHive and run some of the example workflows, e.g. the [Long-Multiplication pipeline](https://ensembl-hive.readthedocs.io/en/master/walkthrough/long_mult_walkthrough.html), to get the concepts of eHive.
Then, have a look at the manual in general, and critique:
1. The level of details. Which sections are for which users ? Which sections are missing for each user profile ?
2. The structure of the manual. Are you able to find the information you need ? Is it where you expect it to be ? Are the sections appropriately linked to one another ?
3. The quality of the language, the verbal style used
4. The typography and the layout; the relative length of the various sections

The project is not only about writing some documentation, it is about making the manual used at its full potential.
