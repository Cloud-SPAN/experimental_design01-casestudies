---
title: "Platforms available and what is best for my experiment?"
teaching: 20
exercises: 20
questions:
- "What platform should we chose?"
- "What things influence platform choice or design if platform is fixed?"
objectives:
- "Understand the difference between long and short read sequencing"
- "Understand that different applications may require one or both types of sequencing"
- "Know that you may not neccesarily have control over the experimental design, but you should still be able to identify good and bad parts of experimental design"

keypoints:
- Short read sequencing is high throughput and can generate in many millions of reads. These reads are usually between 150-300bp long and have a high base accuracy
- Long read sequencing is lower throughput in terms of the number of reads we see compared to short read sequencing. However the reads are many kbs in length
- If in doubt about design, ask your facility you are using

---


# Outline


When we talk about sequencing, we can generally group it into either long read or short read sequencing.  However these are actually third generation and second generation sequencing technologies. Sanger sequencing was the first generation of sequencing and could sequence longer fragments than short read sequencing of today, however it was low throughput. Second generation sequencing, or next generation sequencing (NGS) as it is more commonly called, is a much higher throughput method but with reads typically 150-300bp long. As of July 2022, the NextSeq 550 high-output system runs  were capable of generating upto [800 million paired-end reads](https://emea.illumina.com/systems/sequencing-platforms/nextseq/specifications.html) in one run. Currently illumina sequencing is the predominant short read technology. Due to the length of the reads, the DNA/cDNA fragments ned to be broken into smaller pieces during the library preparation process, either through chemical means or through sonication. This is a key difference between short and long read technologies.

Long read sequencing is third generation sequencing, the current leading technologies for this are nanopore and pacbio. Unlike short read sequencing, these samples do not need fragmenting and so depending on the quality of the sample, reads are often several kb in length and 10-30kb fragments are common in good quality sample cases. Currently the longest read length for a nanopore run is 2.3Mb, [see here](https://www.biorxiv.org/content/10.1101/312256v1.full).

# Which type of sequencing is the most appropriate for me?


There are benefits to both kinds of sequencing, short read sequences have a higher based accuracy, whereas long read sequences are much longer, but have a lower base accuracy. Depending on your application, you may need to use one or both in combination. In some cases, for example if you're using publically available data, you will have no control over how the data is generated. Other factors to consider are what facilities you have access to at your institution. If your institution is a centre of excellence for nanopore sequencing for instance, you will have more expertise in handling these samples at your institution.

## How will my research question impact on the appropriateness of the platform/method of sequencing used?


There are lots of ways in which your research question can impact on what sequencing method you will use. Some of the following are worth considering before choosing your method:

- Does the system you are working on have a good reference?
- If you have a good reference, you may only need to align to this reference, and so short reads would be a good option
- If you don't have a good reference, are you trying to assemble your organism? If yes, long read assembly is much easier than short reads
- If the reference available appropriate for your organism? Or is the organism you're working on far enough removed to cause downstream analysis problems?
- Do you need to sequence lots of samples, or a few samples?
- Are you doing downstream analyses that require a high depth of sequencing?
- What is the content of the genome you're working on like? Does it contain lots of repeats that short reads might find hard to bridge?
- Does your downstream analysis depend on the base quality of your reads e.g. for SNP calling, or is abundance more importance e.g. RNAseq and metagenomics?



## Sequencing facilities


The current sequencing methods evolve rapidly, however there are established sequencing facilities that your data may be generated from if you are based in the UK. Some of the bigger centres are listed below. They should be able to inform you on the most up to date library preparation methods, how much data is required for your downstream analysis and any other requirements for sequencing:


[University of York, Technology Facility](https://www.york.ac.uk/biology/technology-facility/genomics/)

[University of Glasgow, Polyomics facility](https://www.polyomics.gla.ac.uk/)

[University of Sheffield, Genomics core facility](https://www.sheffield.ac.uk/medicine/facilities/genomics-core-facility)

[University of Liverpool, Centre of Genomic Research](https://www.liverpool.ac.uk/genomic-research/)


# How to deal with data from experiments you haven't designed?


You may be dealing with data that you haven't generated yourself, and have no control over experimental design. This could be data that is already within your lab, or this could be that you are using data that is in a data repository such as the european nucleotide archive [ENA](https://www.ebi.ac.uk/ena/browser/home or the short read archive) or [SRA](https://www.ncbi.nlm.nih.gov/sra).


If this is the case you may want to think of a few of the following? We will cover some of these points, such as replication and controls in greater detail, so don't worry if you don't understand these now.

- Will you be able to answer your research question with the data you are using?
- If not, could you adapt your research question to use the data and answer this new question?
- Is the platform used appropriate for your downstream analysis?


We should also be able to answer these additional questions later today

- Do they have the appropriate controls?
- Is there an appropriate number of replicates?
- Do we know how much variability there is in the system we are using?
- Do we have enough power in the data to see the effect we're anticipating?
