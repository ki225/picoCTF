First, download the files from the website, then you will get the .zip file.

<img width="642" alt="截圖 2024-04-01 中午12 19 11" src="https://github.com/ki225/picoCTF/assets/123147937/d31300ed-f7d9-445e-9f8d-938717bf5181">

Use the command below to unzip it. You will get a file named "drop in". If you are MAC user and do not find the file have been unzipped automatically and no directory called "drop in," you can try to use Linux os.
```shell
unzip challenge.zip
```
<img width="519" alt="截圖 2024-04-01 中午12 25 56" src="https://github.com/ki225/picoCTF/assets/123147937/14ea95c2-2704-4db2-87fb-054de93afc22">


If you cat the information from the .txt file, you will only see :

<img width="758" alt="截圖 2024-04-01 中午12 36 32" src="https://github.com/ki225/picoCTF/assets/123147937/7cb830a0-71bd-466c-aff4-0471f16979c1">

or
```
350 63 353 198 114 369 346 184 202 322 94 235 114 110 185 188 225 212 366 374 261 213 %
```

The hint says "Version control can help you recover files if you change or lose them!" so I decided to use git. Let's check out the version.
```shell
git --version
```
<img width="519" alt="截圖 2024-04-01 中午12 27 06" src="https://github.com/ki225/picoCTF/assets/123147937/9dc7d510-60e2-4c74-a107-0b8525039b08">

Now we know that we already have the git. Let's initialize the git.

<img width="623" alt="截圖 2024-04-01 中午12 28 04" src="https://github.com/ki225/picoCTF/assets/123147937/afaf94df-f04f-4c0a-bcc5-688e256a89b8">

More about how to use the git command, you can see this [website](https://primer.picoctf.org/#_git_version_control).

To see past 'save points' and their commit IDs for tracing back, you can use the command :
```shell
git log
```
<img width="623" alt="截圖 2024-04-01 中午12 30 14" src="https://github.com/ki225/picoCTF/assets/123147937/6a486619-48ca-4e98-ae53-501e230da752">

The command below is to go to a past commit.
```shell
git checkout PAST_COMMIT_ID
```
BTW this command can also let you switch to other branch, the way to use is the command `git checkout ANOTHER_BRANCH_NAME`.


<img width="623" alt="截圖 2024-04-01 中午12 33 16" src="https://github.com/ki225/picoCTF/assets/123147937/18ef0e2b-2d72-4bc7-a9c0-70501c10a149">

Because the this commit is for creating the flag, we go to it.

<img width="623" alt="截圖 2024-04-01 中午12 34 01" src="https://github.com/ki225/picoCTF/assets/123147937/18dc62b0-11e1-414b-abb8-950b3e34945b">

Finally, we print the infomation in this file and get the flag.

<img width="623" alt="截圖 2024-04-01 中午12 34 24" src="https://github.com/ki225/picoCTF/assets/123147937/c5706039-3f72-4c4b-8724-4f461e4da761">
