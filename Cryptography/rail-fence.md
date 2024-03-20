In the discription, we can find a link to [Rail fence cipher](https://en.wikipedia.org/wiki/Rail_fence_cipher).

Here are the examples for this method.

## Encryption
If the text is "Hello_word", and the key=3:
```
H      o       r
  e   l  _   o   l
    l      w       d
```

We can know that the key represent the rails number. Then we read these words line in line:
```
Hor+el_ol+lwd
```
So, the encryption is `Horel_ollwd`

## Decryption
If the text is "Horel_ollwd", and the key=3:

```
H      o       r
  e   l  _   o   l
    l      w       d
```

We need to make the rail matrix first:
```
*       *       *
  *   *   *   *   *
    *       *       *
```
Then we fill the star matrix line and line.
```
*       *       *      <------- Hor
  *   *   *   *   *    <------- el_ol
    *       *       *  <------- lwd
```
Finally, we read this matrix by the original way.

# solve
```python
def dencryptRailFence(text,key):
    rail = [['' for i in range(len(text))] for j in range(key)] # init
    
    dir_down = None
    row, col = 0, 0
    # make the rail matrix
    for i in range(len(text)):
        if row == 0:
            dir_down = True
        elif row == key - 1:
            dir_down = False

        rail[row][col] = '*'
        col += 1
        if dir_down:
            row += 1
        else:
            row -= 1
    
    # fill the matrix
    text_i=0
    for i in range(key):
        for j in range(len(text)):
            if rail[i][j] == '*':
                rail[i][j] = text[text_i]
                text_i += 1
            
    result = []
    row, col = 0, 0
    for i in range(len(text)):
        if row == 0:
            dir_down = True
        elif row == key - 1:
            dir_down = False
            
        result.append(rail[row][col])
        col += 1
        if dir_down:
            row += 1
        else:
            row -= 1
    return "".join(result)
    

s = "Ta _7N6D8Dhlg:W3D_H3C31N__387ef sHR053F38N43DFD i33___N6"

print(dencryptRailFence(s, 4))
```
The return is
```
The flag is: WH3R3_D035_7H3_F3NC3_8361N_4ND_3ND_83F6D8D7
```
