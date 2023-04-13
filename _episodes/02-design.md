---
title: "Understanding experimental design"
teaching: 20
exercises: 10
questions:
- What controls do I need
- How many replicates do I need?
- What are sequence coverage and depth
objectives:
- Understand the difference between biological and technical replication   
- Understand important of controls
- Understand sequence depth and coverage
keypoints:
- Most experiments need positive and negative controls
- Technical replicates ensure our measures are reproducible
- Biological replicates ensure our results generalise
- Coverage is the percentage of the reference genome sequenced
- Depth is the average number of times a base is sequenced
- There is a trade-off between sequencing depth and the need for controls and replicates

---
# Controls

Experimental controls are treatments or variables included with predictable outcomes that ensure that the measurements of interest are valid. They allow us to assess whether all the experimental steps were correctly performed and to make meaningful comparisons between treatments. They can be positive or negative.

## Negative controls
Negative controls are samples that are treated the same way as other samples except the variables of interest are a placebo and are not expected to have any effect. An example of a negative control for sequencing experiments is processing "blanks" with no DNA with the same kits and on the same run to determine levels of kit contamination. This can be especially important in environmental samples since contaminating taxa may be indistinguishable from those present in the samples, and in low biomass samples where sequences derived from contamination can dominate.

## Postive controls
Positive controls are samples that should have known results and they used to check that preparation and sequencing procedures are working and are reproducible, that is, to ensure that the contained organisms can be sufficiently extracted. An example of a positive control for microbiome sequencing is a "mock community" containing known mixtures of known organisms.


# Replication
We replicate measurements because things vary and we want to be certain our conclusions are based on a biological explanation rather than noise in the data.


## Biological replication
Most biologists instinctively appreciate the importance of biological replication to ensure that experimental results generalise. If the yield of one geneticaly modified plant is higher than that of one wildtype plant we cannot be sure that this is because of the modifcation (i.e., generalisable) or is a difference just in these two plants. Having multiple GMO and WT plants allows us to determine if the variation been plants types is greater than the random variation within plant types.
Biological replicates from multiple distinct samples need to be taken for each experimental group (e.g., the same treatment or condition) to provide a measure of within-group variation. 

It is common to see three replicates being recommended - this is an absolute minimum suitable only when the variation between samples within experimental groups is low compared to that between experimental groups. This situation is typical in cell biology experiments when experimental conditions can be made very consistent using genetically homogenous cell lines or organisms. It is far less likely for environmental sampling of microbial communities. As a general rule, the greater the random biological variation, the greater the need for more replicates. It is often worth limiting the number of experimental conditions so that sufficient replication in each condition can be achieved.
As a general rule, the greater the replication the greater the power of any statistical testing.

## Technical Replication
Technical replicates are those we make to ensure the reproducibility of the data generated using identical protocols and equipment. Technical replicates are done on the same biological sample so that the only variation between replicates is due to random variation in protocol and equipment outputs. Only if the variation between technical replicates is small relative to the variation between biological replicates can we be sure the variation is down to biology. Technical replication does not contribute to sample size - if you have taken 10 technical replicates from each of two biological replicates, your sample size is n = 2. Technical replicates are non-independent - the values for one technical replicate are more similar to those from another technical replicate on the same biological replicate than to any technical replicate from another biological replicate. Biological replication determines the sample size.

# Sample storage
Storage conditions such as preservation method, duration in storage and the temperature of freezers and refrigerators can affect DNA yield and quality therefore it is essential to rigorously treat all you samples exactly the same way. This minimises the variation between samples which has nothing to do with the effects of interest.

# Depth and coverage
The use of these terms is not consistent but coverage used on its own usually means the the percentage of the reference genome sequenced. It is also known as *breadth of coverage*. However, you do see coverage used to mean depth - the context normally makes it clear which is meant.  Sequencing depth is also known as *read depth* or *depth of coverage* or *redundancy of coverage*.  It is the average number of time a base is sequenced. Every base in a sample must be sequencing multiple times. This is because
- Base calling is not 100% accurate so you meed multiple observations per base to reliably determine the base
- Reads are distributed randomly, not evenly, across the genome so that some bases will be sequences more than average, others less than average.
Depth is calculated by the total number of bases of aligned by the length of the genome or targetted subset of the genome. It is often expresed as 2X (two times coverage), 5X etc. Deep sequencing means aiming for a high number of reads for each base.

The amount of coverage needed depends on the sequencing error rate, the read length and the system under study. If you are trying to detect rare events, such as rare SNPs in genomics or lowly expressed genes in transcriptomics you will need greater depth.

# Further reading


Di Bella, J.M., Bao, Y., Gloor, G.B., Burton, J.P., Reid, G., 2013. High throughput sequencing methods and analysis for microbiome research. Journal of Microbiological Methods 95, 401–414. [https://doi.org/10.1016/j.mimet.2013.08.011](https://doi.org/10.1016/j.mimet.2013.08.011)

Goodrich, J.K., Di Rienzi, S.C., Poole, A.C., Koren, O., Walters, W.A., Caporaso, J.G., Knight, R., Ley, R.E., 2014. Conducting a Microbiome Study. Cell 158, 250–262. [https://doi.org/10.1016/j.cell.2014.06.037](https://doi.org/10.1016/j.cell.2014.06.037)

Ju, F., Zhang, T., 2015. Experimental Design and Bioinformatics Analysis for the Application of Metagenomics in Environmental Sciences and Biotechnology. Environ. Sci. Technol. 49, 12628–12640. [https://doi.org/10.1021/acs.est.5b03719](https://doi.org/10.1021/acs.est.5b03719)

Kim, D., Hofstaedter, C.E., Zhao, C. et al. Optimizing methods and dodging pitfalls in microbiome research. Microbiome 5, 52 (2017). [https://doi.org/10.1186/s40168-017-0267-5](https://doi.org/10.1186/s40168-017-0267-5)

Salter, S.J., Cox, M.J., Turek, E.M. et al. Reagent and laboratory contamination can critically impact sequence-based microbiome analyses. BMC Biol 12, 87 (2014). [https://doi.org/10.1186/s12915-014-0087-z](https://doi.org/10.1186/s12915-014-0087-z)

Sims, D., Sudbery, I., Ilott, N. et al. Sequencing depth and coverage: key considerations in genomic analyses. Nat Rev Genet 15, 121–132 (2014). [https://doi.org/10.1038/nrg3642](https://doi.org/10.1038/nrg3642)
