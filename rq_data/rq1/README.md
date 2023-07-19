# Introduction

This data is the data used when creating RQ1 and consists of a CSV file.

## Structure of folder and file name

Each folder indicates the subject of Defect4J and the CSV file name of each inside the subject folder means tool name.

### **Included Tools**

- EvoRand 600s (ER600)
- EvoSuite 120s & 600s (ES120, ES600)
- Randoop 120s & 600s (RD120, RD600)

## Structure of file

The structure of the header is:

| ID.v | 00-09 | Detection |
| --- | --- | --- |

**ID.v** : ID of Versions. Deprecated versions are already deleted.

**00-09** : Test ID. 1 means that test ID found the test, 0 is vice versa.

**Detection** : If there is at least one test ID that found at least one test, then “Yes” is written. If not, “No” is written.

## Making Table

### For Table 1

#### Total

The number of all versions that is not deprecated. All the CSV file in the same subject have equal amount of rows, hence the total would be the number of rows of one of the CSV file in the subject except the header row.

#### Number of Bugs

The number of ‘Yes’ in each CSV file.

#### Detection Rate

Detection rate is calculated as:

![detection_rate](/md_img/rq1_detectionRate_gray.png)

It is calculated for each tools at each subject. In this case, $Number\ of\ Bugs$ indicates the number of bugs of tool that the tool had detected.

#### Improvement Rate

For **RD→ER**, it is calculated as:

![improvement1](/md_img/rq1_improvement_gray.png)

For **ES→ER,** it is calculated as:

![improvement2](/md_img/rq1_improvement2_gray.png)

RD means Randoop, ES means EvoSuite, and ER means EvoRand.

### For Table 2

#### Finding Uniqueness

For each CSV files that is in period of 600 seconds in each subject, we compare each versions and check the sameness of detection.

For checking the sameness of detection, We label each versions with flags. There are three flags and each and each shows whether the tool is detected the bug at that version or not. In this CSV, that feature could be done by “Detection” column.

**Example of labeling**

| ID.v | Tool 1 | Tool 2 | Tool 3 | Label |
| --- | --- | --- | --- | --- |
| 1 | Yes | No | No | 100 |
| 2 | Yes | No | Yes | 101 |

After labeling process, we only count for the label that has one 1 and two 0. We call this process ‘Filtering’. In other words, we only count the version that is unique for each tool. In the example above, we take ID.v 1 and discard ID.v 2.

The filtered labels through last process called ‘Classify’. The number is counted by increasing the value of the corresponding tool according to the position of each flag.

## Findings

### Finding 1

EvoRand increases the bug detection ability of the base tests by more than 12.8%, surpassing Randoop by 126.7% and EvoSuite by 9% in the same time budget.

### Finding 2

EvoRand detects almost twice of unique bugs that Randoop and EvoSuite are unable to detect.
