# Simons Genome Diversity Project

This repo contains scripts for downloading files from the Simons Genome
Diversity project. Also, in the `raf` directory, scripts for generating
files in .raf format. The repo doesn't have the data files or the .raf
files.

## samples.txt

This file was downloaded from [here][metainfo]. The original name,
"`10_24_2014_SGDP_metainformation_update.txt`" has been shortened to
"samples.txt".

## pops.txt

This file contains 3 columns: (1) the number of samples in a
population, (2) the region in which the population is located, and (3)
the name of the population. It was generated like 
this:

    awk 'BEGIN {OFS="\t"} {print $7, $6}' samples.txt | sort |
    uniq -c > pops.txt

This file groups the Tlingit under CentralAsiaSiberia. They actually
live in Canada.

## harris-ftplist.txt

This file gives the URL where each sample is available. I got it from
Nathan Harris. I haven't been able to figure out where he got it.

## population directories

The subdirectories contain scripts for downloading SGDP data for each of
several populations.

## raf

Scripts for making raf files and (on the server but not the repo) the files
themselves.

[metainfo]:
http://simonsfoundation.s3.amazonaws.com/share/SCDA/datasets/10_24_2014_SGDP_metainformation_update.txt
