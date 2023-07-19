# Introduction

This data is the data used when creating RQ3 and consists of a csv file.

### Structure of folder and file name

Each folder indicates the subject of Defect4J and the csv file name of each inside the subject folder means tool name.

**Included Tools**

- EvoRand 240s & 600s

### Structure of file

The structure of the header is:

| ID.v | 00-09 | Detection |
| --- | --- | --- |

ID.v : ID of Versions. Deprecated versions are already deleted.

00-09 : Test ID. 1 means that test ID found the test, 0 is vice versa.

Detection : If there is at least one test ID that found at least one test, then “Yes” is written. If not, “No” is written.

## Making Table

### For Table 4

#### Number of Bugs

The number of ‘Yes’ in each CSV file.

#### Percentage Found in 240 Seconds

It simply shows the percentage of bugs already found in 240 seconds out of bugs found by the end of 600 seconds. The equation is:

![240detect](https://github.com/starlab-unist/evorand_public/blob/main/md_img/rq3_240detect_gray.png?raw=true)

## Findings

### Finding 4

EvoRand's approach is highly efficient, detecting over 99% of the discovered bugs within the initial 240 seconds time budget.
