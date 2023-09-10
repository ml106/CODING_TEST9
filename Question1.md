---
layout: default
title: Question One
---



## Problem Statement: 

A computer lab has `n` computers and `m` Ethernet cables. Each computer needs to be linked to another computer with a network cable for network connectivity in order to function properly. On day `p`, `s` computers stopped functioning due to a network problem, with an estimated repair cost of `d` dollars each. On top of that, there will be a daily energy loss of `e` dollars if the computers are not working. The lab has only `C` dollars left for repairing the computers.

Write a python function that will calculate how many full days the lab can keep its computers working with the remaining dollars. 

**Function Signature:** 
```python
    def repair_computers(C: int, n: int, m: int, p: int, s: int, d: int, e: int) -> int:
```

**Input**: 
* The function accepts seven parameters: 
    - An integer `C` (1 ≤ `C` ≤ 10000), representing the remaining dollars.
    - An integer `n` (1 ≤ `n` ≤ 50), representing the number of computers.
    - An integer `m` (1 ≤ `m` ≤ 50), representing the number of Ethernet cables.
    - An integer `p` (1 ≤ `p` ≤ 50), representing the day when computers stopped functioning.
    - An integer `s` (1 ≤ `s` ≤ `n`), representing the number of computers that stopped functioning.
    - An integer `d` (1 ≤ `d` ≤ 100), representing the repair cost for each malfunctioned computer.
    - An integer `e` (1 ≤ `e` ≤ 100), representing the daily energy loss in dollars if the computers are not working.
* All parameters are separated by commas.

**Output**: 
* The function should return a single integer, the number of full days the lab can keep its computers working with the remaining dollars.

---

### Example

**Input**: 
```repair_computers(5000, 10, 8, 3, 2, 50, 20)```

**Output**: 
245