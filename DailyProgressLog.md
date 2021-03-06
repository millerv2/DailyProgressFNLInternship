# Daily Progress 6/17/21

## Github
Today, I signed up for a Github account and looked at several tutorials on Youtube to familiarize myself with its workings, learning Git commands like clone, add, commit, push, and pull.
l
Two really good guides that I found are here for reference:

https://www.youtube.com/watch?v=iv8rSLsi1xo

https://www.youtube.com/watch?v=RGOj5yH7evk

I learned how to link up Visual Studio Code, the Github desktop version and Github in the browser. I created a sample repository and wrote this md file in VSC and then added and commmited the changes on my local device and pushed them to the repository on Github.
test

## Oxford Nanopore Website Exploration:
Spent some more time on the Oxford Nanopore tech website, looking at the different sequencing machines, as well as some of the associated publications and documentation. 

### Some publications I looked at today:

#### Reviews:

https://iopscience.iop.org/article/10.1088/0957-4484/26/7/074003/pdf

https://onlinelibrary.wiley.com/doi/epdf/10.1111/dgd.12608

#### Primary Research Papers:

https://www.nature.com/articles/nbt0412-295

https://academic.oup.com/gigascience/article/8/8/giz104/5552683?login=true

https://www.nature.com/articles/sdata2018266

Today I also registered for an account on the NCI's High performance computing cluster, Biowulf, and completed several different logistic/training tasks related to onboarding.

# Daily Progress 6/21/21

## Literature Reading

I continued to look over some of the ONT research papers from last week and also found a few more papers of interest:

https://www.frontiersin.org/articles/10.3389/fgene.2020.00606/full

https://link.springer.com/protocol/10.1007%2F978-1-4939-7834-2_6

https://pubmed.ncbi.nlm.nih.gov/31740818/


## Biowulf HPC Set-up and Tutorial
Over the weekend my Biowulf account was approved with username millerv2 and my password being the same as my NIH password. To familiarize myself with Biowulf, I worked through the introductory course here: 
https://hpc.nih.gov/training/intro_biowulf/ 

I completed the Linux/Bash familiarity quiz and scored a 9/10, I may want to check out some of the Linux tutorials here: 

https://hpc.nih.gov/training/index.php#linux_tutorials

Information about the HPC systems at the NIH:
https://hpc.nih.gov

I worked through most of the introductory Biowulf lectures on the hpc.nih page and successfully logged onto Biowulf login node. I also wrote a sample shell script and submitted the job for execution on a compute node, and tracked its progress with squeue -u millerv2. It successfuly ran.

# Daily Progress 6/22/21

## Literature Reading
I continued to read up more on Oxford Nanopore Technologies applications in transcriptomics work, and found some interesting papers:

https://pubmed.ncbi.nlm.nih.gov/30949200/

https://pubmed.ncbi.nlm.nih.gov/31439691/

https://pubmed.ncbi.nlm.nih.gov/29334379/

https://pubmed.ncbi.nlm.nih.gov/32536962/

## Biowulf
I went through the remainder of the Biowulf tutorials on the hpc.nih webpage and also checked out a few of the Linux tutorials. 

## Github Transciptomics Pipeline Documentation Review
Today I also read through most of the pipeliner documentation here and began to look at the demos and run through them as practice:

https://ccbr.github.io/pipeliner-docs/RNA-seq/Theory-and-practical-guide-for-RNA-seq/

## Snakemake

I visited the Snakemake website and went through some of the documentation, and read through the referenced paper here:

https://f1000research.com/articles/10-33/v1

I also checked out a few Youtube video tutorials on Snakemake. Some were more helpful than others as introductions. Some good ones I found are here:

https://www.youtube.com/watch?v=NNPBDOBHlxo

https://www.youtube.com/watch?v=AZSJKNvkRcg

Tomorrow I plan on going through the Snakemake tutorial on the Snakemake website and also taking a look at the Snakemake files on the RNA-seq repo.

# Daily Progress 6/23

## Snakemake

Today I dedicated most of my time to learning Snakemake a bit more as well as kept up with some of my literature reading. 

I looked at the following Snakemake tutorials:

https://www.youtube.com/watch?v=hPrXcUUp70Y

https://www.youtube.com/watch?v=_wUGzqEjg6A *

I also read through some of the documentation oon the website here:

https://snakemake.readthedocs.io/en/latest/snakefiles/rules.html

I also ran through the complete Snakmake tutorial/guide on the website here:
https://snakemake.readthedocs.io/en/stable/tutorial/tutorial.html


# Daily Progress 6/25

This morning I continued to look through and try to understand all the working parts of the 4USeq repository here:

https://github.com/RBL-NCI/4SUseq

I also had a very helpful introductory session with Skyler to help me get further acquainted with Snakemake and how he utilizes it in his work. He helped orient me to the various directories, files, and working parts of his repository here: 

https://github.com/CCBR/RNA-seek

We talked about how it might be a good idea to use this as some sort of template for a simple Snakemake pipeline I develop, maybe with just a QC and trimming step for ONT RNA-seq reads.

# Daily Progress 6/28/21

## Review
This morning I figured it would be prudent to start off the week by just reviewing some of what I've been learning the past week and a half, from how ONT sequencers work and how the data is processed, to the workings of Github, the Biowulf HPC, and Snakemake. I've been keeping a notebook each day on what I've been learning so I've just reviewed this over to tie up any loose ends. 

## Snakemake
As part of this review I ran through the Snakemake tutorial on their website once again here: 

https://snakemake.readthedocs.io/en/stable/tutorial/basics.html

I also went through the Snakemake tutorial for Biowulf on the nih.hpc website here:

https://hpc.nih.gov/apps/snakemake.html

I then spent a good bit of time looking at the repo Skyler showed me last week to understand all its working parts:

https://github.com/CCBR/RNA-seek/blob/main/workflow/Snakefile
 
# Daily Progress 6/29/21

Good video reviewing VS code and Github connectivity:
https://www.youtube.com/watch?v=Fk12ELJ9Bww

Spent a lot time looking through these Snakemake workflows:



# Daily Progress 6/30/21

## Meeting Review:
 
 To transfer files from current directory to home directory on cluster use:
 $ scp <file> helix.nih.gov:~/

 Can also use $ scp -r <directory> helix.nih.gov:~/ to transfer a directory.

 ## Running Snakemake on Cluster.

 1) Sign in, and load snakemake (module load Snakemake)
 2) Instead of creating + activating an environment in Conda using a .yaml file with the conda directive and using --use-Conda when we run Snakemake, we specify modules directly for each rule with an envmodules directive in the rule like this which specifies the version for use:
 
    envmodules:
        "fastqc/0.11.9"

3) Then, to run the workflow, we run snakemake --cores 1 --use-envmodules
4) What if some rules of the workflow require Conda use (not pre-installed on Cluster) and some can use modules?

## Steps Going Forward:

We discussed the overall vision for this internship which is to reproduce the following workflow using Snakemake:

https://github.com/nf-core/nanoseq/blob/master/README.md

The paper describing the workflow and background is here: 

https://www.biorxiv.org/content/10.1101/2021.04.21.440736v1.full.pdf

The next few steps are to add trimming and second fastqc rules to my sample Snakemake workflow and run it on the cluster, then download some data from the nanoseq github repo and start experimenting with Nanoplot.

# Daily Progress 7/1/21
 
 ## Sample Snakemake Workflow

 I continued to write a simple Snakemake workflow that runs QC with FastQC on raw fq data, trims/filters the reads with cutadapt, and then re-reruns FastQC on the trimmed fastq files.  I took a look at the Cutadapt documentation here before writing my trim rule in the Snakefile:

 https://cutadapt.readthedocs.io/en/stable/guide.html

 I then wrote another rule to perform fastQC a second time on the trimmed reads and compared the html reports. It looks like trimming the reads helped to address several quality concern issues.

 I went over this simple workflow briefly with Skyler. The workflow is on Github here:

https://github.com/millerv2/SimpleSnakemakeWorkflow/blob/main/snakemake-tutorial/

And the Snakefile is here:

https://github.com/millerv2/SimpleSnakemakeWorkflow/blob/main/snakemake-tutorial/snakefile

The workflow ran successfully on an interactive node and I pushed the output folders with the output files to github so they are there as well in their specified directories.

I foresee that in the next workflow I plan on running that some of the programs/tools I'll need are pre-installed on Biowulf and some of them are not and will require me to use conda to create + activate environments with the proper packages. For reference, the packages that the Bioconda channel has are here:

https://bioconda.github.io/conda-package_index.html

I spent some time looking at the nano seq workflow here:

https://github.com/nf-core/nanoseq/blob/master/README.md

# Daily Progress 7/2/21

It looks like the authors already performed the basecalling and/or demultiplexing step, so I went right ahead and downloaded a few of the fq files from the Singapore Nanopore Expression project here:

https://github.com/GoekeLab/sg-nex-data

To start off, I downloaded fq files for PCR-cDNA sequencing, direct cDNA sequencing, and direct native RNA sequencing for lung cancer cell line (A549) samples here:

https://github.com/GoekeLab/sg-nex-data

For each of these sequencing techniques I downloaded at least 3 replicates, and placed all these .fq files in a directory on my Desktop called A549samples. 

I then transferred this directory with all these files to the cluster using scp with recursion:

$ scp -r A549samples/ helix.nih.gov:/data/$USER/samples

See here for review on transferring data to/from the cluster: 

https://hpc.nih.gov/docs/transfer.html

This transfer took several hours, but I then created a subdirectory in user/data called A549samples and moved all the lung samples into there.

# Daily Progress 7/6/21

This morning I spent sometime reviewing the documentation for Nanoplot, a plotting tool for long read sequencing data, on the README page here: 

https://github.com/wdecoster/NanoPlot

Nanoplot takes as input long-read fq files (can be compressed) and produces a statistical summary, number of plots, and an html summary file.

To first exploring this tool, I did it locally by creating and activating a Conda environment that loaded 
in Nanoplot 1.38.

I then ran the following Nanoplot command on the command line:

$ Nanoplot -o summary-plots-log-transformed --fastq /Users/millerv2/Desktop/A549samples/SGNex_A549_directcDNA_replicate1_run3.fastq.gz /Users/millerv2/Desktop/A549samples/SGNex_A549_directcDNA_replicate2_run1.fastq.gz

The results written to the output directory summary-plots-log-transformed included several different plots and summaries for sequencing quality control.

For the next step of this workflow I did FastQC on the raw reads using FastQC.  I already wrote a Snakemake rule for FastQC in my sample workflow so I took this framework and modified it slightly for the A549 sample data sets. I also plan on adding a rule for Nanoplot now above the FastQC rule now that I understood what the output looked like.  

# Daily Progress 7/7/21

This morning I continued working on the Nanoseq workflow in Snakemake, but initially had some trouble linking up the directory on the cluster with the remote Github repo. 

After some troubleshooting and help from Vishal, everything is connected up. The directory /data/millerv2/NanoseqSnakemake which can be reached from the login node contains the snakefile and any env/config files, while the samples are in a separate directory here: /data/millerv2/samples. I will also need to make separate folders for the output results. To set up all these specific directories it may be helpful to make a congif yaml file down the line like the one here:

https://github.com/kopardev/CCBR_ATACseq/blob/master/config/config.yaml

The full Github repo here for the ATACseq Snakemake workflow is a good resource to reference:

https://github.com/kopardev/CCBR_ATACseq

A few tidbits from the meeting with Vishal:

- Down the line include config .yaml file to specify all the directories for the workflow, I/O

- When running Snakemake workflow on interactive node you can request -90GB for FastQC, may not need end up needing all that memory 

Tomorrow I plan on making sure I can get the first few steps of the workflow running, FastQC, and Nanoplot.

# Daily Progress 7/9/21

Today I got the Snakemake workflow successfully running FastQC and Nanoplot successfully.

I met with Skyler and he helped me decide that for rules in the workflow where the executed program is not pre-installed on the cluster, the best strategy is to run that job in a docker/singularity container that you define. Then, you can just run the workflow with --use-singularity in addition to --use-envmodules.

For the Nanoplot rule, since it wasn't available on the cluster, I defined the following docker under the container directive (from Skyler):

container:
        "docker://staphb/nanoplot:1.33.0"

Then, I ran the workflow as follows:
$ module load snakemake/6.5.3
$ module load singularity/3.8.0

$ snakemake --cores 1 --use-envmodules --use-singularity --singularity-args '-B /data/millerv2'

Can use $ history | grep 'snakemake' to look back at previous snakemake commands you've run.

# Daily Progress 7/19/21

Today I created a .gitignore file for my workflow which specifies files or directories that should be intentionally ignored/untracked by Git. I put the .snakemake/ directory in here so that I don't unintentionally push any snakemake logs or singularity image (.simg) files to Github like I was previously. Can update this file as I go to include any files/directories that I don't care about tracking or pushing. Note, this is another hidden directory like .git, so will need to use $ ls -la to see and edit it.

I then pushed all my changes to github. My repo now has the working snakefile which successfully runs FastQC and Nanoplot on input fq files, and the next step was to run some sort of trimming/filtering on the ONT reads using a trimmer program designed for Oxford Nanopore reads. The original candidate, Porechop, seems like it was unsupported and is now abandonware, as stated on the Readme here:

https://github.com/rrwick/Porechop#readme

As an alternative, we decided on using Nanofilt to remove short reads and the first 10 bases from all reads as they tend to be the most error-prone. Adapter trimming of long reads such as those output by Oxford Nanopore sequencers is not as important as for short read technologies because the adapters represent a much smaller relative proportion of the long reads (< 10% of the total read length (unlike illumina)). 

Documentation here:
https://github.com/wdecoster/nanofilt

# Daily Progress 7/20/21

Today I finetuned a lot of my workflow, removed a lot of things that were previously hard-coded by linking up the config.yaml file. I also changed the structure of my workflow to match the cookie-cutter/recommend structure of a Snakemake workflow described here:

https://github.com/snakemake-workflows/snakemake-workflow-template

Right now, the workflow works for 4 rules, and the paths to the output directories and working directories can be specified in the config file so that someone can run it on their local file system.  I pushed these changes to Github and they can be viewed there.


# Daily Progress 7/21/21

Today I finetuned my workflow further for the first htree rules, making various parameters that we're previously harccoded customizable in the key-value pairs of the config file. I also added log and message directives to all my rules as recommend after running $ snakemake --lint. 

I also added params directives to rules within which I specified various output directories for those rules and then referenced those directories in the shell directive using {params.OUT_DIR}. I also redirected standard output and error the log file for rules as in the following example here:
shell:
        "fastqc -o {params.OUT_DIR} {input} &> {log} "

Within other rules I also took parameters that were previously hard-coded and exposed them - ie made them readable/customizable from the config file - and then defined them in the params directive so they could be used in the shell commands. For example:

params:
        OUT_DIR = os.path.join(base_dir,"trimmed_reads"),
        headcrop = config['headcrop'],
        length = config['length']

shell:'''
NanoFilt -l {params.length} --headcrop {params.headcrop} < {input} > {params.OUT_DIR}/{wildcards.sample}.fastq
''' 

This way, if someone else wants to run Nanofilt with different parameters, they can specify them in the config file rather than here, allowing more customizability/reproducability.

# Daily Progress 7/22/21

Today I added a fastqc_trimmed rule which takes the output files produced by Nanofilt (which filters out low quality/short reads) and performs fastqc on these trimmed reads. I then compared the fastqc quality reports produced on the raw/unfiltered reads to these reports on the filtered reads to see if several different quality concerns were addressed.

I then began to write a rule for the actual read alignment to the reference genome, using minimap2.  This program is ideal for read alignment for longer reads produced by third generation sequencers as it can be fine-tuned to use particular seeds for the alignment that optimize performance and sensitivity. The parameters/commands to do so are described here in the 'Use Cases' section:

https://github.com/lh3/minimap2

For direct RNA seq as is the case for the two test samples I've been using, the following command is described:

$ minimap2 -ax splice -uf -k14 ref.fa direct-rna.fq > aln.sam 

My minimap2 rule runs sucessfully but it takes over an hour to run. As of right now I've just been running Snakemake on the command line on an interactive node but going forward now that I'm performing some more computationally intensive jobs I should develop a cluster.json file with keys for the jobs and values for the resources to be allocated.

Now that I've got several rules in my snakemake file I'm planning on modularizing it - ie putting certain rules in their own snakemake (.smk) files - and referencing them with include statements at the top of the snakefile.  I plan on doing this tomorrow along with setting up the cluster.json file.

# Daily Progress 7/23/21

Today I modularized the workflow further by adding additional snakemake (.smk) files, one containing quality control rules called qc.smk, and one containing alignment rules called align.smk.  I may add one for read trimming/filtering as well, but for now this will suffice to keep the main Snakefile from being to lengthy now that the rule all has quite a few output files. 

I also had a few more key value pairs to my config file, such as a genome key so that a user could specify the genome they'd like to use for the read alignment step using Minimap2.  Right now there is the most update to date human and mouse genomes in a directory in my /data/millerv2 directory and the values in the key value pair in config is set to the path to those files.  

Seeing that the alignment step is fairly computationally intensive and took a long time to run just via the command line on an interactive node, so next step is to set up the cluster.json file which has keys for the jobs and the values for the resources to be allocated.


# Daily Progress 7/26/21

Today I took a step back and did a bit of a review day, looking over my daily progress log, my notebook, and snakemake workflow so far, as well as doing a bit more literature reading on Oxford Nanopore technologies and the data processing workflows that are optimized for their long read data outputs. I'm trying to figure out if there are any workflow steps or parameters that are missing from the Nanoseq NextFlow workflow that we can use enhance the workflow and differentiate it a bit.

# Daily Progress 7/27/21

This morning I took the time to review this Linux introduction here:

https://hpc.nih.gov/training/handouts/Introduction_to_Linux.pdf

I've been using Linux/the command line for a while now but there are still some commands and features I'm not fully acquanted with, so I thought this review would be worthwhile.

I also managed to set up my cluster.json file which specifies the resources that should be allocated for each rule, as well as default resources to be allocated if a rule does not have a key in the json file. With Skyler's help, I wrote a bash script that submits the snakemake workflow for submission on the cluster called run.sh. This script makes a new script with all the proper paramters and inputs. I submitted the job and it is currently pending/waiting in queue.

# Daily Progress 7/28/21

Today with Vishal's help we updated the run.sh file which we're using to submit the Master job to the cluster which then submits the different rules as their own child jobs. More specifically, along with a WORKDIR variable that the user can specify when running the script, they can also specify as RUNMODE as a second parameter, and can run the pipeline as dryrun, unlock, or cluster.  

Now, to dry-run the pipeline we can run:

$ ./run.sh /data/millerv2 dryrun

./ calls and runs an executable that is in your $PATH. Remember on Linux/Unix,nearly any file can be executable, the file ending just must describe what or how the file is "excecuted".

Initially this wasn't running properly because I had to update the variable samples in the config file to specify a full path to the samples.tsv file for it to find it.

Another change we made to make testing of the pipeline more effective is creating two dummy.fastq.gz files which are subsets of the first 1000 reads (4000 lines) from the original fastq files in the samples directory. I modified the table (samples.tsv) to contain the names of these dummy fastq files which we will use for running.  

Today I'm going to actually try to run the complete job, ie run the pipeline with the following command:

$ ./run.sh /data/millerv2 cluster

Can check on the jobs with $sjobs, $data job ID, $squeue -u millerv2, jobload, jobhist. The page and video here are a good review on monitoring jobs submitted to the cluster.

Before the jobs runs, should check disk space using:

After the jobs runs, should log CPU utilization, memory utilization, and wlal time. This will give you an idea of how many resources to be allocated for a particular job/rule in the workflow.

First time submitting a job you may need to request ample resources, but then after running it can check CPUs, memory, walltime and adjust as needed for future jobs.

# Daily Progress 7/29/21

Tools for monitoring Biowulf jobs:
1) Before running/submitting, checkquota for disk space
2) Look at .o and .e files from jobs for trouble-shooting.
3) sjobs, squeue show status of jobs
4) jobload -u shows CPU and mem usage for your jobs. can use jobload -j job_id to look at this info for a particular job.
5) Jobhist job_id shows utilization after jobs ends for that job
6) Dashboard on nih website

I met with Skyler to help with submitting the job to the cluster successfully. A few things we changed that are worth noting:
1) Nanofilt, a read trimming/filtering program we are using, requires the fastq files to be unzipped to run. In the filter rule, I added two pipes to the command, one after a gunzip which unzips in the input.fastq.gz files and then a gzip at the end to zip them back up after trimming/filtering.
2) We created a new subdirectory called .tests which is in the NanoseqSnakemake directory and contains the small .fastq files to be used for testing. This samples directory was added as a variable in the config file called samples_dir and was added to the paths in our different rules so that we could point to those files. I also changed the corresponding sample names in the samples.tsv file in config.
3) We also modified the run.sh file which we use to submit the workflow for execution.  The submission command now takes three arguments: runmode($1), workdir($2), and inputdir($3). Runmode specifies whether to dry run or actually submit the master job to the cluster for execution of it and all its child jobs, the workdir is the path to the output directory, and the inpudir should be the path to the folder containing the input fastq files, in .gz format.

The actual commands I ran to submit the workflow for dryrun, and for execution are:
$ ./run.sh dryrun /data/millerv2 /data/millerv2/NanoseqSnakemake/.tests
$ ./run.sh cluster /data/millerv2 /data/millerv2/NanoseqSnakemake/.tests

The workflow ran successfully using these commands. When submitted to the cluster for execution, the workflow ran in 18 minutes, 21 seconds. Taking a closer look at the user dashboard on hpc.nih.gov I took the jobids for the sub jobs and ran jobhist job_id commands to get a sense of how much memory/time different sub-jobs/rules took to run on the cluster so that I could adjust their resource allocations going forward.

FastQC_raw took only around 20 seconds to run and used very little memory. Same for FastQC_trimmed rules. Same for Nanofilt.

Nanofilt, job id 20233596, took 36 seconds to run, and used .4GB of the allotted 24GB/node.

Minimap used 19.4GB memory, and took 2 mins 15 seconds to run with 32 CPUs allocated but only 2 used for job_id 20234442. For the other minimap job_id 20234434, it used 19.1GB memory and took 2 mins 5 seconds to run with max only 2 of allocated 32 CPUs being used.

The caveat when looking at this resource usage for different rules is that we only used two .fastq files as test input, and they were very small .fastq files - only a couple thousand reads long.  

# Daily Progress 7/30/21 

As of today, I have a properly functioning Oxford Nanopore RNA-seq data processing workflow, with an initial raw read Fastqc quality check step, a plotting QC step (Nanoplot), a trimming/filtering step, an additional Fastqc quality check on the trimmed/filtered reads, and a genome alignment step with Minimap2.  The workflow has several working parts so I figured it would make sense to make sure I understand what each file is doing and where everything is.

The directory that is linked up the remote repo on Github is NanoseqSnakemake. In here, there are several subdirectories. The config subdirectory contains a config yaml file which defines everything to configure th workflow on a global scale. In here there is a path to a table containing the samples in .tsv format, a path to a base_dir which will be the output directory for various rule outputs, and a sample_dir varaible which defines the path to the samples used as input. I also have variables/ key-value paris for different parameters for certain rules and a path to a genome used in the alignment step.

In another folder called Resources, it contains resources necessary for running workflow. The cluster.json file here has key value pairs for different rules and the number of resources (memory, time, threads, etc) that should be allocated for that rule when it is submitted as sub/child job for execution on the cluster.

In the workflow directory there is the actual Snakefile and various other .smk files which contain different rules in the rules directory, which are called in the main Snakefile using the include directive. At the top of the Snakefile we define different variables such as the sample directory and the base_dir by accessing those values from the config file where we defined them as key/value pairs. How does th e snakefile know what config is? Where do we define this? Maybe built-in global variable config to snakemake? Yes, but we're just using the --configfile option in the run.sh when actually running Snakemake to provide it with the path to the config file.

The main Snakefile here just contains the rule all, which specifies all the outputs we want to obtain from our various rules. note that if a particular program produces many output files, we should specify all of them in the output directive for that particular rule... but in the rule all we only have to specify the output file that is produced last (most recently) to obtain all of those outputs.
 
The run.sh file is the executable that submits the Snakefile job for execution either dryrun or on the cluster. It contains information about submitting the job to SLURM (#SBATCH parameters) and also the actual Snakemake commands, including the specification of the general configfile and the cluster config file. Upon execution this file creates and submits the batch script called submit.sh.

Today I added a sam_to_sorted_bam rule to my rules/align.smk file which employs Samtools to take the minimap output (.sam alignment file) and convert it to .bam format as well as sort it by coordinates. I also requested various mapping metrics using Samtools to get a summary of the mapping.  I dry-ran and then submitted the workflow and it ran successfully.

Now that the genome alignments for the samples were in proper sorted bam format, the next step is to use these bam files for bigWig and bigBed coverage tracks for visualization. I haven't used either of these programs before so I spent the rest of the afternoon looking over the documentation here and going through some featured tutorials:

https://bedtools.readthedocs.io/en/latest/

# Daily Progress 8/2/21

This morning I reviewed the bedtools documentation and worked on writing a rule for producing coverage tracks for visualization. 

I reviewed the various different file formats that we are using for this rule, including BAM, bed, and bigBED, and what programs/commands are needed to convert between them.

http://genome.ucsc.edu/FAQ/FAQformat.html#format1

First, I had to write a rule using bedtools to go from .BAM format, the compressed binary version of sequence alignment map (.SAM) format output by minimap2, to .bed format. Bed, or browser extensible format, provides a way of defining data lines to be displayed/visualized in an annotation track. It requires three fields, chrom, chromstart, and chromend, and several other optional fields. To convert the bam files to bed, I used bedtools and wrote a rule called bedtools_bam_to_bed in the bedtools.smk file in workflow/rules.

Next, I had to convert the bed files to bigBed format, using the program bedtoBigBed from the ucsc utilities module. BigBed files are also indexed binary format but only protions of th efiles are needed to display a particular region for visualization, so that are faster than regular bed files. The rule bedtobig bed in workflow/rules/bedtools.smk converts the bed files to bigBed format after sorting the bed files. 

For the genome to which the track will be referenced, you need to extract chromosomze sizes and provide this information when converting to bigBed format. I used a samtools command below to extract the chromosomze sizes and put the output in a file chrom.sizes:
$ samtools faidx {input.ref}
$ cut -f1,2 {input.ref}.fai > {output}

This rule is called samtools_get_chrom_sizes and it's located in workflow/rules/align.smk.

I successfully dry-ran and then ran the workflow on the cluster with these added rules. The workflow now produces proper BigBed coverage tracks for visualization, but in the next step tomorrow I'll work on producing bigWig tracks as well.


# Daily Progress 8/3/21

This morning I added rules for going from bam files to bedgraph files, and then from bedgraph to bigWig tracks for visualization. I dryran and then submitted the workflow for execution on the cluster and it ran successfully.

The next step of the workflow is transcript reconstruction and quantification, the first step of what can be considered RNA-specific downstream analysis. The Nanoseq pipeline uses bambu, an R package, to reconstruct and quantify transcripts in a single run, and Stringtie, which produces individual transcript assemblies for each sample and then merges them together to get a more comprehensive transcript profile. 

I began with Stringtie2 by writing an sample_transcript_assembly rule. 

Downloading genome:

wget http://ngi-igenomes.s3.amazonaws.com/igenomes/Homo_sapiens/NCBI/GRCh38/Annotation/Genes/genes.gtf

Downloading reference .gtf annotation:

wget http://ngi-igenomes.s3.amazonaws.com/igenomes/Homo_sapiens/NCBI/GRCh38/Sequence/WholeGenomeFasta/genome.fa



# Daily Progress 8/4/21

This morning I met with Vishal to make an overall gameplan for the next few weeks in terms of meeting major milestones. By the end of this week I want to have the first iteration of the workflow done, start to finish. This means having the gene/transcript assembly with Stringtie done, the gene and transcript quantification producing count matrices with featureCounts, differential expression with DeSeq2, and final QC with MultiQC.

I first wrote the rule for Stringtie individual transcript assembly, then a rule for merging their assemblies, and a final rule to run Stringtie again using the merged.gtf file as the reference transcriptome.

I then looked at the FeatureCounts documentation here:

http://bioinf.wehi.edu.au/featureCounts/

https://manpages.debian.org/testing/subread/featureCounts.1.en.html

Using this as a guide, I wrote a FeatureCounts rule in the transcript_quant.smk snakemake file to produce counts_gene.txt and counts_transcript.txt files which are count matrices for genes and transcripts.

The next step is to perform MultiQC as the end of the workflow.

After finishing the MultiQC step, Vishal and I discussed providing the user the utility to select the specific type of long read sequencing technology (eg direct RNA, cDNA, etc), as a result running different parameters for each program that are tailored to that technology. Downstream we could then running PCA or other unsupervised methods to see if gene expression is more related by read technology or tissue of origin.

# Daily Progress 8/5/21

I began this morning by reviewing the MultiQC docs here:

https://multiqc.info/docs/

I wrote and executed a Multiqc rule in the multiqc.smk snakemake file. I might move this rule to the qc.smk file where I have fastqc and Nanoplot. I included as input all the outputs from the previous rules just to ensure Multiqc runs last and provides reports for all the relevant output files.  

I dryran and then cluster-submitted the workflow and it ran successfully, taking about 30 minutes to run. The multiqc step takes the longest to run, taking about 16 minutes.

Now that I've got every part of the workflow set up except for differential expression analysis, I worked on adding a feature to the workflow where based on the type of sequencing technology (eg directRNA vs cDNA) for the sample, different commands will run for different programs. I started with minimap2.

First, in my samples.tsv table, I added a column called application, which specifies the type of sequencing technology used (directRNA vs cDNA). So this table now had a sample name column, and a sequencing type column. Next, in the config file I added a key called minimap_options and nested two keys within it, one for directRNA and one for cDNA, and the values for these keys were different parameters/options for minimap2. Then, I had to find a way for the rule to extract this information from the samples table and feed it to the shell command. To do this I added a params directive to the minimap rule and used a lambda function to select the application type corresponding to the input sample for the rule, and then search up the settings value for that application type in the config file. Then I call params.options in the shell itself. I dryran and cluster-submitted the workflow and it ran successfully.

The next step is to add a differential expression analysis rule using DESeq2.  DESeq2 is an R package, so I'll have to include a script directive in my rule which loads and executes DESeq2 commands and then have an envmodules directive to load in R to my environment.  The script used in the nextflow workflow is in the bin folder and is called run_deseq2.r.  Before really diving into understanding this script I took a look at the DESeq2 documentation here and will spend some more time with it tomorrow:

http://127.0.0.1:15080/library/DESeq2/doc/DESeq2.html

# Daily Progress 8/6/21

Reviewing the DESeq2 documentation, this program takes as input count data such as that produced by FeatureCounts, which contains genes in the rows, samples in the columns, and assignment or counts values in the cells. An important next step in the analysis is the statistical inference of differences between conditions, as compared to in condition variability between replicates. This package provides methods to test for differential expression by use of negative binomial generalized linear models; the estimates of dispersion and logarithmic fold changes incorporate data-driven prior distributions.

The section about input as count matrices here is particulary useful and walks through an example:

http://127.0.0.1:15080/library/DESeq2/doc/DESeq2.html#countmat

The object class used by the DESeq2 package to store the read counts and the intermediate estimated quantities during statistical analysis is the DESeqDataSet. This data set and its contained information can then be used to run statistical tests. The design formula specifies the variables which will be used in the statistical modeling. For me, this would be either treatment, disease vs control, or tissue type.

I spent a while working with the R script from nextflow's workflow for running DESeq and modified it to read in my data and run DESeq with it. I'll continue working on this over the weekend and next week to have my workflow done for its first iteration from read mapping to differential expression analysis.

# Daily Progress 8/9/21

Most of this morning I spent experimenting with the runDESeq R script to adapt it to successfully read in my counts matrix and samples table into a DESeq dataset which could then be used for douwnstream analysis / statistical tests.  I was getting an checkForExperimentalReplicates(object, modelMatrix) error because I only had two sample files and they were both in the same group. I decided to create two more dummy/test files test3.fq.gz and test4.fq.gz and added them to the samples.tsv file in the config.  To make these files I simply took the first 2000 lines from each of the other sample files using:

$ head -n 2000 test1.fastq > test3.fastq
$ head -n 2000 test2.fastq > test4.fastq

I then dryran and cluster-submitted the workflow with these new sample files being taken as input. It worked properly.

I then reran the DESeq2 R-script now that I had two treatments and two replicates and it ran successfully - ie I was able to create a DESeq data set and write the results to an output file.

# Daily Progress 8/11/21
Today I worked on adding a DESeq2 rule which called the R script to accept specified and output the DESeq data set results. I had to modify a few things in the R script to have it properly function within the rule but it now works and takes two command line arguments in the shell directive of the rule, the path to the gene counts, and the path to the sample information table.

# Daily Progress 8/12/21-8/13/21
Today I added a data viz rule to the Snakemake workflow which employs an R script to produce a PCA plot, a sample distance heatmap, and a gene heatmap of the 50 most variable genes across the samples.  To do so, I used the following R packages: DESeq2, pheatmap, genefilter. The script is called pca_and_heatmaps.R and is called in the scripts directive, taking as standard input the path to the gene counts matrix, the path to the samples table, and the output directory path.

After a lot of experimentation and tweaking with the rule, it now works and outputs a PCA plot, a sample heatmap, and a gene heatmap for the 50 genes whose expression varies the most between the samples.  

# Daily Progress 8/14/21
Today I met with Skyler to take a look at the workflow in its current state and discuss plans going forward to improve its completeness, now that it runs from read qc to differential expression analysis and the foundation is paved. The next few steps are:

- Run the entire workflow with full-sized fastq inputs rather than dummy files. Record number of resources each job needed and update the cluster.json
- Assuming all goes well, go through the entire workflow start to end and examine each line of code to make sure there isn't any remaining functionality that is hard-coded. To double check this I can clone the git repository in /scratch and run it there.
- Another possible check for the validity of the workflow is to clone the Nextflow Nanoseq workflow and run it on the same inputs, and then compare the outputs with what I get running the workflow in Snakemake.
- If time permits, update the Snakemake dataviz rule that currently generates a PCA plot and heatmaps to make interactive plots using plotly. Skyler has a script that can be adapted.

I also took some time today to update the .readme page on the Github repo millerv2/NanoseqSnakemake to provide an overview of the workflow steps and also a section with overall instructions for running the workflow. 

# Daily Progresss 8/17/21

This morning I listened in on the Bioinformatics Project Discussion presentation by Shen about using Fastq screen tool for assessing bacterial contamination in DNA/RNA samples.  Instead of just mapping against a single (human) genome, when genome of origin requires confirmation mapping against multiple genomes is advisable for detecting contamination. Fastq screen works by quantifying the proportion of reads that map to a panel of reference genomes (eg mouse, bacterial, human). Interesting factor to consider that if overall sequence alignment is low perhaps some of the reads that arent mapping to human genome are of different species of origin. 









