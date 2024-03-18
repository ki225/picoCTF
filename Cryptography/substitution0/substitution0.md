# solution
With the hint "Try a frequency attack. An online tool might help," I use the [Frequency Analysis Tool](https://wilsoa.github.io/gallery/frequency_analysis.html) on the web.

First, input the text from the source file. 
<img width="1440" alt="截圖 2024-03-19 凌晨12 11 19" src="https://github.com/ki225/picoCTF/assets/123147937/7cf9c169-ebd3-490f-8f7a-cf8465cc5f37">

Second, we start to substitute the text. I substitute the word "picoctf" first.
It said "The letters E, T, A and O are the most common in English," so I changed "f" into "e" because "f" has highest frequency.

<img width="1440" alt="截圖 2024-03-19 凌晨12 11 35" src="https://github.com/ki225/picoCTF/assets/123147937/6ccc1849-bc7b-47fd-b54b-7aa1025d1a6b">

Then I get the flag.
