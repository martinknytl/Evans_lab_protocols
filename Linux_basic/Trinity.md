How to run trinity
```bash
Trinity --seqType fq  --left /home/xue/borealis_transcriptome/borealis_denovo_transcriptome_oct2018/Trimmed/borealis_R1_paired.fastq.gz --right /home/xue/borealis_transcriptome/borealis_denovo_transcriptome_oct2018/Trimmed/borealis_R2_paired.fastq.gz --CPU 20 --full_cleanup --max_memory 200G --min_kmer_cov 2 --output /home/xue/borealis_transcriptome/borealis_denovo_transcriptome_oct2018/
```
Below is the explaination of what we included in the above command:
- --seqType <string>      :type of reads: ('fa' or 'fq')
- --left  <string>    :left reads, one or more file names (separated by commas, no spaces)
- --right <string>    :right reads, one or more file names (separated by commas, no spaces)
- --CPU <int>                     :number of CPUs to use, default: 2
-  --full_cleanup                  :only retain the Trinity fasta file (only the transcriptome file) and not the intermediate files (ex, file A, file B, and file C), rename as ${output_dir}.Trinity.fasta
- --max_memory <string>      :suggested max memory to use by Trinity where limiting can be enabled. (jellyfish, sorting, etc) provided in Gb of RAM, ie.  '--max_memory 10G'
- --min_kmer_cov <int>           :min count for K-mers to be assembled by Inchworm (default: 1)
- --output <string>               :name of directory for output (will be created if it doesn't already exist)

How to see the full usage
```
/home/xue/software/trinityrnaseq-Trinity-v2.4.0/Trinity --show_full_usage_info
```
