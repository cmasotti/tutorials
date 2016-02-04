# **tutorials**
# From fastq files to FPKM data

## Softwares to download, install, and add to $PATH  
>How to add the applications to $PATH (options):  
+ Directly write in .bashrc file:  
**export PATH=PATH:/pathway/to/software_directory**    
then: **source ~/.bashrc**    
+ Copy executable files from software_directory/bin to /user/local/bin  
+ Create symbolic links (ln –s) to executables in /user/local/bin  

**_BEDtools (version 2.25.0)_**  
http://bedtools.readthedocs.org  
Download: https://github.com/arq5x/bedtools2/releases  

```bash
wget https://github.com/arq5x/bedtools2/releases/download/v2.25.0/bedtools-2.25.0.tar.gz  
cd bedtools-2.25.0  
tar zxvf bedtools-2.25.0.tar.gz  
cd bedtools2/  
make  
cp bin/\* usr/local/bin/.   
```

**_SAMtools (version 0.1.18)_**  
```bash
http://sourceforge.net/projects/samtools/files/samtools/0.1.18/   
wget http://sourceforge.net/projects/samtools/files/samtools/0.1.18/samtools-0.1.18.tar.bz2  
tar zxvf samtools-0.1.18.tar.bz2  
cd samtools-0.1.18  
make  
export PATH=PATH:/pathway/to/samtools-0.1.18  
source ~/.bashrc  
```
**_FastQC_**  
http://www.bioinformatics.babraham.ac.uk/projects/fastqc/  
Requirement: suitable Java Runtime Environment  
```bash
wget http://www.bioinformatics.babraham.ac.uk/projects/fastqc/fastqc_v0.11.4.zip  
```
Unzip and load the application  
  
**_Bowtie 2.1.0_**  
http://sourceforge.net/projects/bowtie-bio/files/bowtie2/2.1.0/  
```bash
wget http://sourceforge.net/projects/bowtie-bio/files/bowtie2/2.1.0/bowtie2-2.1.0-linux-i386.zip  
unzip bowtie2-2.1.0-linux-i386.zip  
cd bowtie2-2.1.0  
```
Copy all executables below to ~/usr/local/bin/.   
+ bowtie2
+ bowtie2-align
+ bowtie2-align-debug
+ bowtie2-build
+ bowtie2-build-debug
+ bowtie2-inspect
+ bowtie2-inspect-debug  

**_TopHat (version 2.0.3)_**  
http://ccb.jhu.edu/software/tophat/downloads/  
```bash
wget http://ccb.jhu.edu/software/tophat/downloads/tophat-2.0.3.0.Linux_x86_64.tar.gz  
tar zxvf tophat-2.0.3.0.Linux_x86_64.tar.gz  
cd ~/usr/local/bin  
ln –s ~/tophat-2.0.3.0.Linux_x86_64/tophat2 .  
```

**_Cufflinks (version 2.2.1)_**  
http://cole-trapnell-lab.github.io/cufflinks/manual/  
```bash
wget http://cole-trapnell-lab.github.io/cufflinks/assets/downloads/cufflinks-2.2.1.Linux_x86_64.tar.gz  
tar zxvf  cufflinks-2.2.1.Linux_x86_64.tar.gz  
cd cufflinks-2.2.1.Linux_x86_64  
```
Copy all executables below to  ~/usr/local/bin/.  
+ cuffcompare  
+ cuffdiff
+ cufflinks
+ cuffmerge
+ cuffnorm
+ cuffquant
+ gtf_to_sam
+ gffread  

**_R packages_**  
Open R session to install packages:  
```R 
# ggplot2: https://cran.r-project.org/web/packages/ggplot2/ggplot2.pdf  
install.packages(“ggplot2”)  
install.packages(“grid”)  
install.packages(“gridExtra”)  

# Plyr: https://cran.r-project.org/web/packages/plyr/plyr.pdf  
install.packages(“plyr”)  

Reshape: https://cran.r-project.org/web/packages/reshape/reshape.pdf  
install.packages(“reshape”)  

# CummRbund: http://bioconductor.org/packages/release/bioc/html/cummeRbund.html  
# Requirement: Bioconductor release 3.2  
source("https://bioconductor.org/biocLite.R")  
biocLite("cummeRbund")  
```
## Raw RNAseq data  
**SRA=Sequence Read Archive**  
http://www.ncbi.nlm.nih.gov/sra  
Raw sequencing and alignment data available to research community!  

_Illumina Human Body Map 2.0 Transcriptome Project_  
http://www.ncbi.nlm.nih.gov/Traces/study/  
SRA Study: ERP000546  
Samples: ERR030874, ERR030872, ERR030875, ERR030873, ERR030876, ERR030885, ERR030878, ERR030882, ERR030886, ERR030887, ERR030883, ERR030880, ERR030881, ERR030877, ERR030884, ERR030879.  
  
## Reference Files    
We need a genome against which to align our reads (fasta file):  
_Download the reference genome (hg19 – GRCh37; Feb 2009 assembly)_  
```bash
wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/chromosomes/chr19.fa.gz  
gunzip chr19.fa.gz  
```
We need a reference gene annotation to quantify expression of known transcripts (.gtf file):  
_Download the human GENCODE Gene Set_   
GENCODE: http://www.gencodegenes.org/releases/  
```bash
wget ftp://ftp.sanger.ac.uk/pub/gencode/Gencode_human/release_16/gencode.v16.annotation.gtf.gz  
gunzip gencode.v16.annotation.gtf.gz  
grep chr19 gencode.v16.annotation.gtf > gencode.v16.annotation_chr19.gtf  
```
## Files needed for this tutorial  





## References


