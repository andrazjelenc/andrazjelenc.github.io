---
title: "Hugo - Retro games on DOSBox"
date: 2023-06-18T00:00:00+02:00
draft: false
tags:
  - other
---

## DOSBox

DOSBox is an open-source emulator that allows you to run software and games designed for the MS-DOS operating system on modern computers. MS-DOS was the dominant operating system in the 1980s and early 1990s.

We can download it from https://www.dosbox.com/. Currently latest release is 0.74-3.

We will be running DOSBox on Windows 10 x64.

## Hugo


On the internet we can find many games for MS-DOS. One of such games is [Hugo](https://en.wikipedia.org/wiki/Hugo_(video_game)) from 1990s.

We can find Hugo 3 in Slovenian language on archive.org as [Hugo 3 (Sl)(1997)(ITE Media)](https://archive.org/details/Hugo3Sl1997ITEMedia).

Extract downloaded files and copy files from .ISO into C:\GAMES\HUGO. Also extract HUGOFIX.ZIP into the same folder.

Now start DOSBox and mount newly created folder to it. With flag `-freesize 500` you tell DOSBox that is can assume the folder has 500MB of free space.
```
Z:> MOUNT C C:\GAMES\HUGO -freesize 500
Drive C is mounted as local directory C:\GAMES\HUGO\
```
Now move over to newly mounted C drive.
```
Z:> C:

C:>
```

First run `HUGOFIX` executable to bypass problem described [here](https://www.vogons.org/viewtopic.php?t=28632).
```
C:> HUGOFIX

C:>
```

Run `INSTALL` file to install Hugo. When asked for path just keep default path pointing at C:\4HUGO and press ENTER.
```
C:> INSTALL
```
When asked for providing Sound card settings keep the defaults and save the settings. At this point you will lose ability to freely move mouse in and out of DOSBox. Press CTRL+F10 to release the mouse. More special keys can be found at https://www.dosbox.com/wiki/Special_Keys.

The game is now installed. Run it with executing `HUGO` and enjoy the game!
```
C:\4HUGO> HUGO
```

Next time you can skip installation process and just run the game.
```
Z:> MOUNT C C:\GAMES\HUGO -freesize 500
Z:> C:
C:> cd 4HUGO
C:> HUGO
```

