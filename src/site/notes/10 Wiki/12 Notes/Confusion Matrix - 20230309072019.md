---
{"dg-publish":true,"permalink":"/10-wiki/12-notes/confusion-matrix-20230309072019/"}
---

# Confusion Matrix
---
A confusion matrix is a table that is often used to describe the performance of a machine learning model on a set of test data for which the true values are known. It allows visualization of the performance of an algorithm.

|                    | Actual Positive     | Actual Negative     |
| ------------------ | ------------------- | ------------------- |
| Predicted Positive | True Positive (TP)  | False Positive (FP) |
| Predicted Negative | False Negative (FN) | True Negative (TN)                    |

True Positive (TP): The model predicted positive and it was actually positive.
False Positive (FP): The model predicted positive but it was actually negative.
False Negative (FN): The model predicted negative but it was actually positive.
True Negative (TN): The model predicted negative and it was actually negative.

The values in the cells represent the number of instances that fall into each of these categories. The confusion matrix is often used to calculate metrics such as [[100 Zettelkasten/Precision\|Precision]], [[100 Zettelkasten/Recall\|Recall]], and [[100 Zettelkasten/F1 Score\|F1 Score]].



###### META
Status:: #wiki/notes/mature 
Plantations:: [[10 Wiki/13 Plantations/Data Science Metrics - 20230221095821\|Data Science Metrics]]
References:: 
