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
i\  vowel -> ih
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
#### 擬增加音素 Phonemes to be added
```
yw semivowel
```
### 聲母 Initials
|#|拼音 Pinyin|現行 Current|建議 Suggestion |備注 Note
|-|-|-|-|-|
|b|**p**|**b**|*多數人讀成 mostly read as* /b/ `b`
|p|**ph**|**p**|
|m|**m**|**m**|
|f|**f**|**f**|
|d|**t**|**d**|*多數人讀成 mostly read as* /d/ `d`
|t|**th**|**t**|
|n|**n**|**n**|
|l|**l**|**l**|
|g|**k**|**g**|*多數人讀成 mostly read as* /g/ `g`
|k|**kh**|**k**|
|h|**x**|**h**|*多數人讀成 mostly read as* /h/ `h`
|j|**ts&#92;** |**j**|*多數人讀成 mostly read as* /dʑ/ `dz\ `
|q|**ts&#92;h**|**q**
|x|**s&#92;** |**x**
|zh|**ts&#96;**|**zh**|*多數人讀成 mostly read as* /dʒ/ `dZ`
|ch|**ts&#96;h**|**ch**|*多數人讀成 mostly read as* /tʃʰ/ `tSh`
|sh|**s&#96;**|**sh**|*多數人讀成 mostly read as* /ʃ/ `S`
|r|**z&#96;**|**r**|*多數人讀成 mostly read as* /ʒ/ `Z`
|z|**ts**|**z**|*多數人讀成 mostly read as*/dz/ `dz`
|c|**tsh**|**c**
|s|**s**|**s**
|y|**j**|**y**
|w|**w**|**w**
### 韻母 Finals
|#|拼音 Pinyin|現行 Current|建議 Suggestion |備注 Note
|-|-|-|-|-|
|a|**a**|**a**
|ia|**ia**|y a|*介音應拆分 should be split as noticed*
|ua|**ua**|w a|*介音應拆分 should be split as noticed*
|o|**o**|**o**
|io|**iAU**|y o|
|uo|**uo**|w o|*介音應拆分 should be split as noticed*
|e|**7**|**e**
|ie|**ie**|y **eh**|*介音應拆分 should be split as noticed*
|üe|**yE**|**yw** eh|*介音應拆分；真實發音仍是 should be split and read as* /ɥe/ `H e`
|i|**i**|**i**
|(zh/ch/sh/r)i|**i&#96;**|**ih**|*不應與下一音素區分 Not necessarily distinguished with below*
|(z/c/s)i|**i&#92;**|ih
|u|**u**|**u**
|ü|**y**|**yu**
|ai|a **:\i**|a y
|iai|ia :\i|y a y
|uai|ua :\i|w a y
|ei|**e** :\i|eh y
|ui|**ue** :\i|u y|*貼近真實發音 cater to authentic pronunciation* /uɪ/
|ao|**AU**|a w|*尾音應拆分；貼近真實發音 split and cater to authentic pronunciation* /aʊ/
|iao|iAU|y a w|*介尾音應拆分 should be split as noticed*
|ou|**@U**|o w|*尾音應拆分；貼近真實發音 split and cater to authentic pronunciation* /oʊ/
|iu|**i@U**|i w|*貼近真實發音 cater to authentic pronunciation* /iʊ/
|an|a **:n**|a n
|ian|**iE** :n|y eh n|*介音應拆分；真實發音仍是 actually read as* /ien/ `j e n`
|uan|ua :n|w a n|介音應拆分
|üan|**y{**:n|yw eh n|*介音應拆分；真實發音仍是 actually read as* /ɥen/ `H e n`
|en|**@** :n|**ex** n
|in|i :n|i n
|un|**u@** :n|u n|*貼近真實發音 cater to authentic pronunciation* /un/
|ün|yE :n|yu n|*正確發音是 actually read as* /yn/
|ang|**A N**|a **ng**|*正確發音是 actually read as* /aŋ/ `a N`
|iang|**iA** N|y a ng|*介音應拆分 should be split as noticed*
|uang|**uA** N|w a ng|*介音應拆分 should be split as noticed*
|eng|@ N|ex ng
|ing|i N|i ng
|ueng|u@ N|w ex ng|*介音應拆分 should be split as noticed*
|ong|**U** N|o ng|*常讀作 normally read as* /oŋ/ `o N`
|iong|**iU** N|y o ng|*介音應拆分 should be split as noticed*
|er|a **r&#92;&#96;**|ex **rr**|*正確發音是 actually read as* /ɚ/~/əɻ/ ``@` `` ~ ``@ r\` ``
### 總計 Total
|拼音 Pinyin|現行 Current|建議 Suggestion
|-|-|-
|63|55|35
### 附注 Notes
本工程中詞典也支持兒化音。  
The Mandarin dictionary of this repository also support rhotification.
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
## Examples 示例
1. 《七子之歌》之《香港》《九龍島》（慶祝香港回歸25周年，聞一多詞，本人曲）工程文件  
*Seven Sons' Song*, *Hong Kong* and *Kowloon Island* repository file, in memory of Hong Kong's handover for 25 years
## Credits 致謝
- [華侃如 先生 Sir Kan-ru "Sleepwalking" Hua](https://github.com/sleepwalking)
- [李迪克 先生 Sir Di-ke "Ddickky" Li](https://weibo.com/ddickky)
- [Dreamtonics](https://dreamtonics.com) [(Github)](https://github.com/dreamtonics)
- [平行四界](https://weibo.com/quadimension) [Quadimension](https://twitter.com/quad_stardust)
