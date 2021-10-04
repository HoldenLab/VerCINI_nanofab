# VerCINI_nanofab
Code for nanofabrication of silicon micropillars

This repository contains files that can be used to produce arrays of square micropillars on a silicon wafer. The patterned wafers can be used as molds for use with Vertical Cell Imaging by Nanostructured Immobilization (VerCINI) and Microfluidic VerCINI (uVerCINI).

The files are as follows:

- Microholes_noarray_171027_2.dxf: A file containing a very simple pattern - a 1x1 square.
- 20180410_Microholes_square_beamer_25BSS.ftxt: A file to be opened in BEAMER (GenISys) that contains the code for producing arrays of squares as a pattern of dots to be written by an e-beam system. This code takes the simple square pattern in Microholes_noarray_171027_2.dxf and outputs several arrays of squares of varying sizes, all spaced by 5 um. Each array is the size of the e-beam main field.
- 20180105_Microholes_square_25nmBSS_1.\*.gpf: Files output from the BEAMER code. Each is an array of squares of a given size (1.7, 1.8, 1.9, and 2.0 um) spaced by 5 um (right edge to right edge) roughly the size of the main field of the Raith EBPG-5000+ e-beam system (~1x10^6 um^2). The beam step size is 25 nm.
- kpillar19.cjob: A file to be opened in Cjob (Vistec Lithography) that contains the code for exporting a job to the e-beam system. This code makes four square arrays - one in each wafer quadrant. Each array has four columns of different sized squares - each taken from the gpf files that were output from the BEAMER code. The arrays from the gpf files are replicated 10 times each to produce larger arrays. Identifiers are also included so that the sizes of squares can be identified throughout the nanofabrication process, as well as during microscopy later. A solid rectangle is also included so that the pillar heights can later be measured with a stylus profilometer.
- kpillar19_Microholes5.job: A job file exported from Cjob that can be directly written by an e-beam system.
