## Problem Statement:

Let's say you are working as a system administrator in a company. You have to manage multiple servers daily. You save the information about servers for different aspects in three different files named `a.txt`, `b.txt` and `c.txt`.

- The text file `a.txt` has information about the Server ID and Server Name. The first line contains the Server ID, and the second line contains the Server Name. The third line again contains the next Server ID and so on. (i.e. There might be empty
space between lines which you don't have to consider.)

- The text file `b.txt` contains information about the Server runtime in hours. Each line contains information in the format `Server was running for = x_y hours`, where `x` denotes the hours the server was running and `y` represents the Server ID.
There might be information regarding other server as well which you don't have to consider if it not necessary.

- The text file `c.txt` has records about the cost per hour for each server. Every line contains information in the format `Server z's per hour running cost = w`, where `z` represents the Server ID and `w` is the cost per hour for that server.
There might be information regarding other server as well which you don't have to consider if it not necessary.

You are given the task to write a Python function that will read those txt files and create a consolidated pandas DataFrame containing SERVER_ID, SERVER_NAME, TOTAL_SERVER_RUNTIME, TOTAL_COST.

**Function Signature:** 

```python
def server_info_to_df() -> pd.DataFrame:
```

**Input:** 

- No input is required for this function. However, it will read data from text files `a.txt`, `b.txt` and `c.txt`.

**Output:** 

- The function should return a pandas DataFrame object.
- The DataFrame should contain the following columns:
    - SERVER_ID: The ID for each server. 
    - SERVER_NAME: The name for each server.
    - TOTAL_SERVER_RUNTIME: The total number of hours each server was running.
    - TOTAL_COST: The total cost for running each server.
 
### Example

Notice: Consider having the required `a.txt`, `b.txt` and `c.txt` files in the same directory where you are running your python script.

**Call**
```python
df = server_info_to_df()
print(df)
```

**Output**
```python
   SERVER_ID SERVER_NAME  TOTAL_SERVER_RUNTIME  TOTAL_COST
0          1         abc                    16         40.0
1          2         dfg                    25        100.0
2          3         efg                     3         69.0
```