# fxaudio-tube-03
A dedicated page for reverse engineering the FXAudio Tube-03 preamp.

![image](img/schematic_front.png)


## Tubes
Comes with a 6K4 (EF95) Chinese vacuum tubes.

<img src="img/parts/tubes.jpg" height="300">

### Compatible Tubes
The compatible tubes found on the internet are:

6J1, 6ж1П, 6AK5, 6BC5, 403A/B, 5654, EF95, CV850, 6J2, 6ж2П, 6AS6, CV2522, CV4011, 6J3, 6ж3П, EF94, CV848, 6BC6, 6AG5, 6J4, 6ж4, 6136, 6BX6, 6AC7, 6AU6, 6J5, 6ж5П, CV2521, 6F36, 6AH6, 6AN5, 6K4, EF93, 6K5, 6K4П, 6BA6, 6DA6, 5749 ([reference](https://doukaudio.com/products/mini-vacuum-tube-headphone-amplifier-hifi-stereo-desktop-audio-pre-amplifier))


### Tube Socket
Using [B7G](http://www.r-type.org/static/baseb7g.htm) sockets for tubes.


## Op-Amps

- AD827JN+MUSES8820 ([reference](https://www.youtube.com/watch?v=S-pgNuk6AKQ))
- MUSES8920D+LM4562 ([reference](https://forum.hifiguides.com/t/chinese-tube-power-pre-amps-tube-buffers/6646/165))
- MUSES8920, LM49860, LM4562, Burson V5i-D, Sparkos SS3602([reference](https://drop.com/buy/fx-audio-tube-03-preamp-buffer/talk/2731379?utm_source=linkshare))

## Capacitors
### Original capacitor values

<img src="img/pcb/capacitors_with_labeling.png" height="300"> 

#### PSU noise filters
 ID | Type 
 -- | ---- 
E102 | 1000uF 16V electrolytic LOWESR (ChongX VEHT)      
E103 | 22uF 250V electrolytic (ChongX VEHT)              
E104 | 22uF 250V electrolytic (ChongX VEHT)

#### Input / Output
**Input**
 ID | Type 
 -- | ---- 
C213 | 1uF 450V film (BMPP)
C214 | 1uF 450V film (BMPP)

**Output**
 ID | Type 
 -- | ---- 
E301 | 22uF 250V electrolytic LOWESR (ChongX VEHT)
E302 | 22uF 250V electrolytic LOWESR (ChongX VEHT)
C301 | 1uF 63V film (A1K9)
C302 | 1uF 450V film (BMPP)
C303 | 1uF 63V film (A1K9)
C304 | 1uF 450V film (BMPP)

#### Op-Amp
 ID | Type 
 -- | ---- 
E101 | 100uF 25V electrolytic LOWESR (ChongX VEHT)
E201 | 100uF 25V electrolytic LOWESR (ChongX VEHT)
E202 | 100uF 25V electrolytic LOWESR (ChongX VEHT)
E203 | 10uF 50V electrolytic LOWESR (ChongX VEHT)
E204 | 10uF 50V electrolytic LOWESR (ChongX VEHT)
E207 | 100uF 25V electrolytic LOWESR (ChongX VEHT)

### Changing Onboard Capacitors

#### #1

- 4 x WIMA MKP4 1uF 250v (C213, C214, C302, C304) ⚠️voltage smaller than original
- 2 x WIMA MKS4 1uF 100v (C301, C303) 💡voltage larger than original
- 4 x Nichicon KT 220uF 25v (E101, E201, E202, E207) 💡capacitance larger than original

<img src="img/mods/camphoto_1804928587.JPG" height="100">  
<img src="img/mods/IMG_4516.JPG" height="100">  
<img src="img/mods/IMG_4517.JPG" height="100">   
<img src="img/mods/IMG_4518.JPG" height="100">  

([reference](https://audiokarma.org/forums/index.php?threads/fx-audio-6j1-tube-preamp-a-31-wonder.848535/post-13997979))

#### #2

- WIMA 1uF/63V (C301, C303)
- electrolytic caps from 100uF/16V to 220uF/25V  (E201, E202, E207) 💡voltage larger than original

<img src="img/mods/20200423_211556.jpg" height="100">  
<img src="img/mods/20200423_211614.jpg" height="100">  

([reference](https://audiokarma.org/forums/index.php?threads/fx-audio-6j1-tube-preamp-a-31-wonder.848535/post-13730561))

#### #3
- Caps are WIMA, Nichicon, and the one Panasonic in the power supply section. ⚠️capacitance not mentioned, not visible
- film caps settling on 1.5uF (C301, C303) ❓not visible
- 2.2uF (C213, C214, C302, C304) ⚠️ voltage less than original
- p/s cap from 1000uF to 2200uF (E102)

<img src="img/mods/81d2943209ab0220c90312e0348ea5b156275322.jpeg" height="100">  

([reference](https://forum.hifiguides.com/t/chinese-tube-power-pre-amps-tube-buffers/6646/165))

## Power Supply
The unit is shipped with an 12V 1A power supply using a standard P1J connector (DC plug).
<img src="img/parts/psu.jpg" height="300">  
<img src="img/parts/psu-plug.jpg" height="300"> 


## Manual
[Manual PDF](manual/fx-audio-tube-03-user-manual.pdf)

## Tutorials
- [Tube matching 101](https://tubemaze.info/tube-matching-101)
- [Bias tuning tubes](https://robrobinette.com/How_to_Bias_a_Tube_Amp.htm)

## Forum Threads
- [drop.com](https://drop.com/buy/fx-audio-tube-03-preamp-buffer/talk#discussions)
- [prohardver.hu (Hungarian)](https://prohardver.hu/tema/fulhallgato_erositok_dacs_headamps_headphone_amplifiers/hsz_87015-87015.html)
- [hifiguides.com](https://forum.hifiguides.com/t/chinese-tube-power-pre-amps-tube-buffers/6646/73)
- [farmedia.com](https://farmedia.com/tube-audio-line-level-buffers/)
- [audiokarma.org](https://audiokarma.org/forums/index.php?threads/a-review-of-fx-audio-6j1-tube-preamp-not.916958/page-2#post-14299487)
- [audiokarma.org](https://audiokarma.org/forums/index.php?threads/redux-and-more-fx-audio-6j1-tube-preamp-a-31-wonder.980897/)
- [toanvoaudio.vn](https://toanvoaudio.vn/shop/fx-audio-tube-03-mod-full-opan-hiend-muses01-muses02/)
- [audiosciencereview.com](https://www.audiosciencereview.com/forum/index.php?threads/tube-03.19480/page-2)