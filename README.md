# zh-dict-synthv
## 説明 Description
這一工程旨在增加Synthesizer V Studio（SV）漢語方言並縮小華語聲庫音素表並降低其解析程序之時空複雜度。既然SVS不區分VOCALOID（VD）區分的英語前L（**l**ot, VD作``l0``）與後L（ge**l**, VD作``l``）、送氣塞音與不送氣塞音，日語ha、he、ho（は、へ、ほ）的h（/h/）與hi（ひ）的h（/ç/），中文的`a`（**a**、**a**n、**a**i）與`A`（**a**u、**a**ng），`o`（**o**）與`U`（**o**ng），``i` ``（zh**i**、ch**i**、sh**i**、r**i**）與`i\ `（z**i**、c**i**、s**i**），`e`（**ê**、**e**i、i**e**）、`E`（i**a**n、ü**e**）與`{`（ü**a**n）、首尾i音、n音也不應細分。

This repository is aimed at extending dialectal support for Chinese voicebanks of Synthesizer V Studio (SVS) and reduce their phoneme list size to lower the time and space complexity of their respective resolution programs. Since SVS does not tell initial L's (`l0` in VOCALOID) apart from the final L's (`l` in VOCALOID), aspired explosives apart from unaspired ones (distinguished in VOCALOID) in English, along with the H's in *ha*, *he*, *ho* (all /h/) and *hi* (/ç/), `a` (**a**, **a**n and **a**i) and `A`, (**a**u and **a**ng)，`o` (**o**) and `U` (**o**ng), ``i` `` (zh**i**, ch**i**, sh**i** and r**i**) and `i\ ` (z**i**, c**i** and s**i**), `e` (**ê**, **e**i and i**e**) and `E` (i**a**n and ü**e**) and `{` (ü**a**n), as well as initial and final *i*'s and *n*'s shall not be differentiated.

## 華語方面列表 List for Mandarin
### 聲母 Initials
|#|拼音 Pinyin|現行 Current (X-SAMPA)|建議 Suggestion |備注 Note
|-|-|-|-|-|
|1|b|**p**|**b**|*多數人讀成 mostly read as* /b/ `b`
|2|p|**ph**|**p**|
|3|m|**m**|**m**|
|4|f|**f**|**f**|
|5|d|**t**|**d**|*多數人讀成 mostly read as* /d/ `d`
|6|t|**th**|**t**|
|7|n|**n**|**n**|
|8|l|**l**|**l**|
|9|g|**k**|**g**|*多數人讀成 mostly read as* /g/ `g`
|10|k|**kh**|**k**|
|11|h|**x**|**h**|*多數人讀成 mostly read as* /h/ `h`
|12|j|**ts&#92;** |**j**|*多數人讀成 mostly read as* /dʑ/ `dz\ `
|13|q|**ts&#92;h**|**q**
|14|x|**s&#92;** |**x**
|15|zh|**ts&#96;**|**zh**|*多數人讀成 mostly read as* /dʒ/ `dZ`
|16|ch|**ts&#96;h**|**ch**|*多數人讀成 mostly read as* /tʃʰ/ `tSh`
|17|sh|**s&#96;**|**sh**|*多數人讀成 mostly read as* /ʃ/ `S`
|18|r|**z&#96;**|**r**|*多數人讀成 mostly read as* /ʒ/ `Z`
|19|z|**ts**|**z**|*多數人讀成 mostly read as*/dz/ `dz`
|20|c|**tsh**|**c**
|21|s|**s**|**s**
|22|y|**j**|**y**
|23|w|**w**|**w**
### 韻母 Finals
|#|拼音 Pinyin|現行 Current (X-SAMPA)|建議 Suggestion |備注 Note
|-|-|-|-|-|
|24|a|**a**|**a**
|25|ia|**ia**|**y a**|*介音應拆分 should be split as noticed*
|26|ua|**ua**|**w a**|*介音應拆分 should be split as noticed*
|27|o|**o**|**o**
|28|uo|**uo**|**w o**|*介音應拆分 should be split as noticed*
|29|e|**7**|**e**
|30|ie|**ie**|y** eh**|*介音應拆分 should be split as noticed*
|31|üe|**yE**|yu eh|*介音應拆分；真實發音仍是 should be split and read as* /ɥe/ `H e`
|32|i|**i**|**i**
|33|(zh/ch/sh/r)i|**i&#96;**|**ih**|*不應與下一音素區分 Not necessarily distinguished with below*
|34|(z/c/s)i|**i&#92;**|ih
|35|u|**u**|**u**
|36|ü|**y**|**yu**
|37|ai|a **:\i**|a y
|38|uai|ua :\i|u a y
|39|ei|**e** :\i|eh y
|40|ui|**ue** :\i|u y|*貼近真實發音 cater to authentic pronunciation* /uɪ/
|41|ao|**AU**|a w|*尾音應拆分；貼近真實發音 split and cater to authentic pronunciation* /aʊ/
|42|iao|**iAU**|y a w|*介尾音應拆分 should be split as noticed*
|43|ou|**@U**|o w|*尾音應拆分；貼近真實發音 split and cater to authentic pronunciation* /oʊ/
|44|iu|**i@U**|y o w|*貼近真實發音 cater to authentic pronunciation* /iʊ/
|45|an|a **:n**|a n
|46|ian|**iE** :n|y eh n|*介音應拆分；真實發音仍是 actually read as* /ien/ `j e n`
|47|uan|ua :n|w a n|介音應拆分
|48|üan|**y{**:n|yu eh n|*介音應拆分；真實發音仍是 actually read as* /ɥen/ `H e n`
|49|en|**@** :n|**ex** n
|50|in|i :n|i n
|51|un|**u@** :n|u n|*貼近真實發音 cater to authentic pronunciation* /un/
|52|ün|yE :n|yu n|*真實發音是 actually read as* /yn/
|53|ang|**A N**|a **ng**|*真實發音是 actually read as* /aŋ/ `a N`
|54|iang|**iA** N|y a ng|*介音應拆分 should be split as noticed*
|55|uang|**uA** N|w a ng|*介音應拆分 should be split as noticed*
|56|eng|@ N|ex ng
|57|ing|i N|i ng
|58|ueng|u@ N|w ex ng|*介音應拆分 should be split as noticed*
|59|ong|**U** N|o ng|*常讀作 normally read as* /oŋ/ `o N`
|60|iong|**iU** N|y o ng|*介音應拆分 should be split as noticed*
|61|er|a **r&#92;&#96;**|ex **rr**|*真實發音是 actually read as* /ɚ/~/əɻ/ ``@` `` ~ ``@ r\` ``
### 總計 Total
|拼音 Pinyin|現行 Current (X-SAMPA)|建議 Suggestion
|-|-|-|
|61|55|38
## Credits 致謝
- [華侃如 先生 Sir Kanru Hua](https://github.com/sleepwalking)
- [Dreamtonics](https://dreamtonics.com) [Github](https://github.com/dreamtonics)
