---
title: 'ReScience C gets a makeover'
authors:
  - name: Olivia Guest
    orcid: 0000-0002-1891-0972
    affiliation: 1
  - name: Benoît Girard
    orcid: 0000-0002-8117-7064
    affiliation: 2
  - name: Konrad Hinsen
    orcid: 0000-0003-0330-9428
    affiliation: "3, 4"
  - name: Nicolas P. Rougier
    orcid: 0000-0002-6972-589X
    affiliation: 5
affiliations:
  - index: 1
    name: Donders Centre for Cognitive Neuroimaging, Radboud University, Nijmegen, Netherlands
  - index: 2
    name: Institut des Systèmes Intelligents et de Robotiques, Sorbonne Université & CNRS, Paris, France
  - index: 3
    name: Centre de Biophysique Moléculaire, CNRS, Orléans, France
  - index: 4
    name: Synchrotron SOLEIL, Saint Aubin, France
  - index: 5
    name: Inria Bordeaux Sud-Ouest, Talence, France
---

ReScience C received and accepted [its first submission](https://github.com/ReScience/ReScience-submission/pull/3) in 2015. Over the eight following years, we have done a lot of fine-tuning, but the overall mode of operation of the journal is still the same: articles are submitted and reviewed on GitHub, and published on [our Web site](https://rescience.github.io/), with the actual article PDFs [deposited and archived on Zenodo](https://zenodo.org/search?q=keywords:%22rescience%20c%22). The technical coordination between GitHub and Zenodo is handled by [a few Python scripts](https://github.com/ReScience/articles) but most of all by our editors, who need to execute 15 steps, ideally without making any mistake, for the publication of an accepted article.

While this lightweight infrastructure was a great way to get started, it is no longer satisfactory. Authors and readers keep asking for proper article DOIs, as provided by [Crossref](https://crossref.org/), rather than the [DataCite](http://www.datacite.org/) DOIs attributed by Zenodo, which are intended for datasets rather than articles. Editors are not complaining, but they don't express enthusiasm about our arcane publishing process either. And we, the editors-in-chief, have been wishing for better tools for overseeing the reviewing and publishing processes than labels on GitHub issues.

Today we proudly present the new face of ReScience C. We have joined [Open Journals](http://www.theoj.org/), the organization behind the [Journal of Open Source Software](https://joss.theoj.org/) and the [Journal of Open Source Education](https://jose.theoj.org/), and adapted their submission, reviewing, and publication infrastructure to our needs. This implies several changes to our operation, which we will outline in the following.

# Preparing and submitting articles

A ReScience C submission consists of an article and of the code that produces the results discussed in the article. All parts of the submission should reside in a Git repository, with the article in a separate directory. Articles are written as Markdown files with a YAML header for metadata, with references provided as a file in BibTeX format and figures as PDF files. We are confident that replacing our previous LaTeX template by Markdown will make authors' life easier, and we hope that the limitations of Markdown compared to LaTeX will not be perceived as overly constraining. For the technical details of preparing articles, see [our author guidelines](https://resciencec.theoj.org/).

**Question:** *is Markdown submission compulsory, as for JOSS? Or can authors submit PDF files produced by other means if they prefer ?*

**Note:** *the author guidelines do not exist yet, the link must be updated when they are ready.*

As before, submission requires at least one author to have a GitHub account, because the reviewing process still happens on GitHub issues. However, the entry point to the submission process is now [the ReScience C Web site](https://resciencec.theoj.org/), where you log in with your [ORCID](https://orcid.org/) -- no need to create yet another account! In the submission form, you will be ask to provide the title of your submission, and the URL of the Git repository. Next, you choose one of the four article types, and pick a subject category that will help us orient your submission to an appropriate handling editor.

The four article types are the same we have had before. Most ReScience C papers describe *replications*, meaning that they provide code that reimplements methods previously published in the scientific literature, and report on the similarities of the obtained results. A more recent article type is the *reproduction* report, inspired by our [ten-year challenge](http://rescience.github.io/ten-years/), in which authors describe the adventure of trying to re-run old scientific software and reproduce published results. For articles *about* replication and reproduction issues in computational science, we have the article type *letter*. Finally, there is the *editorial*, such as the one you are reading right now, but beware that you have to join our editorial board before we will consider your editorial submissions!

# The reviewing process

Our new publishing infrastructure also manages the reviewing process. We hope that it will become more streamlined and faster, because editors can now see at a glance which submissions are in which stage of reviewing. Our editors are also assisted by a bot, which handles mechanical tasks such as recompiling papers upon revisions, watching the review checklists for completion, etc. The bot introduces itself at the beginning of each review, providing instructions for interacting with it.

The reviewing process submission will be overseen by one of our *topic editors*. Their role is to invite reviewers, nudge them towards completing the reviews, provide feedback on the reviews, and answer questions about ReScience C policies and processes that authors or reviewers might have. Topic editors make up the lion's share of our editorial board. We also have *associate editors-in-chief*, roughly one per academic discipline. They assign a topic editors to each new submission, and help them when necessary, in particular with questions concerning ReScience policies and processes. Finally, we have the *editors-in-chief*, who recruit the other members of the editorial board, assist them as necessary, and refuse offers by mega-publishers wishing to take over ReScience C.

# Publication

- DOIs: Crossref rather than DataCite

# Migration from the old publishing system

- Existing submissions will continue to be handled the old way.
- Question: Do we import the old articles into the new platform?

# Acknowledgements

[Juanjo Bazán](https://github.com/xuanxu) developed our new Web site and management platform.

