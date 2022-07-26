Below is a description of the files available for the second method - MLDA - for Combinations of Bacteria

1) additional_file_4_alzheimers_input_data_and_results.xlsx (multiple worksheets, 877 KB)
See readme tab in the spreadsheet for descriptions of each tab.
Shows a succession of files beginning with raw OTU data proceeding through various background removal and name summing stages. 
to the normalized abundances and microbial objects used in the Mathematica code below. 
Shown are results of the rebinning and renaming results described in the Abundance Binning, Microbe Naming and Object Merging section.  
Includes results: sample class distributions and approximate class counts and class distributions for each microbial object.

Below are the Mathematica notebook files (.nb suffix) with their input and output files.

2) additional_file_5_binning_and_object_computation_paper_v1.nb (Mathematica notebook, 35 KB). Takes the raw data with background removed and outputs microbial objects for each sample

input files:
additional_file_6_biomedataFilt.csv (comma-separated values, 110 KB). Raw data with background removed.

results files:
additional_file_7.1_microbiome_alzheimer's_input_11_s1.tsv (tab-separated values, 30KB)y
additional_file_7.2_microbiome_alzheimer's_input_11a_s1.tsv (tab-separated values, 32KB)
Two nearly identical files with microbial objects for each sample. The second file has the sample name in the second column while the first does not.

3) additional_file_8_classification_model_7_alzheimers_paper_v1.nb (Mathematica notebook, 1 MB). Contains the code for the MLDA classification.

input files:
additional_file_7.1_microbiome_alzheimer's_input_11_s1.tsv (tab-separated values, 30 KB)
additional_file_7.2_microbiome_alzheimer's_input_11a_s1.tsv (tab-separated values, 32KB)
See above.
	
additional_file_9_md1UAMS.csv (tab-separated values, 6 KB). Contains the metadata by sample including sample, subject, disease state, and brain location.

results files:
There are several standard output files whose variable names we list and describe below.

All of the following variables can also be exported by the code with computed file prefixes based on various input parameters. Each file will be automatically prefixed by parameters for the run. See the Export Section of this notebook.

>>> assigns: final assignment by sample for each object. Note this is the last assignment and does not have much use.

>>> dtOutputCnts: sample class count distributions after last iteration
additional_file_10_Alzheimers_AK_5_topics_a_0P3_b_0P25_cut_1_12.15rrtst_docTopicSum.csv (comma-separated values, 13 KB)) Sum file resulting from summing the dt1OutputCnts results from five runs and normalizing.


>>> dtOutput: normalized class distributions after last iteration

>>> vocabTopic5: object class count distributions after last iteration

>>> vocabTopic5Int: accumulated object class count distribution for thinned iterations

>>> dt1OutputCnts: accumulated sample class count distributions for thinned iterations

>>> dt1Output: accumulated normalized sample class count distributions for thinned iterations

>>> dataIX: indices of remaining samples after various applied filters 

>>> readme: user description of current run plus automated logging of parameters


4) additional_file_11_graph_alzheimers_paper.nb (Mathematica code, 1.5 MB). Takes the results of the MLDA classification (docTopicSum) and computes graph and approximate microbiomes.

input files:
additional_file_10_Alzheimers_AK_5_topics_a_0P3_b_0P25_cut_1_12.15rrtst_docTopicSum.csv (comma-separated values, 13 KB)) See above.

results files:
additional_file_12_microbiome_obj_approx_cnts.csv (comma-separated values, 4 KB)
additional_file_13_microbiome_obj_approx_norm.csv (comma-separated values, 7 KB)
Microbiome objects approximated from sample input data of a given color(output) - counts and normalized results

additional_file_14_allTable7.tsv (tab-separated values, 247 KB)
Combination of input objects, corresponding normalized abundance data, metadata, sample id, subject id and class components for data exploration. It has both raw object data and object data that has been rebinned and renamed. It is formatted for input to Mathematica variables. Useful for additional analysis.
Load with the following code:
allTable = ToExpression[Import["allTable7.tsv", "TSV"]]


Note: Graph results are not provided in this repository. These can be output as Mathematica entities which can be manipulated with Mathematica functions. If you are interested you may request these by contacting the corresponding author:
Jeffrey Lapides (jrl374@drexel.edu or jeffrey.lapides@gmail.com)
 
