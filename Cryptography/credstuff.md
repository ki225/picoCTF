First, I wrote a code for finding the target name and corresponding pwd.

Remember to add "\n" in the end of the name, or you will find nothing.

```python
f = open('passwords.txt', 'r')
f2 = open('usernames.txt', 'r')

i=1
while True:
    print(i)
    username = f2.readline()
    password = f.readline()
    if username == "cultiris\n":
        print(password)
    i+=1
    if i>=506:
        break
    else:
        continue
```

Here is the result of the code. I found that picoCTF is "cvpbPGS", so I decide to use rotation method to decode them.

<img width="1552" alt="截圖 2024-03-20 上午9 36 50" src="https://github.com/ki225/picoCTF/assets/123147937/f711dd94-3d77-48e2-b56f-78dc2fe54246">

The flag is there!

<img width="1552" alt="截圖 2024-03-20 上午9 38 30" src="https://github.com/ki225/picoCTF/assets/123147937/a4bed49e-ba2d-4c55-aa1b-b2dbb22985b5">
