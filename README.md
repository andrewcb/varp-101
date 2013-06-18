varp-101
========

VArp-101 is a Max for Live MIDI effect which acts as a flexible arpeggiator/note repeater. Features include:

* A number of traditional arpeggiator modes (ascending, descending, several alternating modes and random).
* The ability to add up to 3 octaves above the notes held down, as in 1980s-vintage synthesizers.
* A mono mode, in which only the last note held down will be emitted; this is useful when combining with other MIDI effects in Live.
* Variable note durations; the output of the arpeggiator is a stream of single- and double-length notes, which can consist of one of several built-in patterns or a random mix, whose ratio is user-controllable.
* The means to repeat each note pitch and duration between 1 and 4 times; this allows for more complex patterns to be built up.

VArp-101 is built in Max for Live and works as a MIDI Effect in Ableton Live if you have Max for Live. Simply drag VArp-101.amxd in front of any instrument device in the Device View and Bob's your uncle. 

## Overview

VArp-101, like other arpeggiators, responds to keys pressed on a keyboard (or notes sequenced in a Live MIDI Clip) and emits a stream of notes of various pitches. The pitches come from the keys pressed, with copies of those notes at higher octaves optionally added. VArp-101 emits notes when Live's transport is running, at specified note intervals; the stream of notes emitted by VArp-101 can consist of short and long notes, with short notes being a user-specified duration and long notes being of two short notes' duration.

## The controls

The VArp-101 panel has the following controls:

* **Arp mode**: A dropdown menu which selects the arpeggiator mode. Modes are:
 + Ascending (**↗**): The arpeggiator cycles through available note pitches from lowest to highest, then starting again at the lowest.
 + Decending (**↘**): The arpeggiator cycles through available note pitches from highest to lowest, then starting again at the highest.
 + Alternating (**⌃**): The arpeggiator cycles through available note pitches from lowest to highest, and then back to lowest. The lowest and highest notes are played only once in each cycle; i.e., if the notes held down are C, E and G, it will play C E G E C E G E. 
 + Random (**rnd**): The arpeggiator plays notes selected at random from the available note pitches. 
 + Alternating 2 (**↗↘**): In each cycle, the arpeggiator plays the available notes from the lowest to the highest, and then from the highest to the lowest. This differs from the previous Alternating setting in that the lowest and highest are repeated. I.e., if the notes held down are C, E and G, it will play C E G G E C C E.
 + Alternating 4 (**↗↘↘↗**): In each cycle, the arpeggiator plays the available notes ascending, descending, descending and then ascending. Lowest and highest notes are repeated, as in Alternating 2.
 + Monophonic (**mono**): This is not technically an arpeggiator; while keys are held down, it plays each note with the pitch of the most recently pressed key.

* **Octaves**: The number of octaves to play. If this is 1, only the notes pressed are used by the arpeggiator. Higher values add octaves above those pressed. (Setting this to 2 and playing one note can get a classic 1980s synthpop bassline.)

* **N rpt**: Note repeat. The number of times each note pitch generated by the arpeggiator is played. If 1, they are not repeated; if 2, each pitch is played twice; i.e., an ascending arpeggion on a C Major chord would play C, C, E, E, G, G.

* **Restart**: If on, arpeggio patterns start from the beginning whenever the first note is held down.

* **Duration mode**: How VArp-101 determines whether to emit a long or short note. If set to Random (*rnd*), VArp-101 will randomly choose each note to be either long or short, with the *DurationMix* control determining the probability. Other modes select predefined patterns, which are displayed graphically in the menu. 

* **Duration mix**: If the duration mode is set to random, the proportion of short notes in the mix; this varies from all long notes (0%) to all short notes (100%)

* **D rpt**: Duration repeat. The number of times each note duration value is used. If 1, they are not repeated; if 2, short and long notes are played in groups of two, and so on. Note that this is independent of note repeat; notes of repeated duration may have different pitches and vice versa.

* **Legato**: The proportion of its duration that a note is on; this goes from very short to 1.

* **Base duration**: The duration of a short note, in terms of tempo units. Both ordinary and triplet units are provided.

== Licence ==

VArp-101 is open-source software, distributed under a Creative Commons CC-BY-SA licence; which means that you are allowed to use it commercially or noncommercially, copy it and release derivative works, as long as the author (Andrew Bulhak) is acknowledged and any derivative works are equally free to use and copy.
For more details, see http://creativecommons.org/licenses/by-sa/3.0/
