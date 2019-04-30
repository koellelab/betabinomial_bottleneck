# betabinomial_bottleneck
Code for estimating transmission bottleneck sizes using the betabinomial approach. 

The betabinomial approach for estimating transmission bottleneck sizes is described in:
Sobel Leonard et al. (2017) Journal of Virology. doi: 10.1128/JVI.00171-17
Transmission Bottleneck Size Estimation from Pathogen Deep-Sequencing Data, with an Application to Human Influenza A Virus

Here, we are providing both Matlab code and R code. Both sets of code include the mock (simulated) dataset that was used in the paper to test the apporach. 

Note that this paper also provides an application of the betabinomial approach to a dataset published by Poon et al. (2016) Nature Genetics (doi: 10.1038/ng.3479). From these data, we estimated bottleneck sizes on the order of 200 between transmission pairs, consistent with findings from Poon et al. However, a later analysis of this Poon et al. dataset indicated that the deep-sequencing data were "technically contaminated" (Xue and Bloom (2019) Nature Genetics, doi: 10.1038/s41588-019-0349-3). When our betabinomial approach was applied to a different deep-sequencing dataset from Michigan, it gave estimated of 1-2 virions as the transmission bottleneck size for influenza A virus (McCrone et al. (2018) eLife, doi: 10.7554/eLife.35962).  


