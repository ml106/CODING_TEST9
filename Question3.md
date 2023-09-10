---
layout: default
title: Question Three
---



## Problem Statement:

Given a dataset, you are required to process and transform the data based on the following criteria:

1. Extract the digits from each cells in 'COL_1', 'COL_2', 'COL_3' and 'COL_4'.

2. Create a new column 'ANSWER' in the DataFrame by using the following formula: `ABS(COL_1 - COL_2 + COL_3 - COL_4)%100`. ABS is the absolute value and '%' denotes the modulus operation.

3. As the dataset contains multiple rows with the same 'ID', for each unique 'ID', find the maximum 'ANSWER' and add it to a new column 'MAX_ANSWER' in the DataFrame.

4. Next, map the values in 'MAX_ANSWER' to a word based on their range in the provided mapping. The word mapping is described below: 

    * "ANT": corresponds to values from 1 to 10 (inclusive),
    * "BUS": corresponds to values from 11 to 20 (inclusive),
    * "CAT": corresponds to values from 21 to 30 (inclusive),
    * "DOG": corresponds to values from 31 to 40 (inclusive),
    * "EGG": corresponds to values from 41 to 50 (inclusive),
    * "FAN": corresponds to values from 51 to 60 (inclusive),
    * "GUN": corresponds to values from 61 to 70 (inclusive),
    * "HAT": corresponds to values from 71 to 80 (inclusive),
    * "ICE": corresponds to values from 81 to 90 (inclusive),
    * "JAR": corresponds to values from 91 to 100 (inclusive)

Store this mapping in a dictionary named `ranges_dict`. Add a new column to the DataFrame 'MAPPED_WORD', which contains the word corresponding to the 'MAX_ANSWER' value for that row based on the provided mapping.

5. Lastly, generate a sentence `'I have a/an MAPPED_WORD'` for each row and add these sentences to a new column 'MAPPED_SENTENCE' in the DataFrame.

The initial DataFrame to be provided is saved in a file named `dataset.csv`.

[Get The File](https://drive.google.com/file/d/1xAIEFEVRZ7SfKrkyApy7MDiWeHgYsw-Y/view?usp=sharing)

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
---
<img src="https://cdn.discordapp.com/attachments/945567352014118962/1149405340450947153/image.png" alt="input1" style="display:inline-block; height:auto;"> 


To this:
---
<img src="https://cdn.discordapp.com/attachments/945567352014118962/1149405955528871996/image.png" alt="input1" style="display:inline-block; height:auto;"> 