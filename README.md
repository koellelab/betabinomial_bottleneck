# betabinomial_bottleneck
Code for estimating transmission bottleneck sizes using the betabinomial approach. 

The betabinomial approach for estimating transmission bottleneck sizes is described in:
Sobel Leonard et al. (2017) Journal of Virology. doi: 10.1128/JVI.00171-17
Transmission Bottleneck Size Estimation from Pathogen Deep-Sequencing Data, with an Application to Human Influenza A Virus

Here, we are providing both Matlab code and R code. Both sets of code include the mock (simulated) dataset that was used in the paper to test the approach. The Matlab code was written by Katia Koelle (katia.koelle@gmail.com). The R code was written by Tyler Smith (tyler.smith@emory.edu). The R code has some Python dependencies. For any updates to the R code, you can go to:  https://github.com/weissmanlab/BB_bottleneck

2/25/2021 UPDATE:
Katia Koelle has uploaded a new zip file ("betabinomial_Nb_code_02_25_2021.zip") that contains extended/edited Matlab code for the betabinomial approach for estimating transmission bottleneck sizes. This zip file has edits that include:
- two more mock datasets, one for transmission bottleneck size Nb = 1 and one for transmission bottleneck size of Nb = 2
- the function "GetLikelihoodConfidenceIntervals" was corrected such that the 95% confidence intervals did not expand out by 1 too far on either side
- we noticed in the previous code that if a donor iSNV got fixed in a recipient (as one might expect when Nb is small), the code was not implemented to recognize this case. We have corrected this oversight in both the exact and approximate versions of the code, in the functions "GetBetaBinomialLogLikelihoodAtSite" and "GetBetaBinomialApproxLogLikelihoodAtSite", respectively. To further correct this oversight, there have been edits made to "main_BetaBinomial_estimateNb" and "main_BetaBinomial_approx_estimateNb". If you have used the old betabinomial code previously and have a situation where a donor iSNV became fixed in a recipient, your previously estimated bottleneck size likely errs on being too high. 

Tyler Smith has made analogous changes to these in his R implementation of the betabinomial approach. You can find his updated code here: https://github.com/weissmanlab/BB_bottleneck.  

Note that our JVI paper also provides estimates of the between-host transmission bottleneck size for influenza A virus that were based on data from Poon et al. 2016 Nature Genetics (doi: 10.1038/ng.3479). Xue & Bloom (2019) Nature Genetics (doi: 10.1038/s41588-019-0349-3) have shown that these data are “technically contaminated” with read pairs split between unrelated samples. In addition to increasing the amount of genetic diversity within a sample, this contamination inflates the similarities in allele frequencies between samples. As a result, when applied to these data, our betabinomial approach gives transmission bottleneck size estimates that are too large. The validity of the betabinomial estimation method presented in this paper is itself unaffected. However, the method estimated a transmission bottleneck size of 1-2 virions when it was applied to a different influenza A virus dataset (McCrone et al. (2018) eLife, doi: 10.7554/eLife.35962). We therefore would like to caution the reader when citing evidence for loose transmission bottleneck sizes for influenza A virus. 

