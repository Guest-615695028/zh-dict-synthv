# zh-dict-synthv
## English
This repository is aimed at extending dialectal support for Chinese voicebanks of Synthesizer V Studio and reduce their phoneme list size to lower the time and space complexity of their respective resolution programs. 
## 中文
這一工程旨在增加Synthesizer V Studio（SV）漢語方言並縮小華語聲庫音素表並降低其解析程序之時空複雜度。既然SVS不區分VOCALOID（VD）區分的英語前l（**l**ot, VD作``l0``）與後l（ge**l**, VD作``l``），日語ha、he、ho（は、へ、ほ）的h（/h/）與hi（ひ）的h（/ç/），中文的`a`（**a**、**a**n、**a**i）與`A`（**a**u、**a**ng），`o`（**o**）與`U`（**o**ng），`i``（zh**i**、ch**i**、sh**i**、r**i**）、`i\`（z**i**、c**i**、s**i**），`e`（**ê**、**e**i、i**e**）、`E`（i**a**n、ü**e**）、`{`（ü**a**n）也不應細分。
ü
|#|拼音|現行(X-SAMPA)|建議|備注
|-|-|-|-|-|
|1|b|**p**|**b**|多數人讀成`b`
|2|P|**ph**|**p**|
|3|m|**m**|**m**|
|4|f|**f**|**f**|
|5|d|**t**|**d**|多數人讀成`d`
|6|t|**th**|**t**|
|7|n|**n**|**n**|
|8|l|**l**|**l**|
|9|g|**k**|**g**|多數人讀成`g`
|10|k|**kh**|**k**|
|11|h|**x**|**h**|多數人讀成`h`
|12|j|**ts&#92;** |**j**|多數人讀成`dz\ `
|13|q|**ts&#92;h**|**q**
|14|x|**s&#92;** |**x**
|15|zh|**ts&#96;**|**zh**|多數人讀成`dZ`
|16|ch|**ts&#96;h**|**ch**|多數人讀成`tSh`
|17|sh|**s&#96;**|**sh**|多數人讀成`S`
|18|r|**z&#96;**|**r**|多數人讀成`Z`
|19|z|**ts**|**z**
|20|c|**tsh**|**c**
|21|s|**s**|**s**
|22|y|**j**|**y**
|23|w|**w**|**w**
|24|a|**a**|**a**
|25|ia|**ia**|**y a**
|26|ua|**ua**|**w a**
|27|o|**o**|**o**
|28|uo|**uo**|**u o**
|29|e|**7**|**e**
|30|ie|**ie**|i** eh**
|31|üe|**yE**|yu eh
|32|i|**i**|**i**
|33|(zh/ch/sh/r)i|**i&#96;**|**ih**
|34|(z/c/s)i|**i&#92;**|ih
|35|u|**u**|**u**
|36|ü|**y**|**yu**
|37|ai|a **:\i**|a y
|38|uai|ua :\i|u a y
|39|ei|**e** :\i|eh y
|40|ui|**ue** :\i|u y
|41|ao|**AU**|a w
|42|iao|**iAU**|i a w
|43|ou|**@U**|o w
|44|iu|**i@U**|i o w
|45|an|a **:n**|a n
|46|ian|**iE** :n|i eh n
|47|uan|ua :n|u a n
|48|üan|**y{**:n|yu eh n
|49|en|**@** :n|**ex** n
|50|in|i :n|i n
|51|un|**u@** :n|u n
|52|ün|yE :n|yu n
|53|ang|**A N**|a **ng**
|54|iang|**iA** N|i a ng
|55|uang|**uA** N|u a ng
|56|eng|@ N|ex ng
|57|ing|i N|i ng
|58|ueng|u@ N|u ex ng
|59|ong|**U** N|o ng
|60|iong|**iU** N|i o ng
|61|er|a **r&#92;&#96;**|ex **rr**
|总计|61|55|37
