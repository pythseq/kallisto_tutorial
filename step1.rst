|CyVerse logo|_

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_


Organize Kallisto Input Data
-----------------------------

**Description:**

Kallisto has relatively few input requirements. You will need to have either
single or paired end reads, as well as a refference transcriptome. It is suggested
that your RNA-Seq reads are analyzed using `FastQC <https://cyverse-fastqc-quickstart.readthedocs-hosted.com/en/latest/>`_,
followed by any additional trimming and filtering using and application such as
`Trimmomatic <https://cyverse-trimmomatic-quickstart.readthedocs-hosted.com/en/latest/>`_.

.. note::

    **About the Sample Dataset**
    In this tutorial, we are using publically available data from the SRA. This
    tutorial will start with cleaned and processed reads. The SRA experiment used
    data from bioproject PRJNA272719 `<https://www.ncbi.nlm.nih.gov/bioproject/PRJNA272719>`_.
    The abstract from that project is reprinted here:

    'To survey transcriptome changes by the mutations of a DNA demethylase ROS1
    responding to a phytohormone abscisic acid, we performed the Next-gen
    sequencing (NGS) associated RNA-seq analysis. Two ROS1 knockout lines
    (ros1-3, ros1-4; Penterman et al. 2007 [PMID: 17409185])
    with the wild-type Col line (wt) were subjected. Overall design:
    Three samples (ros1-3, ros1-4 and wt), biological triplicates, ABA or mock
    treatment, using Illumina HiSeq 2500 system' `[citation] <https://www.ncbi.nlm.nih.gov/bioproject/PRJNA272719>`_.

----

**Input Data:**

.. list-table::
    :header-rows: 1

    * - Input
      - Description
      - Example
    * - Refference transcriptome
      - fasta
      - `Example transcriptome <http://datacommons.cyverse.org/browse/iplant/home/shared/cyverse_training/tutorials/kallisto/01_input_transcriptome>`_

*Importing Reference  Transcriptome*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

In this example, we will import a reference transcriptome for Arabidopsis from
Ensembl. In many cases you can find an appropriate transcriptome from Ensembl
for your organism of interest, or provide your own fasta-formmatted transcriptome.

  1. Go to the Ensembl Plants Arabidopsis page:|ensembl|.

  2. In the 'Gene annotation' section, click on the 'Download genes, cDNAs, ncRNA,
     proteins' 'FASTA' link:|fasta link|.

  3. The transcriptome files will be located in the 'cdna' folder: |ftp link|.

  4. Right-click/command-click on the `Arabidopsis_thaliana.TAIR10.cdna.all.fa.gz`
     and copy the link location/URL to the clipboard

  5. Login to the CyVerse |discovery_enviornment|. 

  6. In your home directory, create a folder to organize your Kallisto project

  7. In the created folder, go to the 'Upload' menu, and select, 'Import from URL...';
     paste in the Ensembl link and click 'Import from URL' to begin the import


**Output/Results**

.. list-table::
    :header-rows: 1

    * - Output
      - Description
      - Example
    * - Reference transcriptome
      - fasta
      - `Example transcriptome`_


----

**Description of results and next steps**

This example transcriptome will be indexed in the next step. RNA-Seq reads will
be mapped against this set of transcripts. Once you have the transcriptome and
your RNA-Seq reads, you can proceed with the next step. We suggest organizing
your RNA-Seq reads in the folder created in step 6 above.

----

**Fix or improve this documentation**

- On Github: `Repo link <https://github.com/CyVerse-learning-materials/kallisto_tutorial>`_
- Send feedback: `Tutorials@CyVerse.org <Tutorials@CyVerse.org>`_

----

|Home_Icon|_
`Learning Center Home <http://learning.cyverse.org/>`_

.. |CyVerse logo| image:: ./img/cyverse_rgb.png
    :width: 500
    :height: 100
.. _CyVerse logo: http://learning.cyverse.org/
.. |Home_Icon| image:: ./img/homeicon.png
    :width: 25
    :height: 25
.. _Home_Icon: http://learning.cyverse.org/

.. |ensembl| raw:: html

    <a href="http://plants.ensembl.org/Arabidopsis_thaliana/Info/Index" target="_blank">http://plants.ensembl.org/Arabidopsis_thaliana/Info/Index</a>

.. |fasta link| raw:: html

    <a href="ftp://ftp.ensemblgenomes.org/pub/plants/release-36/fasta/arabidopsis_thaliana/" target="_blank">ftp://ftp.ensemblgenomes.org/pub/plants/release-36/fasta/arabidopsis_thaliana/</a>

.. |ftp link| raw:: html

    <a href="ftp://ftp.ensemblgenomes.org/pub/plants/release-36/fasta/arabidopsis_thaliana/cdna/" target="_blank">ftp://ftp.ensemblgenomes.org/pub/plants/release-36/fasta/arabidopsis_thaliana/cdna/</a>

.. |discovery_enviornment| raw:: html

    <a href="https://de.cyverse.org/de/" target="_blank">Discovery Environment</a>
