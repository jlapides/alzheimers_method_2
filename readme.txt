The following files are submitted with the paper and posted in GitHub

1) alzheimers_input_data_and_results.xlsx 
See readme tab in the spreadsheet
includes a spreadsheet which shows a succession of files beginning with raw OTU data proceeding through various background removal and name summing stages to the normalized abundances, microbial objects, rebinning and renaming results,  and metadata. It also includes mold results: sample class distributions and approximate class counts for each microbial object.

The following Mathematica notebooks (code) and files are posted in GitHub at:
https://github.com/jlapides/MLDA.
Note: with have added a letter prefix to show which data files are associated with each notebook. If you wish to use the data files, remove the prefix as the notebook input code does not include the prefix. 


2) binning_and_object_computation_paper_v1.nb 

input files:
biomedataFilt.csv 

results files:
microbiome_alzheimer's_input_11_s1.tsv
microbiome_alzheimer's_input_11a_s1.tsv 

3) classification_model_7_alzheimers_paper_v1.nb

input files:
microbiome_alzheimer's_input_11_s1.tsv
microbiome_alzheimer's_input_11a_s1.tsv
md1UAMS.csv

results files:
There are several files whose variable names we list and describe below.
We have posted the sum file resulting from summing the dt1OutputCnts results from five runs and normalizing.
Alzheimers_AK_5_topics_a_0P3_b_0P25_cut_1_12.15rrtst_docTopicSum.csv 

All of the following variables can also be exported by the code with computed file prefixes based on various input parameters. Each file will be automatically prefixed by parameters for the run. See the Export Section of this notebook.

>>> assigns: final assignment by sample for each object. Note this is the last assignment and does not have much use.

>>> dtOutputCnts: sample class count distributions after last iteration

>>> dtOutput: normalized class distributions after last iteration

>>> vocabTopic5: object class count distributions after last iteration

>>> vocabTopic5Int: accumulated object class count distribution for thinned iterations

>>> dt1OutputCnts: accumulated sample class count distributions for thinned iterations

>>> dt1Output: accumulated normalized sample class count distributions for thinned iterations

>>> dataIX: indices of remaining samples after various applied filters 

>>> readme: user description of current run plus automated logging of parameters


4) graph_alzheimers_paper.nb

input files:
Alzheimers_AK_5_topics_a_0P3_b_0P25_cut_1_12.15rrtst_docTopicSum.csv

results files:
allTable7.tsv: this file has a mix of input objects, corresponding normalized abundance data, metadata, sample id, subject id and class components for data exploration. It is loaded at the end.

note: the main result for this notebook is the graph which we have not stored as 
separate files. See the figures in the paper.

The following files are submitted with the paper:


