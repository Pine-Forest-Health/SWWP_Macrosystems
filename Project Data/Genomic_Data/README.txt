#Mitra Menon, 21-May-2020####

##############################################
#Pipeline for SNP calling and filtering#####


All fasta files were trimmed to 80bp, because of bad quality towards the tails for several files. 

1. denovo reference generated using a subset of individuals, with atleast one individual representing each population.
2. SNPs called using all individuals, NAU samples and FIA samples. This gave me a total of 3,97,671 SNPs.
 *Step 1 & 2 were done in dDocent
 
3. Filtering steps on 012 coded file (coded for count of minor allele).:
https://github.com/EckertLab/protocols/blob/master/ddRAD-seq%20data%20processing.md

This process retained 49859 SNPs that is provided in this directory.




#######################
****File details********
#########################
minor012.txt
This file contains SNP data (coded 012) along with population, individual tree ID, mean lat-long for each population and the group the individual was classified into. 
Groups are: LP, MX, US, 113, 114 & unk. Unknown includes LPI (which may actually be LSI).
Some of the NAU samples will contain "merge" in front of them. That just means that for a specific individual I merged multiple fasta files prior to SNP calling because we had duplicates.
Some samples will contain "unk", this usually happens with trees for which there are "FOL" and maternal trees. "unk" just means that I was not able to resolve whether that specific tree is foliage only tree or a maternal tree.

FIA samples were recoded because the names were too long to input into dDocent. 
The corresponding original IDs for these samples is in FIA_sampleInfo.xlxs

	
