These files represent the many ways someone can acquire or create a genome file. The many sources are tested because the source and add or delete components that are important to KBase import.

In KBase, the file must have a valid file extension. The current valid extensions are .gbff, .gbk, .gb, .genbank, and .dat. In addition, files can be compressed. Currently, KBase will recognize .gz, .zip, and .tar.gz. Other may be possible but they haven’t been explicitly tested.

Data can come from many sources including, GenBank/Refseq, EMBL, PATRIC, KEGG, JGI/IMG and many other potential sources. Files from GenBank have used all but the .dat extension. Files downloaded from the EMBL plants web site use the .dat extension. EMBL allows users to download genomes in text format but no extension is given and it isn’t clear that they cleanly fit into one of the acceptable formats. 

It is possible for users to create a file in one format but give it a name from a different format. KBase will use the format specified in the “Source” pulldown. If a file is in EMBL format, no matter what the extension, then Ensembl needs to be selected as the source.

GBFF format

Genbank uses .gbf and .gbff extensions for genomes at their ftp site. The .gbff format can support one or more contigs, chromosome, or plasmids. Testing will be for both one and two chromosome files and for uncompressed, .gz, and .zip formats.

One_chr_NC_018414.gbff
One_chr_NC_018414.gbff.gz
One_chr_NC_018414.gbff.zip
Two_chr_Shewanella.gbff
Two_chr_Shewanella.gbff.gz
Two_chr_Shewanella.gbff.zip

GBK format

Individual contigs, chromosomes, or plasmids can be downloaded from GenBank in .gbk format. Users can take the individual files and combine them in a number of ways to represent 2 or more contigs/chromosomes.  The files can be concatenated together, they can be combined into a .zip file, they can be tar’d and gzipped. The .gbk test files are:

One_chr_NC_006908.gbk
One_chr_NC_006908.gbk.gz
One_chr_NC_006908.gbk.zip
Two_chr_Variovorax.gbk.tar.gz
Two_chr_Variovorax.gbk.zip
Two_chr_concat_Variovorax.gbk
Two_chr_concat_Variovorax.gbk.gz

GB format

At GenBank, .gb is used in the same way that .gbk files are used. They represent an individual contig or chromosome. Only a subset of the permutations represented in .gbk files are in this test list:

One_chr_NC_006908.gb
One_chr_NC_006908.gb.zip
Two_chr_Variovorax.gb.zip

GENBANK format

The .genbank format is just another name for .gbk files. It is sometimes used to distinguish them from other formats. The test files include:

One_chr_NC_006908.genbank
One_chr_NC_006908.genbank.zip
Two_chr_Variovorax.genbank.zip

DAT format

It is possible for users to take a file in GenBank format and name it .dat. These files test to make sure that the importer uses the correct format, even though the extension belongs to EMBL dat.

One_chr_RefSeq_NC_006908.dat
One_chr_RefSeq_NC_006908.dat.zip
Two_chr_RefSeq_Variovorax.dat.zip

IMG/JGI

Users can download genomes from IMG in .gbk format. The test file is:

JGI_Variovorax_EPS.gbk

PATRIC

Users can download genomes from PATRIC in . gbk format. The test file is:

PATRIC.1005471.3.RefSeq.gbk

KEGG

Users can download genomes from KEGG in . gbff format. The test file is:

KEGG_ecoli_GCA_000184185.1.gbff.gz

Ensembl/EMBL
At EMBL, it is possible to find a genome of interest and select text as a download option. The files look like EMBL format and they can be named .dat but I haven’t had any luck getting them to load. They are probably bad examples. The tool Artemis was used to convert one to .gbk format but it is missing header information and won’t load for that reason.

EMBL_two_chr.dat.zip
Embl_CP003541.embl.dat
Embl_CP003541.embl.dat.gz
Embl_artemis_ecoli.gbk

Ensembl plants has a download page with options for both EMBL and GenBank formats. These files are from that site.

Arabidopsis_thaliana.TAIR10.34.chromosome.Mt.dat
Arabidopsis_thaliana.TAIR10.34.chromosome.Mt.dat.gz

KBASE

KBase has an option to download genomes. Some of those genomes are from the Public/Example tab and some will be uploaded by users. Uploaded files can include any of the formats above or they can come from FTP and HTTP sites. Another factor in success has to do with the evolving nature of the files that are downloaded. Their format has changed at least once.

Public genomes seem to work:

KBase_kb_g.239994.c.16.gbk
KBase_kb_g.399.c.1.gbk

Genome imported in December 2016 and January 2017 have problems but the problems are different. The December genomes didn’t have any IDs and the advanced option to “Generated IDs if needed” would create IDs. The January genomes have IDs in the form of kbase_id= but the importer doesn’t recognize them. It has an error about missing protein translations. Both downloads have errors about invalid date formats and there aren’t any dates.

KBase_Dec_imported_genome.gbk
KBase_Jan_imported_Mycoplasma.gbk

Users can add a genome to KBase using FTP, download it at some point, and later try to upload it.

KBase_ftp_then_download_to_local.gbff

FTP of multi-chromosome  .gbff.gz file at genbank
ftp://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/000/010/365/GCA_000010365.1_ASM1036v1/GCA_000010365.1_ASM1036v1_genomic.gbff.gz

FTP of single .dat.gz file from Ensembl plants
ftp://ftp.ensemblgenomes.org/pub/release-34/plants/genbank/arabidopsis_thaliana/Arabidopsis_thaliana.TAIR10.34.chromosome.Mt.dat.gz

FTP of .gbf file from PATRIC
ftp://ftp.patricbrc.org/patric2/genomes/1005471.3/1005471.3.RefSeq.gbf
This format isn’t support despite what the error messages tell you.

HTTP of single chromosome .gbk.gz
http://genome.ornl.gov/~ml3/One_chr_Mycoplasma.gbk.gz

