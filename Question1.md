---
layout: default
title: Question One
---

<style>
body {
    -webkit-user-select: none;  /* Chrome, Safari and Opera */
    -moz-user-select: none;     /* Firefox */
    -ms-user-select: none;      /* IE and Edge */
    user-select: none;          /* standard syntax */
}
</style>
## Problem Statement: 
---
A team of `n` astronauts embarked on a journey to an unknown planet with `m` elephants and `p` tigers. They face an unexpected situation where their oxygen resources deplete significantly leaving them with only `M` units of oxygen. Each astronaut requires 5 units of oxygen daily, an elephant requires 10 units, and a tiger needs 8 units. Their machine was able to generate 10 units of oxygen every five days but was also wasting 20 units of oxygen every 12 hours. 

You have to write python code that will calculate the number of full days the spaceman and their animals would require in order to safely return to Earth given the number of spacemen, elephants, tigers, and the units of leftover oxygen.

**Function Signature** : 
```pyhton
def days_to_return(M: int, n: int, m: int, p: int) -> int:
```

**Input**: 
* The function accepts four parameters: 
    - An integer `M` (1 ≤ `M` ≤ 10000), representing the remaining units of oxygen.
    - An integer `n` (1 ≤ `n` ≤ 50), representing the number of astronauts.
    - An integer `m` (1 ≤ `m` ≤ 50), representing the number of elephants.
    - An integer `p` (1 ≤ `p` ≤ 50), representing the number of tigers.
* All parameters are separated by commas.

**Output**: 
* The function should return a single integer, the number of full days the team and their animals have to safely return to Earth.


---

### Example

**Input**: 
```days_to_return(2000, 5, 3, 5)```

**Output**: 
14


