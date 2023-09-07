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

```python
df = pd.DataFrame(
    {
        'ID': [1, 2, 3, 4, 1, 4],
        'COL_1': ['asd34asdas', 'jdshf23xkljj', '@KKLNmd12*)', '^#^#&*)56&*&', 'klgk95SKD', 'SBU+_)45dsfm'],
        'COL_2': ['abc45def', 'zxc24poi', '%IJKsd78@)', '$^#87)@#', 'rtz98QWE', 'XYZ&(45ghj'],
        'COL_3': ['klm76nop', 'iuy35mnb', '!OPQst12@#', '&^%54$#@', 'xyz78RST', 'TUV#)(23opq'],
        'COL_4': ['zxc43vbn', 'lkm89juh', '&POIgh78*)', '#^%)(54@$', 'pqr12JKL', 'MNO_*&45xyz'],
    }
)
```

To this:

```python
df = pd.DataFrame(
    {'ID': {0: 1, 1: 2, 2: 3, 3: 4, 4: 1, 5: 4},
     'COL_1': {0: 34, 1: 23, 2: 12, 3: 56, 4: 95, 5: 45},
     'COL_2': {0: 45, 1: 24, 2: 78, 3: 87, 4: 98, 5: 45},
     'COL_3': {0: 76, 1: 35, 2: 12, 3: 54, 4: 78, 5: 23},
     'COL_4': {0: 43, 1: 89, 2: 78, 3: 54, 4: 12, 5: 45},
     'ANSWER': {0: 22, 1: 55, 2: 32, 3: 31, 4: 63, 5: 22},
     'MAX_ANSWER': {0: 63, 1: 55, 2: 32, 3: 31, 4: 63, 5: 31},
     'MAPPED_WORD': {0: 'GUN', 1: 'FAN', 2: 'DOG', 3: 'DOG', 4: 'GUN', 5: 'DOG'},
     'MAPPED_SENTENCE': {0: 'I have a GUN',
                         1: 'I have a FAN',
                         2: 'I have a DOG',
                         3: 'I have a DOG',
                         4: 'I have a GUN',
                         5: 'I have a DOG'}}
)
```