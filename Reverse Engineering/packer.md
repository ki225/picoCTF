First, I try to cat content in this, but it does not work. Then I check the file's format by the following command.
```
file out
```
result:
```
out: ELF 64-bit LSB executable, x86-64, version 1 (GNU/Linux), statically linked, no section header
```
ELF is a common standard file format for executable files, object code, shared libraries, and core dumps. We need to decrease the range of information. I found [this website](https://www.iblue.team/malware-analysis/identifying-upx-packed-elf-decompressing-fixing-and-analysing-linux-malware) which topic is about "Identifying UPX packed ELF" so that I guess it is related to upx.
```
string out
```
In the output, the string "UPX!" appears two times in the end. We guess that it is an UPX file. The output also show `$Info: This file is packed with the UPX executable packer http://upx.sf.net $ $Id: UPX 3.95 Copyright (C) 1996-2018 the UPX Team. All Rights Reserved. $` in the middle of the file.

In the [website](http://upx.sf.net) output gave us, we know that upx file typically compresses better than Zip, use UPX to decrease the size of your distribution, in other words, we can decompressed it. 

```
upx -d out
```
result:

<img width="640" alt="截圖 2024-07-21 中午12 51 33" src="https://github.com/user-attachments/assets/16a3d51e-96c2-4e5f-a160-5b287f2e9625">

Let check the file's type now.

<img width="640" alt="截圖 2024-07-21 中午12 51 55" src="https://github.com/user-attachments/assets/699a3469-1ca1-4beb-bdaa-4494fbe63e68">

Use the following commands to print the content. It should contains different and more readable information.
```
strings out
```
<img width="640" alt="截圖 2024-07-21 中午12 53 05" src="https://github.com/user-attachments/assets/295582e4-9137-49b3-8b44-cd68b3613b0a">

Try to get flag by grepping keywords.

<img width="640" alt="截圖 2024-07-21 下午1 02 22" src="https://github.com/user-attachments/assets/1c50ed0b-a916-4fa0-9d89-6e8e9770c11f">

Decode these.

<img width="1021" alt="截圖 2024-07-21 下午1 06 48" src="https://github.com/user-attachments/assets/3cf1b826-e525-4630-be30-583f4e54d3f1">
