# Introduction

This data is the data used when creating RQ2 and consists of a csv file.

### Structure of folder and file name

Each folder indicates the subject of Defect4J and the csv file name of each inside the subject folder means tool name.

**Included Tools**

- EvoRand 600s
- EvoSuite 120s & 600s
- Randoop 120s & 600s

### Structure of file

The structure of the header is:

| ID.v | 00-09 | Count |
| --- | --- | --- |

**ID.v** : ID of Versions. Deprecated versions are already deleted.

**00-09** : Test ID. 1 means that test ID found the test, 0 is vice versa.

**Count** : Counts how many test ID found the test.

## Making Table

### For Table 3

#### Likelihood

The likelihood is calculated as:

![likelihood](https://github.com/starlab-unist/evorand_public/blob/main/md_img/rq2_likelihood_gray.png?raw=true)

$Count$ is from the value of Count column of CSV file, and  $Total$ is from the number of the version except deprecated version, same as RQ1 definition. 

We define the likelihood as the proportion of detected IDs out of total test IDs. In this equation, we do the experiment with 10 tests per version, hence  $\\#\ of\ Tests\ per\ Version$ would be 10.

#### Improvement Rate

For **RD→ER**, it is calculated as:

![improvement1](https://github.com/starlab-unist/evorand_public/blob/main/md_img/rq2_improvement_gray.png?raw=true)

For **ES→ER,** it is calculated as:

![improvement2](https://github.com/starlab-unist/evorand_public/blob/main/md_img/rq2_improvement2_gray.png?raw=true)

RD means Randoop, ES means EvoSuite, and ER means EvoRand.

## Findings

### Finding 3

EvoRand generates tests that detect bugs more consistently over multiple generations than Randoop and EvoSuite. $\text{E\scriptsize VO\normalsize R\scriptsize AND}\$ manifests a bug detection rate that is approximately 178% higher than Randoop and 13% higher than EvoSuite throughout all the projects.
