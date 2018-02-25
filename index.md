## Introduction

[tamagotch.org](http://tamagotch.org) aims at documenting the technical specifications of Tamagotchi toys. We focus on the worldwide releases. Do you want to contribute or report a broken link? Please [open a pull request](https://github.com/loociano/tamagotch).

## Original Series

* Versions: [P1 and P2](http://tamagotchi.wikia.com/wiki/Tamagotchi_(1996_Pet)), [Angel](http://tamagotchi.wikia.com/wiki/Tamagotchi_Angel) and [Ocean](http://tamagotchi.wikia.com/wiki/Tamagotchi_Ocean) 
* Release Dates: 1996-1998

## Connection Series

* Versions: [V1](http://tamagotchi.wikia.com/wiki/Tamagotchi_Connection_Version_1), [V2](http://tamagotchi.wikia.com/wiki/Tamagotchi_Connection_Version_2), [Mini](http://tamagotchi.wikia.com/wiki/Tamagotchi_Mini), [V3](http://tamagotchi.wikia.com/wiki/Tamagotchi_Connection_Version_3), [V4](http://tamagotchi.wikia.com/wiki/Tamagotchi_Connection_Version_4), [V4.5](http://tamagotchi.wikia.com/wiki/Tamagotchi_Connection_Version_4.5), [V5](http://tamagotchi.wikia.com/wiki/Tamagotchi_Connection_Version_5), [V5.5 (Celebrity)](http://tamagotchi.wikia.com/wiki/Tamagotchi_Connection_Version_5_Celebrity) and [V6 (Music Star)](http://tamagotchi.wikia.com/wiki/Tamagotchi_Music_Star).
* Release Dates: 2004-2009

## Mini

Mini was released in 2005 and re-launched worldwide in 2017.

* [Official Page (Japanese)](http://tamagotch.channel.or.jp/tamagotchi/mini)
* [Tamagotchi Wiki entry](http://tamagotchi.wikia.com/wiki/Tamagotchi_Mini)

### Tech Specs

* CPU: ?
* Memory: ?
* IO: 3 buttons, 16x16 pixel screen

### Disassembly

![](assets/img/IMG_20180224_134246.jpg)
![](assets/img/IMG_20180224_181646.jpg)
![](assets/img/IMG_20180224_182121.jpg)
![](assets/img/IMG_20180224_182359.jpg)

## TamaTown Tama-Go

[TamaTown Tama-Go](http://tamagotchi.wikia.com/wiki/TamaTown_Tama-Go) was released in 2010 and reverse engineered by [Natalie Silvanovich](http://natashenka.ca).

### Tech Specs

* CPU: 8-bit CMOS GPLB52320A ([datasheet](http://www.generalplus.com/doc/ds/GPLB52640A-52320A-51640A-51320AV19_ds.pdf)) with 2x 16-bit timers.
* RAM: 1,536 bytes
* ROM: 320K bytes = 10 banks of 32K ([dump](https://github.com/natashenka/Tamagotchi-Hack/tree/master/codedump/rompages), [GP Test Program](https://github.com/natashenka/Tamagotchi-Hack/blob/master/codedump/GPTestProgram))
* IO: 16 ports PA[7:0], PB[7:0]
  * Serial Peripheral Interface (SPI)
  * Display Controller: 4 levels of gray with 512 bytes of dedicated RAM. 64 segments and 32 commons = 2048 pixels
* Sound Processing Unit (SPU)

### Memory Map

```
$0000-$0600 SPU RAM, GP RAM
$0600-$0FFF -
$1000-$1FFF DPRAM (VRAM)
$2000-$2FFF -
$3000-$3FFF IO Reg
$4000-$7FFF ROM bank (lower)
$8000-$BFFF ROM bank (high)
$C000-$CBBF SPU table, test program
$CBC0-$CBFF Test Interrupt Vector
$CC00-$FFBF ROM (33C0 bytes)
$FFC0-$FFEF Interrupt Vector
$FFF0-$FFF9 -
$FFFA-$FFFD NMI and reset vector
$FFFE-$FFFF -
```

### Links

* [Tamagotchi Wiki. TamaTown Tama-Go](http://tamagotchi.wikia.com/wiki/TamaTown_Tama-Go)

## Friends Series

Versions: Friends and Friends: Dream Town (2014-2016).

### Links

* [Tamagotchi Wiki. Tamagotchi Friends](http://tamagotchi.wikia.com/wiki/Tamagotchi_Friends)
* [Tamagotchi Wiki. Tamagotchi Friends: Dream Town](http://tamagotchi.wikia.com/wiki/Tamagotchi_Friends:_Dream_Town_Digital_Friend)

## References

### Sites

* [tamagotchi.wikia.com](http://tamagotchi.wikia.com) The most comprehensive Tamagotchi Wiki to date.
* [Wikipedia. List of Tamagotchi releases](https://en.wikipedia.org/wiki/List_of_Tamagotchi_releases)
* [Natalie Silvanovich. Personal Site](http://natashenka.ca)
* [kwartzlab. Natalie Silvanovich posts](https://www.kwartzlab.ca/author/natalies)
* [spritesmods.com. Creating the Tamagotchi Singularity](http://spritesmods.com/?art=tamasingularity)

### Presentations

* [29c3: Many Tamagotchis Were Harmed in the Making of this Presentation](https://www.youtube.com/watch?v=c4PkcZScBV8)
* [30c3: Even More Tamagotchis Were Harmed in the Making of this Presentation](https://www.youtube.com/watch?v=mCt5U5ssbGU) ([slides](https://events.ccc.de/congress/2013/Fahrplan/system/attachments/2195/original/30c3_(1).pdf))

### GitHub repos

* [@natashenka Tamagotchi-Hack](https://github.com/natashenka/Tamagotchi-Hack)
* [@natashenka Egg-Shell - Tamagotchi Development Tools](https://github.com/natashenka/Egg-Shell)
* [@hortinstein Tamagotchi Matrix](https://github.com/hortinstein/tamatrix)

### Datasheets

* [Generalplus. GPLB52640A-52320A-51640A-51320A Version 1.9 (Dec 30, 2010).](http://www.generalplus.com/doc/ds/GPLB52640A-52320A-51640A-51320AV19_ds.pdf)
* [GPLB5x/3x GM03 Library User's Manual Version 2.0 (April 29, 2009)](http://www.lcis.com.tw/paper_store/paper_store/gplb5x_lb3x-GM03%20Libraryv20_user-201471313910398.pdf)