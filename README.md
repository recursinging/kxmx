# kxmx

kxmx, pronounced "krachmacher", is a moniker connecting a heterogenous, but loosely coupled group of projects, mostly having to do with audio and music.  In sum, the components should form a sort of musical instrument, or maybe better a "rig", but I don't consider that a design goal.

## Motivation

I'm in a band.  Actually, two.  I sing, not particularly good, but it's fun, and I enjoy making music.  What I enjoy more though, is learning about, and tinkering with the technical aspects of making music. Because of this, actual music composition or lyric writing can be regularly postponed for technical reasons.

Easily bored, I like to keep a diverse set of projects going parallel.  These projects may lie dormant for months. I work, I have kids, I don't have much me time.

## Parts, moving or otherwise

Here's a list of projects either already underway, or things I'd like to do eventually...

### kxmx_hirn

A robust, portable (but damn heavy) [DJ case](https://www.magma-bags.de/multi-format-workstation-xl-plus.html) which I gutted and hacked to support Eurorack modules with 350 HU of capacity.  Built in are +19v, +12v, -12v, and +5v power supplies. A lot of the other kxmx components are in, or destined for this case, but since there are a number of ideas I'd like to explore with the case itself, making it a project in it's own right.

### kxmx_erack

A set of basic PCB templates for Eurorack modules which leverage the wonder of exceptionally cheap chinese fabrication.

### [kxmx_ruitar](https://github.com/recursinging/ruitar)

A guitar shaped MIDI/OSC controller, and hopefully someday, a standalone synthesizer.  I wanted to make something tactile to control parameters with, but in a more familiar way (to me) Being more comfortable on the guitar than the keyboard, the ruitar is the logical solution.

### kxmx_trig

A piezo drum trigger module, intended to collect and send a few drum events to kxmx_hirn where they can be abused.

### kxmx_vl2

The brain of a lobotomized TC Helicon [Voice Live 2](https://www.tc-helicon.com/Categories/Tchelicon/Vocal/Multi-Effects/VOICELIVE-2/p/P0CMC) which has been converted from a foot pedal to Eurorack format mounted in kxmx_hirn

### kxmx_4x4

A 4x4 VCA matrix mixer based on SSM2164 clones, and has a modular design:

* *kxmx_4x4_core* - The 16 x2164 voltage control ports of the core module are intentionally broken out to the edge of the board. This allows for pluggable control boards to control the gain of the matrix however they want.  
* *kxmx_4x4_control_esp32* - This module controls the gain of the core using an Expressif ESP32 MCU which has WiFi and Bluetooth out of the box.  This module will make the mixer gain levels remotely controllable via MIDI or OSC.
* *kxmx_4x4_control_cv* - This module allows the gain of the core to be controlled by TRS jack at Eurorack CV levels.

### [kxmx_dsp](https://github.com/recursinging/kxmx_dsp)

Experiments with DSP concepts and algorithms

### [kxmx_trestle](https://github.com/recursinging/kxmx_trestle)

A bi-directional OSC SLIP encoded serial to UDP bridge.

## Licenses

I'll try to be consistent:

* Standalone software/firmware is [LGPLv3](https://www.gnu.org/licenses/lgpl-3.0.en.html)
* Software libraries are [MIT](https://opensource.org/licenses/MIT)
* Hardware/Media is [CC-BY-NC-SA 3.0](https://creativecommons.org/licenses/by-nc-sa/3.0/)