# RQ2

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