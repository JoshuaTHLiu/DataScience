# Nuanced Metrics for Measuring Unintended Bias with Real Data for Text Classification

## GOAL

Create an evaluation metric that measures the amount of biases.  The metric is also designed to be  threshold-agnostic and robust to class implance.

## METRIC

Evaluate metric for each subgroup (identity) and compare to the background data (the rest of the data).  Calculates AUC for each subgroup which attempts to minimize class imblance.

Subgroups
1. positive background D<sup>+</sup>
2. negative background D<sup>-</sup>
3. positive subgroup D<sup>+</sup><sub>g</sub>
4. negative subgroup D<sup>-</sup><sub>g</sub>

Subgroup Metrics
1. Subgroup AUC = AUC(D<sup>-</sup><sub>g</sub> + D<sup>+</sup><sub>g</sub>)
2. Background Positive Subgroup Negative (BPSN) AUC = AUC(D<sup>+</sup> + D<sup>-</sup><sub>g</sub>) (attempts to track false positives)
3. BNSP = AUC(D<sup>-</sup> + D<sup>+</sup><sub>g</sub>) (attempts to track false negatives)
3. Positive AEG = MWU(D<sup>+</sup><sub>g</sub>, D<sup>+</sup>) / |D<sup>+</sup><sub>g</sub>| |D<sup>+</sup>|
 - Mann-Whiteny U test (MWU)
 - values range from -1/2 to 1/2
 - value of 0 means the mean for TPR<sub>g</sub> and TPR are the same.
4. Negative AEG - same as positive AEG but with true false rate (TFR)


## TERMS

Area Under the Receiver Operating Characteristic Curve (ROC-AUC, or AUC) metric - For any classifier, AUC measures the probability that a randomly chosen negative example will receive a lower score than a randomly chosen positive example, i.e. that the two will be correctly ordered. An AUC of 1.0 means that all negative/positive pairs are correctly ordered, with all negative items receiving lower scores than all positive items

Equality Gap - The Equality Gap is the difference between the true positive rates of the subgroup (TPR(D<sub>g</sub>)) and the background (TPR(D)), at a specific threshold

Equality of Opporunity - this exists when
 - P(y'<sub>g</sub> > y'| y<sub>g</sub> in D<sup>+</sup><sub>g</sub>, y in D<sup>+</sup>) = 0.5

## REFERENCES

https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#lists
