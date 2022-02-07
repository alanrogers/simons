# Simons Genome Diversity Project

## samples.txt

This file was downloaded from
[here](http://simonsfoundation.s3.amazonaws.com/share/SCDA/datasets/10_24_2014_SGDP_metainformation_update.txt). The
original name, "`10_24_2014_SGDP_metainformation_update.txt`" has been
shortened to "samples.txt".

## pops.txt

This file contains 2 columns: (1) the number of samples in a
population, and (2) the name of the population. It was generated like
this:

    awk '{print $6}' samples.txt | sort | uniq -c > pops.txt

