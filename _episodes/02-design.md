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
Negative controls are samples that are treated the same way as other samples except the variables of interest are a placebo and are not expected to have any effect. An example of a negative control for sequencing experiments is processing "blanks" with no DNA with the same kits and on the same run to determine levels of kit contamination. This can be especially important in environmental samples since contaminanting taxa may be indistinguishable from those present in the samples and in low biomass samples where sequences derived from contamination can dominate.

### Postive controls
Positive controls are samples that should have known results and they used to check that preparation and sequencing procedures are working and are reproducible, that is, to ensure that the contained organisms can be sufficiently extracted. An example of a positive control for microbiome sequencing is a "mock community" containing known mixtures of known organisms.


# Replication
general


## Biologicial replication
Most biologists instinctively appreciate the importance of biological replication to ensure that experimental results generalise. If we compare one wildtype plant against one geneticaly modified plant

## Technical Replication
measurement accuracy

control every aspect of variablity that you can. sample prep etc

what is downstream analysis - a particular software may have demands.

## Effect of replication on statistical analysis

depends on variation
calculation of, source of the  n = 3 rule
for signifcance, variation within groups < variation between group
some variation can be controlled, some is inherent. control as much as you can
importance of controlling as much variation as possible = fewer replicates needed. increasing more variation that is strictly requires greater replication.


## Pseudoreplication

# Budget
number of samples
number of reps
availability of equipment
might need to amend your question to meet budget

# Sample storage
Storage conditions such as preservation method, duration in storage and the temperature of freezers and refrigerators can alter samples therefore it is essential to rigorously treat all you samples exactly the same way. This minimises the variation between samples which has nothing to do with the effects of interest.

# Further reading
Salter, S.J., Cox, M.J., Turek, E.M. et al. Reagent and laboratory contamination can critically impact sequence-based microbiome analyses. BMC Biol 12, 87 (2014). https://doi.org/10.1186/s12915-014-0087-z

Kim, D., Hofstaedter, C.E., Zhao, C. et al. Optimizing methods and dodging pitfalls in microbiome research. Microbiome 5, 52 (2017). https://doi.org/10.1186/s40168-017-0267-5

