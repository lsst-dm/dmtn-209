.. image:: https://img.shields.io/badge/dmtn--209-lsst.io-brightgreen.svg
   :target: https://dmtn-209.lsst.io
.. image:: https://travis-ci.com/lsst-dm/dmtn-209.svg
   :target: https://travis-ci.com/lsst-dm/dmtn-209

###################################################
Rubin Science Platform on Google: the story so far.
###################################################

DMTN-209
========

In 2020 Rubin Observatory made a tender for a three year interim data facility. This was won by Google. In partnership with Google we have now deployed the first externally used version of the Rubin Science Platform consisting of a jupyter environment and a portal. Sitting behind this is TAP access to our project developed large scale database Qserv holding a synthetic catalogue of 140 million objects  and around 500TB of simulated  images. This is  hosted on Google Cloud Platform  using Terraform and Kubernetes. The initial few hundred users were given access to this in July 2021. In this talk we will describe the system, the initial use and the coming years. 

Links
=====

- Live drafts: https://dmtn-209.lsst.io
- GitHub: https://github.com/lsst-dm/dmtn-209

Build
=====

This repository includes lsst-texmf_ as a Git submodule.
Clone this repository::

    git clone --recurse-submodules https://github.com/lsst-dm/dmtn-209

Compile the PDF::

    make

Clean built files::

    make clean

Updating acronyms
-----------------

A table of the technote's acronyms and their definitions are maintained in the `acronyms.tex` file, which is committed as part of this repository.
To update the acronyms table in ``acronyms.tex``::

    make acronyms.tex

*Note: this command requires that this repository was cloned as a submodule.*

The acronyms discovery code scans the LaTeX source for probable acronyms.
You can ensure that certain strings aren't treated as acronyms by adding them to the `skipacronyms.txt <./skipacronyms.txt>`_ file.

The lsst-texmf_ repository centrally maintains definitions for LSST acronyms.
You can also add new acronym definitions, or override the definitions of acronyms, by editing the `myacronyms.txt <./myacronyms.txt>`_ file.

Updating lsst-texmf
-------------------

`lsst-texmf`_ includes BibTeX files, the ``lsstdoc`` class file, and acronym definitions, among other essential tooling for LSST's LaTeX documentation projects.
To update to a newer version of `lsst-texmf`_, you can update the submodule in this repository::

   git submodule update --init --recursive

Commit, then push, the updated submodule.

.. _lsst-texmf: https://github.com/lsst/lsst-texmf
