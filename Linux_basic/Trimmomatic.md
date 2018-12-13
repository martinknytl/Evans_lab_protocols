# Trimmomatic 

# Installing trimmomatic

This software is used to trim off bad sequences based on position in the read and quality scores of the nucleotides.  You can get it like this `wget http://www.usadellab.org/cms/uploads/supplementary/Trimmomatic/Trimmomatic-0.36.zip`

Uncompress it like this:
`unzip Trimmomatic-0.36.zip`

path to raw read file: 
```
/home/xue/diploid_tetraploid_transcriptome_QA/Laevis_TranscriptomeData/Sample_BenEvansBJE3909cDNA_Library
```
# what does trimmomatic does
This will perform the following:

- Remove adapters (ILLUMINACLIP:TruSeq3-PE.fa:2:30:10)
- Remove leading low quality or N bases (below quality 3) (LEADING:3)
- Remove trailing low quality or N bases (below quality 3) (TRAILING:3)
- Scan the read with a 4-base wide sliding window, cutting when the average quality per base drops below 15 (SLIDINGWINDOW:4:15)
- Drop reads below the 36 bases long (MINLEN:36)

##Run trimmomatic 
run it like this if it is paired end
learn how to run trimmomatic and what the command means: http://www.usadellab.org/cms/?page=trimmomatic

```
java -jar /home/xue/Trimmomatic-0.36/trimmomatic-0.36.jar PE -phred33 -trimlog trim_out.txt /home/xue/transcriptome_data/Sample_BenEvansBJE3909cDNA_Library/BenEvansBJE3909cDNA_Library_GTGAAA_L004_R1_001.fastq.gz /home/xue/transcriptome_data/Sample_BenEvansBJE3909cDNA_Library/BenEvansBJE3909cDNA_Library_GTGAAA_L004_R2_001.fastq.gz /home/xue/transcriptome_data/BJE3909_tropicalis_trimmed_data/BenEvansBJE3909cDNA_Library_GTGAAA_L004_R1_001_paired.fastq.gz /home/xue/transcriptome_data/BJE3909_tropicalis_trimmed_data/BenEvansBJE3909cDNA_Library_GTGAAA_L004_R1_001_single.fastq.gz /home/xue/transcriptome_data/BJE3909_tropicalis_trimmed_data/BenEvansBJE3909cDNA_Library_GTGAAA_L004_R2_001_paired.fastq.gz /home/xue/transcriptome_data/BJE3909_tropicalis_trimmed_data/BenEvansBJE3909cDNA_Library_GTGAAA_L004_R2_001_single.fastq.gz ILLUMINACLIP:/home/xue/Trimmomatic-0.36/adapters/TruSeq2-PE.fa:2:30:10 SLIDINGWINDOW:4:15 MINLEN:36
```
What the parameters mean:
- LLUMINACLIP: Cut adapter and other illumina-specific sequences from the read.
- SLIDINGWINDOW: Perform a sliding window trimming, cutting once the average quality within the window falls below a threshold.
- LEADING: Cut bases off the start of a read, if below a threshold quality
- TRAILING: Cut bases off the end of a read, if below a threshold quality
- CROP: Cut the read to a specified length
- HEADCROP: Cut the specified number of bases from the start of the read
- MINLEN: Drop the read if it is below a specified length
- TOPHRED33: Convert quality scores to Phred-33
- TOPHRED64: Convert quality scores to Phred-64
