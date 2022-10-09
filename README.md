# RNASeq Pipeline

Welcome to mamakf/rnaseq pipeline!

* You can create FPKM files from paired-end fastq files with this pipeline container.  
* How it works?:  
  * This container using Subread align for creating bam files from paired-end fastq files. After getting a bam files, create FPKM values of each sample with Rsubread featurecounts function and saves in a tsv file.

* Commands to download the RNASeq Pipeline image:  
```bash
docker pull mamakf/rnaseq
```
 

For running:  
```bash
docker run -it -v (your_project_folder_pathway):/mamakf/volume -v (your_indexes_ folder_pathway):/mamakf/volume/indexes mamakf/rnaseq
```

* Your project folder should contain the folder named "Fastq" which contains raw matched fastq files and "rnaseq_parameters.txt"

* What is "rnaseq_parameters.txt"?:  
  * This text file contains your subread align and rsubread featurecounts parameters. If you don't have this text file, don't worry, you can create own parameters with RNASeq pipeline, program will save your parameters in your Fastq folder so you can use them at other times.
