---
layout: default
title: Question Two
---

<style> 
    body { -webkit-user-select: none; /* Chrome, Safari and Opera */ 
    -moz-user-select: none; /* Firefox */ 
    -ms-user-select: none; /* IE and Edge */ 
    user-select: none; /* standard syntax */ } 
</style>

## Problem Statement:
---
Given a folder containing text files, write a Python function that traverses through each file in the folder and calculates a final sum. Each file contains numbers paired with the following character signs:

- `a` or `+` denotes addition
- `s` or `-` denotes subtraction
- `m` or `*` denotes multiplication

The number and its corresponding operation are represented as a string e.g. `a20`, `s10`, `*.5`, where `a`, `s`, and `m` or `+`, `-`, `*` represent the operation (addition, subtraction, multiplication respectively), and the numbers following these characters represent operands. 

The function should perform the corresponding mathematical operation for each file, based on the given operation sign and operand, thereby producing a final sum for each file. If a file contains the name of another file, the final sum of the initial file should also include the summation of the file it has referenced.

Your task is to write a Python function that calculates the final sum for each file and returns the overall value for all files combined in the folder. 

Please note that each individual file does not contain any whitespace characters or empty lines, and all files are well-formatted, containing only valid operations (`a`, `s`, `m`, `+`, `-`, `*`) followed by a valid number (positive floating point or integer). 

Assume that folder structure can be at one level only, i.e., there are no folders inside another folder and there is no deadlock.

Additionally, remember to handle potential file and I/O exceptions in case a referenced file does not exist or cannot be read. 

The solution should be modular, well-structured and the code should be commented wherever necessary.

---

**Example**:
2 files [a.txt](https://raw.githubusercontent.com/ml106/CODING_TESTS/main/example_files/a.txt) and [b.txt](https://raw.githubusercontent.com/ml106/CODING_TESTS/main/example_files/b.txt) are as follows:

| a.txt | b.txt |
|-------|-------|
| a5    | a5    |
| -3    | m2    |
| b.txt |       

**Output**:
``{'a': 12.0, 'b': 10.0}`` 
a dictionary containing filenames as keys and their corresponding sums as the values.

