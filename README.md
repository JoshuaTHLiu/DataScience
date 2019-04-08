# Nuanced Metrics for Measuring Unintended Bias with Real Data for Text Classification

GOAL

Create an evaluation metric that measures the amount of biases.  The metric is also designed to be  threshold-agnostic and robust to class implance.

METRIC

Evaluate metric for each subgroup (identity) and compare to the background data (the rest of the data).

Subgroups
1. positive background G<sup>+</sup>
2. negative background G<sup>-</sup>
3. positive subgroup G<sup>+</sup><sub>g</sub>
4. negative subgroup G<sup>-</sup><sub>g</sub>

TERMS

Area Under the Receiver Operating Characteristic Curve (ROC-AUC, or AUC) metric. For any classifier, AUC measures the probability that a randomly chosen negative example will receive a lower score than a randomly chosen positive example, i.e. that the two will be correctly ordered. An AUC of 1.0 means that all negative/positive pairs are correctly ordered, with all negative items receiving lower scores than all positive items

REFERENCES

https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet#lists
