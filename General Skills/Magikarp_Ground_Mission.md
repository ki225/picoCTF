Fisrt, use the command to connect to the server.
```
ssh ctf-player@venus.picoctf.net -p xxxxx
```
Then input the password.

If you see `ctf-player@pico-chall$` on the left hand side, it represents that you connect successfully. 
<img width="745" alt="截圖 2024-03-23 下午4 50 21" src="https://github.com/ki225/picoCTF/assets/123147937/07e2b1cf-1684-4fc3-b393-1c42b8b64849">

list the file in your dir, and you will find two txt files.
```
ls
```
```
1of3.flag.txt  instructions-to-2of3.txt.
```
Just print the information in the txt file, you will get the first part of flag and some info. In the second file, it says:
```
Next, go to the root of all things, more succinctly `/`
```
However, we cannot jump to root directory.
```sh
ctf-player@pico-chall$ cd /root
-bash: cd: /root: Permission denied
```
I tried to list all the things in this dir, and I found something.
```
ls -a
```

<img width="745" alt="截圖 2024-03-23 下午4 54 45" src="https://github.com/ki225/picoCTF/assets/123147937/5ca9698c-6b9f-4059-b661-769ee92effe2">

Just keep doing the following commands, you will find the second part and the third part of the flag.
<img width="745" alt="截圖 2024-03-23 下午4 55 07" src="https://github.com/ki225/picoCTF/assets/123147937/45a9e18d-d880-4f11-a313-5e2536671286">

<img width="745" alt="截圖 2024-03-23 下午4 55 27" src="https://github.com/ki225/picoCTF/assets/123147937/f786ca5a-8da7-4e66-aae1-0f29ab634d10">

