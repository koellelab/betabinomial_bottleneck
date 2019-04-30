# betabinomial_bottleneck
Code for estimating transmission bottleneck sizes using the betabinomial approach. 

The betabinomial approach for estimating transmission bottleneck sizes is described in:
Sobel Leonard et al. (2017) Journal of Virology. doi: 10.1128/JVI.00171-17
Transmission Bottleneck Size Estimation from Pathogen Deep-Sequencing Data, with an Application to Human Influenza A Virus

Here, we are providing both Matlab code and R code. Both sets of code include the mock (simulated) dataset that was used in the paper to test the apporach. 

Note that our JVI paper also provides estimates of the between-host transmission bottleneck size for influenza A virus that were based on data from Poon et al. 2016 Nature Genetics (doi: 10.1038/ng.3479). Xue & Bloom (2019) Nature Genetics (doi: 10.1038/s41588-019-0349-3) have shown that these data are “technically contaminated” with read pairs split between unrelated samples. In addition to increasing the amount of genetic diversity within a sample, this contamination inflates the similarities in allele frequencies between samples. As a result, when applied to these data, our betabinomial approach gives transmission bottleneck size estimates that are too large. The validity of the betabinomial estimation method presented in this paper is itself unaffected. However, the method estimated a transmission bottleneck size of 1-2 virions when it was applied to a different influenza A virus dataset (McCrone et al. (2018) eLife, doi: 10.7554/eLife.35962). We therefore would like to caution the reader when citing evidence for loose transmission bottleneck sizes for influenza A virus. 

