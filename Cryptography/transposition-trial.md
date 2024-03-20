The order of the answer is incorrect, but we can find the rule:

In the article, it says "every block of 3 got scrambled around!", so we target at every 3 blocks:
- The words "The" become "heT", the order is 231
- The sentence " flag " becomes "fl g a", the order is 231231


Therefore, I wrote a python code
```python
s = "heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V091B0AE}2"

for i in range(0, len(s), 3):
    print(s[i+2]+s[i]+s[i+1], end="")
```
