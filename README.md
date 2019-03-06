This repository includes code use in the article:

#  **Comparative evolutionary analysis and prediction of genomic diversity patterns between sorghum and maize**
![language: R](https://img.shields.io/badge/language-R-blue.svg)
![language: Python](https://img.shields.io/badge/language-Python-green.svg)
![status: WIP](https://img.shields.io/badge/status-WorkInProgress-red.svg)

![alt text](https://github.com/GoreLab/Sorghum-HapMap/blob/master/CIRCOS/GitHub_figure.svg)

## **Building the Sorghum HapMap** (_`/HAPMAP/Sorghum-HapMap`_)

  ### SNP calling: 
*0_Sentieon_BWA_Batch5.sh* - Sample of alignment file using BWA  
*1_Sentieon_merge_and_remove_duplicates.sh* - Merging Bam files according to Figure S2A  
*2_bam_stat.sh* - Calculate alignment stats  
*3_Sentieon_GATK_command_line_Indel_realigner.sh* - Realign reads around InDels  
*4_Sentieon_GATK_command_line_Recal_providing_list.sh* - Recalibration using high quality positions 
*5_Sentieon_GATK_command_line_HC_step2.sh* - Haplotypes (produces gVCFs)  
*6_joint_variant_calling.sh* - Call the variants and produce a VCF file.
    
  ### Describing the Population:

  *Population_structure_pub.Rmd:* - Calculates principal component analysis on the marker matrix using SNPrelate. Plots included  
  *MAF_FST.Rmd* - Calculates Allele frequency spectrum and FSTs between races  
  *Duplicates* - Checking the duplicates IBS matrix  
  *Linkage_disequilibrium.Rmd* - Code use to plot local LD plot and classic LD decay plots.  
  
  ### Misc:
*Filter_MAF_OE.py* - Extract monomorphic sites and sites with a threshold of heterozygosity   
*count_fastq.sh* - Count the number of reads in a fastq  
*vcfaddanot.py* - Add allele balancing field AB in a vcf file  

  
## **Deleterious alleles:**





## **Evolutionary model:**

  ### Defining  sorghum genome windows.- 
  The midpoint distance between adjacent genes was calculated and a series of intervals that covered each chromosome from start to end were calculated. In total, the sorghum genome was divided into 34,028 fragments.
  Go to `Sorghum-HapMap/Evol_model/Windows/` for details. 


  ### Recombination rates.-

  *FASTEPRR.R:* Wrappper to calculate rho across the genome in fixed windows

  *FASTEPRR_segments.R:* Wrapper to calculate rho across windows specified in a bed file

  *Recombination_Rates.Rmd:* R Notebook for plotting recombination rates across the chromosomes together with gene density 

  ### Genetic diversity (Pi).-
  
  ### GERP (Genomic evolutionary rate profiling).-
  
  ### TAU (SSW 20bp alignment between sorghum and maize).- 

  ### Circos Plots: (/CIRCOS/)
  *1_gene_density.py:* - Calculates gene density per chromosome from a gff3 file  
  *CIRCOS/cplot/ :* - includes conf files (circos.conf, ideogram.conf, mycolors.conf and ticks.conf) also includes the output in png and svg formats  
  
  ## Data availability:
  The raw sequencing data is available through the NCBI BioProject **PRJNA513297**. Alignment Bam files are available through the CyVerse repository #######. Code used throughout the article is available through this GitHub repository. For any other inquiry please contact the authors directly. 
  
