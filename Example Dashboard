### DNA-methylation-preprocessing

Suite of tools to conduct methylation data analysis. Methods from this workspace can be used for alignment and quality control analysis for various protocols including Whole Genom Bisulfite Sequencing (WGBS), Reduced Representation Bisulfite Sequencing (RRBS) and Hybrid Selection Bisulfite Sequencing (HSBS).

More information could be find in the github repo here: https://github.com/aryeelab/dna-methylation-tools

---

### Data

**Sample Data**  
All preprocessing methods require forward and reverse  fastq or fastq.gz files entered into the data participants table.  The tables below outline the format and content of the **Participant** data model tables (tab separated files with “tsv” extension).

   **Example 1:** Participants.tsv for RRBS and WGBS

| entity:participant_id 	| bs_fastq1                          	| bs_fastq2                          	|
|-----------------------	|------------------------------------	|------------------------------------	|
| Sample1               	| gs://location/sample_1_R1.fastq.gz 	| gs://location/sample_1_R2.fastq.gz 	|
| Sample2               	| gs://location/sample_2_R1.fastq.gz 	| gs://location/sample_2_R2.fastq.gz 	||

   **Example 2:** Participants.tsv for HSBS requires an additional input, the target_region.

| entity:participant_id 	| bs_fastq1                          	| bs_fastq2                          	| target_region                         	|
|-----------------------	|------------------------------------	|------------------------------------	|---------------------------------------	|
| Sample1               	| gs://location/sample_1_R1.fastq.gz 	| gs://location/sample_1_R2.fastq.gz 	| gs://location/hg38_targetCoverage.bed 	|
| Sample2               	| gs://location/sample_2_R1.fastq.gz 	| gs://location/sample_2_R2.fastq.gz 	| gs://location/hg38_targetCoverage.bed 	|


   **Example 3:** Participant_set_membership.tsv can be created from participant_id by creating a table in this format:

| membership:participant_set_id 	| participant 	|
|-------------------------------	|-------------	|
| Human_single_cell_Expt_1      	| Sample1     	|
| Human_single_cell_Expt_1      	| Sample2     	|


This workspace includes test sets to help you  become familiar with the workflows

| participant_set_id 	| participants 	| cell type                                             	|
|--------------------	|--------------	|-------------------------------------------------------	|
| HES                	| 3            	| Human single cell                                     	|
| HES_set2           	| 2            	| Human single cell                                     	|
| Human_wgbs         	| 1            	| Human whole genome                                    	|
| MES                	| 4            	| Mouse single cell                                     	|
| Mouse_wgbs         	| 1            	| Mouse whole genome                                    	|
| test_set_mouse_sc  	| 3            	| Small mouse single cell data set(for program testing) 	|

**Workspace Data**  
This workspace has no set attributes.  To change reference genomes and target regions,  you will need to modify the input json before running the program.

---

### Tools

This workspace contains the following preset method configurations, already set up for grch38, hg19 and mm10.  Other genomes can be loaded by changing the json inputs.  

* Preprocessing tools are run as "participant", selecting one sample or a set of samples.  
* The aggregation tool is run as a "participant set" on a set of preprocessed samples aligned to the same genome.  
* Aggregation can only be done after preprocessing.      
* Both preprocessing and aggregation generate html reports (see links to examples below).  

**Preprocessing:**

* bismark_wgbs: Preprocess Whole Genome Bisulfite Sequencing (WGBS) data
* bismark_rrbs: Preprocess Reduced Representation Bisulfite Sequencing (RRBS) data
* bismark_hsbs: Preprocess Hybrid Selection Bisulfite Sequencing (HSBS) data

[Example bismark processing report](https://storage.googleapis.com/terra-featured-workspaces/methylation-preprocessing/example_output/test_HES_sample_1_R1.fastq.gz_bismark_report.html)

**Aggregation:**

* aggregate_bismark_output: Aggregates outputs from preprocessing pipelines and produces an aggregated data structure for further downstream analysis

[Example output from scmeth R package](https://storage.googleapis.com/terra-featured-workspaces/methylation-preprocessing/example_output/qcReport.html)

Based on the reference genome different method configurations could be selected. So far, we have hg38, hg19 and mm10 reference genome versions of all preprocessing and aggregation tools.

---

### Example Time and Cost to Run Workflow

| Sample size |     Per-sample preprocessing |     Aggregation and QC | Total |
| :---:    | :---: | :---: | :---: |
|     | (Hours / $)                  | (Hours / $)            | (Hours / $)        |
| ..................................... | ............................................................................. | .......................................................... | ......................... |
| 10              | 0.98 ($0.93)                 | 0.97 ($0.28)           | 1.95 ($1.21)       |
| 100             | 1.47 ($8.99)                 | 6.00 ($0.86)           | 7.47 ($9.85)       |
| 1000            | 4.48 ($52.48)                | 58.01 ($13.74)         | 62.49 ($66.22)     |


To obtain these estimates, we ran the workflows in FireCloud on the default n1-highmem-4 compute nodes (26 GB RAM with 4 CPUs). Test-run samples were 1000 single-cell RRBS samples with a median of 872,223 reads.

---

### Contact information  

Divy Kangyen, 
Department of Biostatistics
Harvard T.H. Chan School of Public Health
Email address: divyswar01@g.harvard.edu

Issues and feature requests can be submitted to issue tracker in the [dna-methylation-tools github repo](https://github.com/aryeelab/dna-methylation-tools/issues)

---

### License  

**Copyright Broad Institute, 2019 | BSD-3**
All code provided in this workspace is released under the WDL open source code license (BSD-3) [full license text here](https://github.com/openwdl/wdl/blob/master/LICENSE). Note however that the programs called by the scripts may be subject to different licenses. Users are responsible for checking that they are authorized to run all programs before running these tools.
