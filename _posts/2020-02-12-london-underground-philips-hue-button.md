---
title: The London Underground Philips Hue Light Switch
date: 2020-02-12T23:56:01Z
redirect_from:
  - /2020/02/12/london-underground-philips-hue-button.html
teaser:
  text: |
    A decommissioned Jubilee Line door button turned in to a Philips Hue light switch, complete with Sonos
    integration for a little bit of disco.
    <p><iframe width="480" height="270" src="https://www.youtube.com/embed/HGSPCLT5efM"></iframe></p>

---

A decommissioned Jubilee Line door button turned in to a Philips Hue light switch, complete with Sonos integration for
a little bit of disco.

<iframe width="560" height="315" src="https://www.youtube.com/embed/HGSPCLT5efM?si=ZSNAvSJyxemp1orn" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

I picked up a [decommissioned Jubilee line door button](https://www.ltmuseumshop.co.uk/vintage-shop/railwayana/jubilee-line-buttons)
after a trip to the London Transport museum. Given my addiction to Hue lights, a switch was the obvious thing to do with
it.

There wasn't much information on repurposing the door button, so I created an Instructable ["Hacking a London Underground Jubilee Line Door Button"](https://www.instructables.com/id/Hacking-a-London-Underground-Jubilee-Line-Door-But).

I had a few options to control the lights: an ESP8266 / ESP32 Arduino to talk to the Hue API, a DIY Zigbee light link
device such as described on [PeeVeeOne](https://peeveeone.com/?p=187), or taking apart a Hue Switch and modifying
it to work with one button by the use of a microcontroller (although Philips have since released [this](https://www2.meethue.com/en-gb/p/hue-smart-button/8718699693985)).

I went down the ESP32 route as it would also let me integrate with the Sonos API to create a secret disco mode.
If I get around to putting the ESP32 into sleep mode then the battery should last a decent amount of time, although for some reason my
ESP32 refuses to be powered by my 3.7V lipo battery so I am currently running it off of USB.

The code for the ESP32 is on [github](https://github.com/mnkii/esp32-philips-hue-button), with the code for the Sonos
integration in its own branch.

One of the tricky parts of the project was the Sonos integration, I've created a
[small app](https://github.com/mnkii/sonos-token) to ease the generation of Sonos auth tokens for Microcontroller projects.


<img src="/assets/images/door-button/lit-up.jpg" alt="Lit up button" width="1024" height="683">

<img src="/assets/images/door-button/purple.jpg" alt="Purple button" width="1024" height="683">

<img src="/assets/images/door-button/as-purchased.jpg" alt="As purchased" width="683" height="1024">

<img src="/assets/images/door-button/back.jpg" alt="Back of button" width="683" height="1024">
