

Hello there 😄 Welcome to this Jupyter Book instance to document mainly a data analysis workflow for analysing data from the technique : **S**aturated **T**ransposition **A**nalysis in **Y**east. 

## Status of the project
- Beta release on Zenodo 
- Lacking automated tests
  
### Next steps
<!-- 
1. Make the software package ready to be published in [Journal of Open Source Software](https://joss.readthedocs.io/en/latest/index.html)

    - Automated testing with continuous integration
    - Comand line interface with a pip install mode
    - GitFlow implementation for contributors to the software -->

<!-- 3.  Make a plan how to define trimming and alignment settings.
Currently the trimming and processing options are chosen by trial-and-error.
Each dataset requires unique processing and therefore no fixed settings for the trimming and alignment can be determined, but potentially some guidelines can be created that helps for the processing. -->

<!-- 4. The code is relying on software third party software tools (e.g. for the trimming, alignment and quality checking).
This currently requires to be installed manually and in the [workflow](https://github.com/leilaicruz/LaanLab-SATAY-DataAnalysis/blob/master/satay.sh) paths need to be set to some these tools (in satay.sh, the paths are all defined in the beginning of the script in the `DEFINE PATHS` section). This is not convenient for other users and is prone to errors.
Therefore a package need to be created that installs the third party software tools at a fixed location relative to the workflow.
Then the paths doesn't have to set manually by the user and makes it easier to set up and use. -->
<!-- 
5. Implementing unit testing in the Github repository. This allows for automatic testing of the codes after changes have been made in the repository and should ensure the outcome is still correct.
Most importantly this needs to be implemented in the [transposonmapping_satay.py](https://github.com/leilaicruz/LaanLab-SATAY-DataAnalysis/blob/master/python_transposonmapping/transposonmapping_satay.py) code (the final step of the processing pipeline) and the depending [python modules](https://github.com/leilaicruz/LaanLab-SATAY-DataAnalysis/tree/master/python_transposonmapping/python_modules).
The other processing steps are all relying on third party software that probably already some testing implemented. -->

<!-- 6. For the transposon mapping in the pipeline [a custom python script](https://github.com/leilaicruz/LaanLab-SATAY-DataAnalysis/blob/master/python_transposonmapping/transposonmapping_satay.py) is created that inputs a bam file and outputs lists of insertion locations and the corresponding number of reads. This script is based on the [matlab code](https://sites.google.com/site/satayusers/complete-protocol/bioinformatics-analysis/matlab-script) from the Kornmann lab.
The matlab code contained some bugs that were solved in the python script (see the [satay forum](https://groups.google.com/g/satayusers/search?q=matlab)). Therefore some small differences may be present between the matlab processing and the python processing. But recently, some more differences were found that could not be explained by the matlab bugs.
The exact cause is yet unclear, but has maybe to do with reading the samflag in the python script (line 183 in the original [transposonmapping_satay.py]((https://github.com/leilaicruz/LaanLab-SATAY-DataAnalysis/blob/master/python_transposonmapping/transposonmapping_satay.py)) code which uses the [samflag.py](https://github.com/leilaicruz/LaanLab-SATAY-DataAnalysis/blob/master/python_transposonmapping/python_modules/samflag.py) module).
The insertions found by the transposon mapping python scripts can be compared with IGV that loads the corresponding bam file.
This shows the read locations so the output of the transposon mappping script can be manually checked. -->

<!-- 7.  Currently [BWA](http://bio-bwa.sourceforge.net/bwa.shtml) is used for the alignment of the reads.
This tools work fine, but the Kornmann lab (and many other labs) use [Bowtie](http://bowtie-bio.sourceforge.net/index.shtml).
This is already installed on the Linux machine, but needs to be implemented in the [workflow](https://github.com/leilaicruz/LaanLab-SATAY-DataAnalysis/blob/master/satay.sh).
The current aligner is implemented in the section `SEQUENCE ALIGNMENT`.
Note to set the option for paired-end and single-end alignment for bowtie (defined in the variable `${paired}`). -->

<!-- 8. Allow mulitple files to be processed at once using a for-loop in the [bash script](https://github.com/leilaicruz/LaanLab-SATAY-DataAnalysis/blob/master/satay.sh).
Currently only one dataset at the time can be processed, but this can be extended to allow a series of datasets to be processed in a for-loop.
To allow for this, the bash script satay.sh should be altered where the code between line 285 and line 680 (of the original code) should be placed in a loop over all file paths.
Ideally each dataset is located in a separate folder where the output folders and files are stored for that particular dataset.
If multiple datasets are located in the same folder, it might happen that things are being overwritten.
It is possible to put all datasets to be processed in the same folder, but then in the code all these datasets should be automatically be moved to individual folders.
Note to pay attention that the paths to the datasets are all correct in the for-loop. -->

<!-- 9. Automated documentation based on the help texts from the python scripts. -->


:::{panels}
:container: +full-width text-center
:column: col-lg-6 px-2 py-2
:card:

**Publication in JOSS** ✍
^^^
Make the software package ready to be published in [Journal of Open Source Software](https://joss.readthedocs.io/en/latest/index.html)

  <!-- - Automated testing with continuous integration
    - Comand line interface with a pip install mode
    - GitFlow implementation for contributors to the software -->

---
**Data sequencing processing gudelines** 🚀
^^^
Each dataset requires unique processing and therefore no fixed settings for the trimming and alignment can be determined, but potentially some guidelines can be created that helps for the processing.

---
**Unit testing continous integration** ✨
^^^
Unit testing implemented in the main functions to make the pipeline more maintanable and prevent crashes when customizing it. 

---
**Multiple files analysis** 🎁
^^^
Allow mulitple files to be processed at once using a for-loop in the bash script.
Currently only one dataset at the time can be processed, but this can be extended to allow a series of datasets to be processed in a for-loop.
<!-- - To allow for this, the bash script satay.sh should be altered where the code between line 285 and line 680 (of the original code) should be placed in a loop over all file paths.
Ideally each dataset is located in a separate folder where the output folders and files are stored for that particular dataset.
If multiple datasets are located in the same folder, it might happen that things are being overwritten.
It is possible to put all datasets to be processed in the same folder, but then in the code all these datasets should be automatically be moved to individual folders.
Note to pay attention that the paths to the datasets are all correct in the for-loop. -->

---
**Python package** 🛰
^^^
Build a python package that is pip installable for the ease of use for other researchers. 

---

**Tutorials** 📝
^^^
Make tutorials of usage of the pipeline 

---

:::





:::{admonition} Learn more and get involved
:class: tip full-width

💡 [Open an issue](https://github.com/SATAY-LL/LaanLab-SATAY-DataAnalysis/issues)
: We track enhancement requests, bug-reports, and to-do items via GitHub issues.


🙌 [Send a pull request](https://github.com/SATAY-LL/LaanLab-SATAY-DataAnalysis/pulls)
: We appreciate that contributors send a pull request to improve the code base or introduce a new feature. 
:::


## What do we have currently?

- [![DOI](https://zenodo.org/badge/248577762.svg)](https://zenodo.org/badge/latestdoi/248577762)
- [Download here the Public release v1.0.beta-1](https://github.com/leilaicruz/LaanLab-SATAY-DataAnalysis/archive/refs/tags/v1.0-beta.1.zip)


## Software License

- [![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
- This work is licensed under Apache 2.0 . 
The 2.0 version of the Apache License, approved by the ASF in 2004, helps us achieve our goal of providing reliable and long-lived software products through collaborative open source software development. 

## Current Contact 

- Leila Inigo de la Cruz
    - email: L.M.InigoDeLaCruz@tudelft.nl


## Acknowledgements 💙

- Many thanks to the group of [Prof. Benoit Kornmann](https://www.bioch.ox.ac.uk/research/kornmann) , in particular to [Prof. Agnes Michel](https://www.kornmann.group/people/agn%C3%A8s) , for all the nice discussions and colaboration with our team. Also thanks to them due to the [SATAY forum](https://groups.google.com/forum/#!forum/satayusers)  they keep on running for all the community of satayers 🎉 . 

- Many thanks to the [DCC department at TU Delft](https://tu-delft-dcc.github.io/01_Welcome.html), specially to [Maurits Kok](https://github.com/mwakok) who in his role of Research Software Engineer has supported us in developing the software package to be distributed to the scientific community. 

<!-- :::{image} https://pbs.twimg.com/profile_images/1226944724365447169/MzFpwY5P_400x400.png
:class: float-left mr-2 rounded
:width: 100px
::: -->