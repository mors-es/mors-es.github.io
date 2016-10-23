---
title: A bicycle to increase volume
date: 2016-10-23 22:14:02.868000000 Z
tags:
- Tutorial
- Arduino
- Makers
- AppleScript
description: When the party stands for sports
---

I've discovered Arduino and all the makers's world with this project. The idea was at first to hack an *exercise bike* to control the volume of the music. (It was for a theme-based party: blackout ).

In the original project I'd maked it with a dynamo and read the signal with the Arduino. Here I explain how to make it with a bike speedometer (in fact, only the sensor and the magnet). This tutorial work only with a Mac, but if any people want to make a version compatible with Linux or Windows, <a href="https://github.com/mors-es/sound-bike/fork">fork</a> the project on GitHub, it's on MIT licence ;)

<a class="github-button" href="https://github.com/mors-es/sound-bike/fork" data-icon="octicon-repo-forked" data-style="mega" aria-label="Fork mors-es/sound-bike on GitHub">Fork Sound-bike</a>

## Stuff you need

![stuff](/assets/images/posts/stuff-sb.jpeg)

* An exercise bike ([or a bike](http://www.instructables.com/id/Indoor-Bike-Trainer/) :-) )
* An ARDUINO/GENUINO UNO
* A Bike speedometer (the sensor and the magnet of it)
* A pliers
* Some cable ties
* A computer (in this tutorial you need a Mac)

------

## 1. Install the sensor and the magnet

You need to cut the wire of the sensor near the bike computer. After that, you can set the sensor on the fork of the bike exercise and the magnet on the wheel. Be carful, the magnet need to be on the front on the sensor.

## 2. Install the .ino file in the Arduino

Download the zip (repository) of *Sound-bike*

<a class="github-button" href="https://github.com/mors-es/sound-bike/archive/master.zip" data-icon="octicon-cloud-download" data-style="mega" aria-label="Download mors-es/sound-bike on GitHub">Download</a>

or clone-it

<pre>$ git clone https://github.com/mors-es/sound-bike.git</pre>

If you didn't it already, download and install the latest version of Arduino Software (go to the [Download page of Arduino](https://www.arduino.cc/en/Main/Software)).

Plug the ARDUINO UNO by usb on your Mac. Open the [bike-running-check.ino](https://github.com/mors-es/sound-bike/blob/master/bike-running-check/bike-running-check.ino) file (in the namesake folder) with **Arduino Software**. En upload the file in your ARDUINO UNO (menu Sketch > Upload or **⌘ + U**).

> Beware that you have to select the right port. You can find your ARDUINO UNO's port on the menu (Tools > Port).

## 3. Run the AppleScript and enjoy!

Open the [volume-controller.scpt](https://github.com/mors-es/sound-bike/blob/master/volume-controller.scpt) file with your **Script editor** on your Mac.

Set the right port on the line 2 of the code. You need to copy the information from Arduino Software (on the bottom of the windows or in menu Tools > Port).

<pre>set use_port to "/dev/cu.usbmodemfa131"</pre>

Than run the code with the **Script editor**. Now, you can play some music on iTunes, Spotify or whatever and when you ride your bike --> the volume change !! Awesome no !?

Any problem to install ? Ask help on the comment of this post. Any bug ? post an issus on GitHub. Don't hesitate to share this post or [the project page](http://mors.es/sound-bike) on Twitter or Facebook.

<a class="github-button" href="https://github.com/mors-es/sound-bike/issues" data-icon="octicon-issue-opened" data-style="mega" aria-label="Issue mors-es/sound-bike on GitHub">Post an issue</a>
