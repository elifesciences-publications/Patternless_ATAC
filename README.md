### This code is associated with the paper from Soluri et al., "Zygotic pioneer factor activity of Oddpaired/Zic is necessary for late function of the _Drosophila_ segmentation network". eLife, 2020. http://doi.org/10.7554/eLife.53916


This repository contains a markdown describing the core analysis of the ATAC-seq data published in Soluri et al (Biorxiv 2019). There are two versions of the markdown, 1) an .rmd file with executable code; 2) an .html file with the output of this code run by the authors. The analysis was done in R. All supporting files, unless they have a .txt file extension, are R-formatted files as well. Most are "Genomic Ranges" objects. 

This is intended to document the analysis described in Soluri et al, but it is possible that users may want to reproduce the analysis for themselves, or to adapt the code for their own work. We've tried to explain choices made along the way to facilitate any adaptations that users may want to make. 

There are MACS2-generated peaks lists for the "Patternless ATAC" dataset, as well as peaks for ChIP against myc-tagged Odd-paired. There are two types of count data included as well. For samples that are subjected to DESeq, we've included GenomicRangesList objects with the locations of all short (open) ATAC fragments. These are essentially R-formatted versions of .bam file data that just report the mapped positions of short reads. In addition, there are .wig style coverage datasets, also in Genomic Ranges format, that are used for plotting coverage over example regions. If desired, these could easily be converted to UCSC-compatible (or IGV compatible, I guess) files using `rtracklayer`. 

While this is not meant to replace an SRA/GEO submission, I think that for many prospective users, this data might be more useful than the raw sequencing data itself. Once the GEO submission is completed/made public, this file will be updated with that information.
