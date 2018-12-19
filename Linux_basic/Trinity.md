How to run trinity
```bash
time /home/xue/software/trinityrnaseq-Trinity-v2.4.0/Trinity --seqType fq  --left /home/xue/borealis_transcriptome/borealis_denovo_transcriptome_oct2018/Trimmed/borealis_R1_paired.fastq.gz --right /home/xue/borealis_transcriptome/borealis_denovo_transcriptome_oct2018/Trimmed/borealis_R2_paired.fastq.gz --CPU 20 --full_cleanup --max_memory 200G --min_kmer_cov 2 --output /home/xue/borealis_transcriptome/borealis_denovo_transcriptome_oct2018/; echo "trinity is done at info114 in screen assembly" | mail songxy2@mcmaster.ca
```

How to see the full usage
```
/home/xue/software/trinityrnaseq-Trinity-v2.4.0/Trinity --show_full_usage_info
```
