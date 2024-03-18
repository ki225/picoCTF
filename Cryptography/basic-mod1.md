This is the number series from the file.

<img width="758" alt="截圖 2024-03-19 凌晨1 35 59" src="https://github.com/ki225/picoCTF/assets/123147937/3c5b6780-dc71-40e7-87aa-41d4a2523f76">

After mod 37 from [Modulo Cipher](https://www.dcode.fr/modulo-cipher), we get a new series : 17 26 20 13 3 36 13 36 17 26 20 13 3 36 0 3 3 27 33 4 2 28

<img width="1552" alt="截圖 2024-03-19 凌晨1 36 37" src="https://github.com/ki225/picoCTF/assets/123147937/be972915-5ba7-4a80-8d2c-603e2550a2d8">

Because the hint says "0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore," I wrote a python code for decoding.
```python
# the array for 17 26 20 13 3 36 13 36 17 26 20 13 3 36 0 3 3 27 33 4 2 28
array = [17, 26, 20, 13, 3, 36, 13, 36, 17, 26, 20, 13, 3, 36, 0, 3, 3, 27, 33, 4, 2, 28]

# change the num to word or number
#  0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.
def num_to_word(num):
    if num < 26:
        return chr(num + 65)
    elif num < 36:
        return str(num - 26)
    elif num == 36:
        return "_"
    else:
        return "?"
    

for i in array:
    print(num_to_word(i), end="")
```
Here is the flag.

<img width="1552" alt="截圖 2024-03-19 凌晨1 39 05" src="https://github.com/ki225/picoCTF/assets/123147937/c7c0c5a8-a9b3-4641-a3ee-56fbc82e8a81">
