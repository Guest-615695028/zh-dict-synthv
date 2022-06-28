# zh-dict-synthv
## 説明 Description
這一工程旨在增加Synthesizer V Studio（SV）漢語方言並縮小華語聲庫音素表並降低其解析程序之時空複雜度。  
This repository is aimed at extending dialectal support for Chinese voicebanks of Synthesizer V Studio (SVS) and reduce their phoneme list size to lower the time and space complexity of their respective resolution programs.
### 既定事實 Accomplished Facts
1. SVS不區分VOCALOID區分的英語前L（**l**ot, ``l0``）與後L（ge**l**, ``l``）、送氣塞音與不送氣塞音；  
SVS does not tell initial L's (`l0` in VOCALOID) apart from the final L's (`l` in VOCALOID), aspired explosives apart from unaspired ones (distinguished in VOCALOID) in English;
2. SVS不區分日語ha、he、ho（は、へ、ほ）的h（/h/）與hi（ひ）的h（/ç/）；  
SVS does not distinguish the H's in *ha*, *he*, *ho* (all /h/) and *hi* (/ç/);
3. SVS誤將中文io并入iao；  
SVS mistakes Chinese *io* as *iao*;
4. SVS中文音素方案難以獨立理解、記憶，不利於跨語種調教。  
SVS phoneme system for Chinese (`mandarin-xsampa`) is difficult to comprehend and memorize without the assistance of Pinyin, which results in a disadvantage of translingual synthesis.
5. 自1958年出版以來，中華人民共和國《[漢語拼音方案](https://zh.wikipedia.org/wiki/%E6%B1%89%E8%AF%AD%E6%8B%BC%E9%9F%B3)》從未將漢語拼音與國際音標音值（表徵爲X-SAMPA）對應，且現有對應關係頗存爭議。  
[Scheme for the Chinese Phonetic Alphabet](https://en.wikipedia.org/wiki/Pinyin) has not been mapping Pinyin to IPA (then X-SAMPA) ever since its publication by the Chinese Government in 1958, with their corrrespondence still controversial.

## 華語方面列表 List for Mandarin
### 音素 Phonemes
```
a   vowel -> a
A   vowel *
o   vowel -> o
@   vowel -> e
e   vowel -> eh
7   vowel -> ex
U   vowel *
u   vowel -> u
i   vowel -> i
i\  vowel -> i
i`  vowel *
y   vowel -> yu
AU  diphthong *
@U  diphthong *
ia  diphthong *
iA  diphthong *
iAU diphthong *
ie  diphthong *
iE  diphthong *
iU  diphthong *
i@U diphthong *
y{  diphthong *
yE  diphthong *
ua  diphthong *
uA  diphthong *
u@  diphthong *
ue  diphthong *
uo  diphthong *
:\i coda *
r\` coda -> rr
:n  coda *
N   coda -> ng
p   stop -> b
ph  stop -> p
t   stop -> d
th  stop -> t
k   stop -> g
kh  stop -> k
ts\  affricate -> j
ts   affricate -> z
tsh  affricate -> c
ts`  affricate -> zh
ts`h affricate -> ch
x    aspirate *actually h* -> h
f    fricative -> f
s    fricative -> s
s`   fricative -> sh
ts\h fricative *actually affricate* -> q
s\   fricative -> x
m   nasal -> m
n   nasal -> n
l   liquid -> l
z`  semivowel -> r
w   semivowel -> w
j   semivowel -> y
pau silence *
sil silence -> sil
```

`*` 擬淘汰 To be eliminated
### 聲母 Initials
|#|拼音 Pinyin|現行 Current|建議 Suggestion |備注 Note
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
|#|拼音 Pinyin|現行 Current|建議 Suggestion |備注 Note
|-|-|-|-|-|
|24|a|**a**|**a**
|25|ia|**ia**|y a|*介音應拆分 should be split as noticed*
|26|ua|**ua**|w a|*介音應拆分 should be split as noticed*
|27|o|**o**|**o**
|28|io|**iAU**|y o|
|29|uo|**uo**|w o|*介音應拆分 should be split as noticed*
|30|e|**7**|**e**
|31|ie|**ie**|y **eh**|*介音應拆分 should be split as noticed*
|32|üe|**yE**|yu eh|*介音應拆分；真實發音仍是 should be split and read as* /ɥe/ `H e`
|33|i|**i**|**i**
|34|(zh/ch/sh/r)i|**i&#96;**|**ih**|*不應與下一音素區分 Not necessarily distinguished with below*
|35|(z/c/s)i|**i&#92;**|ih
|36|u|**u**|**u**
|37|ü|**y**|**yu**
|38|ai|a **:\i**|a y
|39|iai|ia :\i|y a y
|38|uai|ua :\i|w a y
|39|ei|**e** :\i|eh y
|40|ui|**ue** :\i|u y|*貼近真實發音 cater to authentic pronunciation* /uɪ/
|41|ao|**AU**|a w|*尾音應拆分；貼近真實發音 split and cater to authentic pronunciation* /aʊ/
|42|iao|iAU|y a w|*介尾音應拆分 should be split as noticed*
|43|ou|**@U**|o w|*尾音應拆分；貼近真實發音 split and cater to authentic pronunciation* /oʊ/
|44|iu|**i@U**|i w|*貼近真實發音 cater to authentic pronunciation* /iʊ/
|45|an|a **:n**|a n
|46|ian|**iE** :n|y eh n|*介音應拆分；真實發音仍是 actually read as* /ien/ `j e n`
|47|uan|ua :n|w a n|介音應拆分
|48|üan|**y{**:n|yu eh n|*介音應拆分；真實發音仍是 actually read as* /ɥen/ `H e n`
|49|en|**@** :n|**ex** n
|50|in|i :n|i n
|51|un|**u@** :n|u n|*貼近真實發音 cater to authentic pronunciation* /un/
|52|ün|yE :n|yu n|*正確發音是 actually read as* /yn/
|53|ang|**A N**|a **ng**|*正確發音是 actually read as* /aŋ/ `a N`
|54|iang|**iA** N|y a ng|*介音應拆分 should be split as noticed*
|55|uang|**uA** N|w a ng|*介音應拆分 should be split as noticed*
|56|eng|@ N|ex ng
|57|ing|i N|i ng
|58|ueng|u@ N|w ex ng|*介音應拆分 should be split as noticed*
|59|ong|**U** N|o ng|*常讀作 normally read as* /oŋ/ `o N`
|60|iong|**iU** N|y o ng|*介音應拆分 should be split as noticed*
|61|er|a **r&#92;&#96;**|ex **rr**|*正確發音是 actually read as* /ɚ/~/əɻ/ ``@` `` ~ ``@ r\` ``
### 總計 Total
|拼音 Pinyin|現行 Current|建議 Suggestion
|-|-|-
|61|55|34
## 粵語方面列表 List for Cantonese
提供且僅提供合法音節組合。  
This repository provides and only provides legal syllabic combinations.
### 聲母 Initials
与華語對應相同（除`h`爲/h/而不是/x/；華語母語者也常以/h/代/x/），斜體見於《分韻撮要》及港鐵站名。
|1|2|3|4|5|
|-|-|-|-|-|
|b|p|m|f|-|
|d|t|n|-|l|
|g|k|h|ng|-|
|gw|kw|-|-|w|
|*zh*|*ch*|*sh*|-|-|
|z|c|s|-|y|
### 韻母 Finals
|medial|-|`j`|`w`|`m`|`n`|`N`|`p`|`t`|`k`|
|-|-|-|-|-|-|-|-|-|-|
|`a`|aa/a|aai|aau|aam|aan|aang|aap|aat|aak|
|`@`|-|ai|au|am|an|ang|ap|at|ak|
|`e`|e|ei|-|-|-|eng|-|-|ek|
|`i`|i|-|iu|im|in|ing|ip|it|ik|
|`o`|o|oi|ou|*om*|on|ong|*op*|ot|ok|
|`u`|u|ui|-|-|un|ung|-|ut|uk|
|`7`|oe|eoi|-|-|eon|oeng|-|eot|oek|
|`y`|yu|-|-|-|yun|-|-|yut|-
## Examples 案例
1. 《七子之歌》之《香港》《九龍島》（慶祝香港回歸25周年，聞一多詞，本人曲）工程文件
## Credits 致謝
- [華侃如 先生 Sir Kan-ru "Sleepwalking" Hua](https://github.com/sleepwalking)
- [李迪克 先生 Sir Di-ke "Ddickky" Li](https://weibo.com/ddickky)
- [Dreamtonics](https://dreamtonics.com) [Github](https://github.com/dreamtonics)
- [平行四界](https://weibo.com/quadimension) [Quadimension](https://twitter.com/quadimension)
