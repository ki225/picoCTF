There are countless files in folder "files" so we cannot check them one by one. The checknum is equal to the SHA-256 number in target file.
```sh=
sha256sum files/* | grep 5848768e56185707f76c1d74f34f4e03fb0573ecc1ca7b11238007226654bcda
```
You will get the file name called `8eee7195`.

Decrypt it.
```sh=
./decrypt.sh files/8eee7195
```

picoCTF{trust_but_verify_8eee7195}

<img width="682" alt="截圖 2024-07-20 下午2 59 30" src="https://github.com/user-attachments/assets/11c92d97-0ec5-42fb-9ce3-2fa17e88169b">y
