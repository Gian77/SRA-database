### How to download files from the SRA archive using terminal

Install the `sra-tools` official module form the NCBI website. Using conda for this task it is easy.

```
conda search -c bioconda sra-tools
conda create -n sra -c bioconda sra-tools=2.11.0=pl5321ha49a11a_3
conda info --envs
```

Then we run the following:

```
conda activate
fastq-dump \
    --outdir /mnt/home/benucci/Genome_work/sra/ \
    --split-3 $ERR008613
conda deactivate
```

Then you have your files downloaded in the directory you have specified.

For more options about sra-tools see the link: <br>
* https://edwards.flinders.edu.au/fastq-dump/
