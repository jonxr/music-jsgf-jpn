# Japanese Context Free Grammar w/ Java Speech Grammar Format

_Sample Use Case: Voice Command Natural Language Processing for Music Automation Artificial Intelligence_

@author Jon Reyes © All Rights Reserved.
	
```
#JSGF V1.0 utf-8 en;
grammar music_play;

public <music_play> =
<filter> <action> <request>;
```
### STRUCTURE
English is structured by subject verb object 

> I want <request_verb> to <unk> listen <action_verb> to <unk> the beatles <filter> 
(music object noun)

> <request> <action> <filter> english usage

In contrast, Japanese is structured by subject object verb.

### SAMPLE UTTERANCE

**EXAMPLE 1**

Japanese: 米津玄師プレイして!

> 米津玄師 <artist> Kenshi Yonezu
> プレイ <action> play action verb
> して <request> command verb : do this

English: Play Kenshi Yonezu!

**EXAMPLE 2**

Japanese: 現星野の恋聞きたい!　
Japanese: 現星野の恋聞くことしたい！

> 現星野 <artist> Gen Hoshino
> 恋 <song> Koi (Love)
> 聞　| 聞く <action> listen action verb
> きたい | ことしたい <request> desire verb : i want to do this

English: I want to listen to Gen Hoshino's Koi!

```
<request> = 
(can you | (して | してもいい | こと出来る) | 
(i want | お願い | くれ | ください | ことしたい　| きたい）;
```

### LIMITATIONS / SCALABILITY
The scalability limitations that could be improved upon specifically for the Japanese Language	includes consideration for intermediate particles (subject: ga | が; direct object: を; possession/description: no | の) and different suffixes for different modes of speech (i.e. casual: タメ語, polite / honorific: 丁寧語,　敬語, 尊敬語, 謙譲語)

We will mostly assume casual in the use case context of the simplest voice commands 
for Google Assistant, Microsoft Cortana, Apple Siri, etc. in auto starting a music player like Spotify.
		
```
<action> = 
(put on | して) | (play | プレイ） | (listen | 聞く | 聞);

<filter> = 
<artist> | <song> | <genre> | <album>;

<artist> =
beatles |
radio head |
cake |
pink floyd |
(米津玄師 | Kenshi Yonezu) |
(フレデリック | Frederic) |
(星野源 | Gen Hoshino);

<song> =
confortably numb |
paranoid android |
let it be |
hey jude |
(レモン | Lemon) |
(オドループ | oddloop) |
(恋 | Koi);

<genre> = 
(jazz | ジャズ) | (rock | ロック) | (pop | ポップ);

<album> = 
ummagumma | 
the wall | 
ok computer | 
let it be | 
hey jude |
(レモン | Lemon) |
(オドループ | oddloop) |
(恋 | Koi);
```

### TRANSLITERATION
For Japanese, English songs are mostly taken as is, but could be converted to Katakana as transliteration of foreign words (i.e cake -> ケーキ kekki). Other Japanese music examples were also added.
