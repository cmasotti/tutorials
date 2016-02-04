# **tutorials**
# From fastq files to FPKM data

## Working data

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
**wget https://github.com/arq5x/bedtools2/releases/download/v2.25.0/bedtools-2.25.0.tar.gz**  
**cd bedtools-2.25.0**  
**tar zxvf bedtools-2.25.0.tar.gz**  
**cd bedtools2/**  
**make**  
**cp bin/\* usr/local/bin/.**   
  
**_SAMtools (version 0.1.18)_**  
http://sourceforge.net/projects/samtools/files/samtools/0.1.18/  
**wget http://sourceforge.net/projects/samtools/files/samtools/0.1.18/samtools-0.1.18.tar.bz2**  
**tar zxvf samtools-0.1.18.tar.bz2**  
**cd samtools-0.1.18**  
**make**  
**export PATH=PATH:/pathway/to/samtools-0.1.18**  
**source ~/.bashrc**  
  
**_FastQC_**  
http://www.bioinformatics.babraham.ac.uk/projects/fastqc/  
Requirement: suitable Java Runtime Environment  
**wget http://www.bioinformatics.babraham.ac.uk/projects/fastqc/fastqc_v0.11.4.zip**  
Unzip and load the application  
  
**_Bowtie 2.1.0_**  
http://sourceforge.net/projects/bowtie-bio/files/bowtie2/2.1.0/  
**wget http://sourceforge.net/projects/bowtie-bio/files/bowtie2/2.1.0/bowtie2-2.1.0-linux-i386.zip**  
**unzip bowtie2-2.1.0-linux-i386.zip**  
**cd bowtie2-2.1.0**  
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
**wget http://ccb.jhu.edu/software/tophat/downloads/tophat-2.0.3.0.Linux_x86_64.tar.gz**  
**tar zxvf tophat-2.0.3.0.Linux_x86_64.tar.gz**  
**cd ~/usr/local/bin**  
**ln –s ~/tophat-2.0.3.0.Linux_x86_64/tophat2 .**  

**_Cufflinks (version 2.2.1)_**  
http://cole-trapnell-lab.github.io/cufflinks/manual/  
**wget http://cole-trapnell-lab.github.io/cufflinks/assets/downloads/cufflinks-2.2.1.Linux_x86_64.tar.gz**  
**tar zxvf  cufflinks-2.2.1.Linux_x86_64.tar.gz**  
**cd cufflinks-2.2.1.Linux_x86_64**  
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
ggplot2: https://cran.r-project.org/web/packages/ggplot2/ggplot2.pdf  
**install.packages(“ggplot2”)**  
**install.packages(“grid”)**  
**install.packages(“gridExtra”)**  

Plyr: https://cran.r-project.org/web/packages/plyr/plyr.pdf  
**install.packages(“plyr”)**  

Reshape: https://cran.r-project.org/web/packages/reshape/reshape.pdf  
**install.packages(“reshape”)**  

CummRbund: http://bioconductor.org/packages/release/bioc/html/cummeRbund.html  
Requirement: Bioconductor release 3.2  
**source("https://bioconductor.org/biocLite.R")**  
**biocLite("cummeRbund")**  








## References


