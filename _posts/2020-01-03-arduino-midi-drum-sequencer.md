---
title: "Midi Drum Sequencer"
date: 2020-01-03T01:02:01Z
draft: false
teaser:
    text: My analogue style MIDI step sequencer.
    image: /img/drum-sequencer/front.jpg
---

My analogue style MIDI step sequencer.

![image](/img/drum-sequencer/front.jpg)

<!--more-->

It has 48 switches to control 6 drums over 8 beats, a tempo control, LED indicator and start/stop switch all connected to
an Arduino Nano.

As the nano has 22 I/O pins, I used a keyboard matrix to connect the 48 toggle switches to 14 pins. This post at
the [bald engineer](https://www.baldengineer.com/arduino-keyboard-matrix-tutorial.html) was invaluable.

The diodes ares 1N4148, the box was from the [The Works](https://www.theworks.co.uk). The source code and
more circuit details are on [github](https://github.com/mnkii/arduino-midi-drum-sequencer/blob/master/arduino-midi-drum-sequencer.ino)

![image](/img/drum-sequencer/inside.jpg)

![image](/img/drum-sequencer/back.jpg)
