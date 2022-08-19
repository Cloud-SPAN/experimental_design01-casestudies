---
title: "Understanding experimental design"
teaching: 20
exercises: 10
questions:
- What controls do I need
- How many replicates do I need?
- What are sequence coverage and depth
- What can I afford
objectives:
- understand the difference between biological and technical replication   
- understand important of controls
- understand depth and coverage
- Identify best choices when budget is limited
keypoints:
- "X,Y,Z are important and should be looked at when designing experiments"

---
# Planning

## Controls

Experimental controls are treatments or variables included with predictable outcomes that ensure that the measurements of interest are valid. They allow us to assess whether all the experimental steps were correctly performed and to make meaningful comparisons between treatments. They can be positive or negative.

### Negative controls
Negative controls are samples that are treated the same way as other samples except the variables of interest are a placebo and are not expected to have any effect. An example of a negative control for sequencing experiments is processing "blanks" with no DNA with the same kits and on the same run to determine levels of kit contamination. This can be especially important in environmental samples since contaminanting taxa may be indistinguishable from those present in the samples, and in low biomass samples where sequences derived from contamination can dominate.

### Postive controls
Positive controls are samples that should have known results and they used to check that preparation and sequencing procedures are working and are reproducible, that is, to ensure that the contained organisms can be sufficiently extracted. An example of a positive control for microbiome sequencing is a "mock community" containing known mixtures of known organisms. 


# Replication
general


## Biologicial replication
Most biologists instinctively appreciate the importance of biological replication to ensure that experimental results generalise. If the yield of one geneticaly modified plant is higher than that of one wildtype plant we cannot be sure that this is because of the modifcation (i.e., generalisable) or is a difference just in these two plants. Having multiple GMO and WT plants allows us to determine if the variation been plants types is greater than the random variation within plant types.
Biological replicates from multiple distinct samples need to be taken for each experimental group (e.g., the same treatment or condition) to provide a measure of within-group variation. It is common to see three replicates being recommended - this is an absolute minimum suitable only when the variation between samples within experimental groups is low compared to that between experimental groups. This situation is typical in cell biology experiments when experimental conditions are well controlled and often on genetically homogenous cell lines or organisims. It is far less likely for environmental sampling of microbial communities when it is wiser to have more samples. It is often worth limiting the number of experimental conditions so that sufficient replication in each condition can be achieved. 
Biological replication determines the sample size.

## Technical Replication
Technical replicates are those we make to ensure the reproducibility of the data generated using identical protocols and equipment. Technical replicates are done on the same biological sample so that the only variation between replicates is due to random variation in protocol and equipment outputs. Only if the variation between technical replicates is small relative to the variation between biological replicates can we be sure the variation is down to biology. Technical replication does not contribute to sample size - if you have taken 10 techincal replicates from each of two biological replicates, your sample size is n = 2.

## Pseudoreplication

## Effect of replication on statistical analysis

depends on variation

for signifcance, variation within groups < variation between group
some variation can be controlled, some is inherent. control as much as you can
importance of controlling as much variation as possible = fewer replicates needed. increasing more variation that is strictly requires greater replication.




# Budget
number of samples
number of reps
availability of equipment
might need to amend your question to meet budget

# Sample storage
Storage conditions such as preservation method, duration in storage and the temperature of freezers and refrigerators can affect DAN yield and quality therefore it is essential to rigorously treat all you samples exactly the same way. This minimises the variation between samples which has nothing to do with the effects of interest.

# Sequencing coverage and depth
coverage must be sufficient for assembly


# Further reading


Di Bella, J.M., Bao, Y., Gloor, G.B., Burton, J.P., Reid, G., 2013. High throughput sequencing methods and analysis for microbiome research. Journal of Microbiological Methods 95, 401–414. https://doi.org/10.1016/j.mimet.2013.08.011

Goodrich, J.K., Di Rienzi, S.C., Poole, A.C., Koren, O., Walters, W.A., Caporaso, J.G., Knight, R., Ley, R.E., 2014. Conducting a Microbiome Study. Cell 158, 250–262. https://doi.org/10.1016/j.cell.2014.06.037

Ju, F., Zhang, T., 2015. Experimental Design and Bioinformatics Analysis for the Application of Metagenomics in Environmental Sciences and Biotechnology. Environ. Sci. Technol. 49, 12628–12640. https://doi.org/10.1021/acs.est.5b03719

Kim, D., Hofstaedter, C.E., Zhao, C. et al. Optimizing methods and dodging pitfalls in microbiome research. Microbiome 5, 52 (2017). https://doi.org/10.1186/s40168-017-0267-5

Salter, S.J., Cox, M.J., Turek, E.M. et al. Reagent and laboratory contamination can critically impact sequence-based microbiome analyses. BMC Biol 12, 87 (2014). https://doi.org/10.1186/s12915-014-0087-z
