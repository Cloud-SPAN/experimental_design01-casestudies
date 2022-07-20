---
title: "Statistical Analysis"
teaching: 20
exercises: 10
questions:
-  "What is a type I and type II error?"
-  "What is multiple correction and why would we use it?"
-  "What are the multiple correction methods we can use"
objectives:
- Understand what a type I and type II error is.
- Understand ways we can increase/decrease type I and type II errors using statistical design.
- Understand the difference between the Bonferroni correction and Benjamini and Hochberg False Discovery rate.
keypoints:
- Type I errors are those caused by False positives.
- Type II errors are those caused by False negatives.
- We can reduce Type I errors by using a more stringent alpha threshold.
- We can reduce Type II errors by improving the power in an experiment by increasing the number of replicates used.
- High throughput experiments require us to use multiple testing correction. There are two popular methods to do this, the most stringent is the Bonferroni correction, the least stringent is the Benjamini Hochberg FDR.

---


**Note this is not a statistics course, and there are plenty of free resources where you can find out more about how type I and type II errors are calculated. This is just enough information for you to have the key concepts needed for this course**

# What are type I and type II errors?

## Type I errors : false positive

When you have rejected a true null hypothesis incorrectly. Your finding appears significant but this has occured by chance.

### How to counter?

The probability of type I errors are represented by an alpha value (**α**). This is the significance level (the p-value),  that you have used to reject the null hypthothesis. The commonly used 0.05 value means that you accept a 5% chance of a insignificant value being accidentally significant.You can reduce type I errors by using a lower p-value, e.g. using a 0.01 p value would lower the chance of a type I error to 1%.

## Type II errors: false negative

You have failed to reject the null hypthothesis. Your finding appears insignificant but is it is significant.

### How to counter

Type II errors are related to the power of a statistical test. The probability of a type II error is represented by a beta value (**β**). The power of a statistical test is calculated as power = 1- β. The larger the β value, the higher the risk of type II errors. You can reduce type II errors by making sure you test has enough power. This can be controlled by making sure your sample size is large enough to observe the effect you're measuring. One of the ways you can do this is to include enough replicates in your experimental design. It also depends on how big the effect is you're trying to test. Smaller effects will require large sample sizes.



# What do we need multiple testing correction?

In high throughput experiments, such as generating proteomic data, or sequencing data, you are performing many tests of significance. For example, in the *Mus Musculus* genome,there are approximately 24,000 protein coding genes. In an RNAseq experiment, we are performing a test of significance in the number of counts as a proxy for expression 24,000 times. This means that if 5% of the tests are false positives, we would have 1200 genes that are considered falsely to be significantly different in expression. So for experiments like we need to perform additional corrections to account for these. We call this **multiple testing correction**.

There are a couple of common correction methods. The two most common are Bonferroni and the Benjamini and Hochberg False Discovery Rate. You might see these referred to as the BC (Bonferroni Correction), BH  (Benjamini Hochberg), and FDR (False Discovery Rate).

## Bonferroni correction
 This is calculated by multiplying the p-value of the test by the number of total tests performed. If we use an error rate of 0.05, and the corrected value is still under 0.05, it is considered significant.

 **Corrected p-value = p-value * n (number of tests)**

 Conversely, you can calculate the p-value threshold needed to pass the significance thershold after correction by dividing 0.05 * n.

 This is  very stringent. If you were looking at 24,000 genes like in the mouse example above, the p-value would have to be  **0.0000021** pre correction to pass.

This is using the Family-wise error rate (FWER) rate of 0.05. We do not have to understand how this is calculated, but the FWER rate is the probability of calculating any Type I errors at all. So it is related to the α value above, but it is not the same. After  correction, an FWER rate of 5% expects 5% of the genes to be significant by chance.

Bonferroni uses the FWER to control the type of error. So it is very stringent, but it reduces the number of false positives. **However** as a result you increase the number of false negatives.

## Benjamini and Hochberg False Discovery Rate

This correction is less stringent. As a result you will end up with more false positives, but you will also have less false negatives. It is slightly more complicated than the Bonferroni corection. Instead of the FWER controlling the error rate, we use instead a False Discovery Rate (FDR). This means that with a FDR value of 0.05, 5% of the genes are significant after correction are false positives.

 1. You take all p-values from all of your tests and rank them from smallest to largest.
 2. The p-values are corrected by multiplying the number of tests divided by it's rank. For a error rate of 0.05, if the corrected p-value is less than 0.05, it is significant.

 **Corrected p-value = p-value*(n/rank)**

## Example

 If we look at the top three genes (largest p-values) using the mouse RNAseq example again. The number of genes (n) is 24,000. We are setting the error rate at 0.05. We are ranking from smallest to largest, so the largest values will have the highest ranks. The gene with the highest p-value, 0.2, will have a rank of 24,000. The second and third, will have ranks 23,999, 23,998.


        |p-value |  Rank Corrected | p-value |
|-------|--------|-----------------|---------|
| Gene A | 0.2 | 24,000 | Uncorrected |
| Gene B | 0.06 | 23,999 | 0.060002501b |
| Gene C | 0.04 | 23,998 | 0.04000333361 |

 **Gene A**  

 **Corrected p-value = 0.2 * (24,000/24,000)**

 For the largest p-value gene, the rank and number of tests equals 1, and so this p-value is not corrected

 **Gene B**

  **Corrected p-value = 0.06 * (24,000/23,999)**


 **Gene C**

**Corrected p-value = 0.04 * (24,000/23,998)**



Due to the ratio between (n/rank), the correction is more stringent as the p-value decreases.

There are other variations on these multiple testing methods, but these are the most common. The default for most software is to use the Benjamini and Hochberg False Discovery rate because  having less stringency means that you get a good balance between false positives and false negatives. You can still control the false positives by changing the FDR value.

However depending on your situation, for instance if you are concerned about false positives more than false negatives and need to be conservative, for instance in a medical trial where safety is very important. Then the Bonferroni correction may be more useful for you.
