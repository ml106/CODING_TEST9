---
layout: default
title: Question Three
---

<style> 
    body { -webkit-user-select: none; /* Chrome, Safari and Opera */ 
    -moz-user-select: none; /* Firefox */ 
    -ms-user-select: none; /* IE and Edge */ 
    user-select: none; /* standard syntax */ } 
</style>

## Problem Statement:

Given a dataset, you are required to process and transform the data based on the following criteria:

1. Extract the digits from each cells in 'COL_1', 'COL_2', 'COL_3' and 'COL_4'.

2. Create a new column 'ANSWER' in the DataFrame by using the following formula: `ABS(COL_1 - COL_2 + COL_3 - COL_4)%100`. ABS is the absolute value and '%' denotes the modulus operation.

3. As the dataset contains multiple rows with the same 'ID', for each unique 'ID', find the maximum 'ANSWER' and add it to a new column 'MAX_ANSWER' in the DataFrame.

4. Next, map the values in 'MAX_ANSWER' to a word based on their range in the provided mapping. The word mapping is described below: 

    "ANT": corresponds to values from 1 to 10 (inclusive),
    "BUS": corresponds to values from 11 to 20 (inclusive),
    "CAT": corresponds to values from 21 to 30 (inclusive),
    "DOG": corresponds to values from 31 to 40 (inclusive),
    "EGG": corresponds to values from 41 to 50 (inclusive),
    "FAN": corresponds to values from 51 to 60 (inclusive),
    "GUN": corresponds to values from 61 to 70 (inclusive),
    "HAT": corresponds to values from 71 to 80 (inclusive),
    "ICE": corresponds to values from 81 to 90 (inclusive),
    "JAR": corresponds to values from 91 to 100 (inclusive)

Store this mapping in a dictionary named `ranges_dict`. Add a new column to the DataFrame 'MAPPED_WORD', which contains the word corresponding to the 'MAX_ANSWER' value for that row based on the provided mapping.

5. Lastly, generate a sentence `'I have a/an MAPPED_WORD'` for each row and add these sentences to a new column 'MAPPED_SENTENCE' in the DataFrame.

The initial DataFrame to be provided is saved in a file named `dataset.csv`.

Your task is to write a Python function with the following signature:
```python
def process_data(file_path: str) -> pd.DataFrame:
```

**Input:**
- file_path : str : Path to the input csv file `dataset.csv`.

**Output:**
- pd.DataFrame : The processed DataFrame with new columns 'ANSWER', 'MAX_ANSWER', 'MAPPED_WORD' and 'MAPPED_SENTENCE'.

**Example:**

You need to transform this DataFrame:

| Index | ID | COL_1    | COL_2    | COL_3    | COL_4    |
|-------|----|----------|----------|----------|----------|
| 0     |  1 | asd34asdas | abc45def | klm76nop | zxc43vbn |
| 1     |  2 | jdshf23xkljj | zxc24poi | iuy35mnb | lkm89juh |
| 2     |  3 | @KKLNmd12*) | %IJKsd78@) | !OPQst12@# | &POIgh78*) |
| 3     |  4 | ^#^#&*)56&*& | $^#87)@# | &^%54$#@ | #^%)(54@$ |
| 4     |  1 | klgk95SKD | rtz98QWE | xyz78RST | pqr12JKL |
| 5     |  4 | SBU+_)45dsfm | XYZ&(45ghj | TUV#)(23opq | MNO_*&45xyz |

To this:

| Index | ID | COL_1 | COL_2 | COL_3 | COL_4 | ANSWER | MAX_ANSWER | MAPPED_WORD | MAPPED_SENTENCE |
|-------|----|-------|-------|-------|-------|--------|------------|-------------|-----------------|
| 0     |  1 |    34 |    45 |    76 |    43 |     22 |         63 | GUN         | I have a GUN    |
| 1     |  2 |    23 |    24 |    35 |    89 |     55 |         55 | FAN         | I have a FAN    |
| 2     |  3 |    12 |    78 |    12 |    78 |     32 |         32 | DOG         | I have a DOG    |
| 3     |  4 |    56 |    87 |    54 |    54 |     31 |         31 | DOG         | I have a DOG    |
| 4     |  1 |    95 |    98 |    78 |    12 |     63 |         63 | GUN         | I have a GUN    |
| 5     |  4 |    45 |    45 |    23 |    45 |     22 |         31 | DOG         | I have a DOG    |