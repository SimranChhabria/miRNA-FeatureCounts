# miRNA-FeatureCounts
This is a python snakemake file which creates feature counts table for miRNA sequences combining cutadapt function and bowtie2 reference alignment.

# Currently Loaded Modules:
1) python/py37-anaconda-2019.10   2) snakemake/5.7.1-py37   3) gbc-cutadapt/2.10   4) gbc-bowtie2/2.4.1   5) subread/2.0.1

# Step-by-step analysis:

1) Activate the python anaconda-snakemake environment.
   conda activate snakemake
   
2) Edit the config.json file according to your data and file paths.

3) Ensure that meta-table contains all the necessary fields.

** NOTE EXACT HEADERS HAVE TO BE ENFORCED WITH ONLY ONE SPACE BETWEEN THE ENTERIES or key errors will be thrown during processing**

4) Try the dry run of the snakefile created to check any potential errors.
   snakemake -n -s Snakefile
  
5) Launch all the jobs.  

# Launching the jobs:
snakemake --latency-wait 120 -p -j 100 -s Snakefile

6) The pipeline will produce a countfinal.txt file containing all the details of the miRNA sequences required along with an output directory with all the trimmed and mapped reads.


  

   

