From the source file, you can find the text "picoCTF{gvswwmrkxlivyfmgsrhnrisegl}," but this is not the answer.

<img width="758" alt="截圖 2024-03-19 凌晨1 06 32" src="https://github.com/ki225/picoCTF/assets/123147937/4633cf34-8796-45b9-ad0d-ed526c2dbb11">

The hint give us the link for caesar cipher, but I can not reach it. So, I search on the web.

# Caesar Cipher

It is a substitution cipher that shifts letters in a message to make it unreadable if intercepted.

# solve
I use [cryptii](https://cryptii.com/pipes/caesar-cipher) to decode "gvswwmrkxlivyfmgsrhnrisegl". The default result seems not the correct one, so we keep changing the shift. 

<img width="1552" alt="截圖 2024-03-19 凌晨1 13 45" src="https://github.com/ki225/picoCTF/assets/123147937/7a9ba558-7c55-4679-9edb-0b422ee8208a">

Finally, we found a string seems to be a sentence. This is th flag.

<img width="1552" alt="截圖 2024-03-19 凌晨1 14 53" src="https://github.com/ki225/picoCTF/assets/123147937/b011d7f2-cc27-4a55-bac7-5d89c97eaf79">

ps. crossing the rubicon is a history event !
<img width="1552" alt="截圖 2024-03-19 凌晨1 16 33" src="https://github.com/ki225/picoCTF/assets/123147937/5d2ec36f-21a3-4183-86af-b148134ca454">
