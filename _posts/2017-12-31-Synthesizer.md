---
permalink: synthesizer
title: Synthesizer 
date: 2017-12-31
tag: [music, electronics]
category: objects
---

{WORK IN PROGRESS}

Musical **synthesizers** (synths) are electronic devices which generates audible sound through the means of manipulating or creating discrete or continuous signal data and allows for significant control over the timbre of the sound. With this definition, we're able to group between analogue and digital synthesizers while excluding the electric guitar out of the definition. Hopefully. I haven't seen built-in effect pedals for guitars.

## Types of synthesis

Different synthesizers employ different methods of generating sounds. These generated sounds can also be later modified by other components of the synthesizer, but the core of the synth lies in its type of synthesis.

The most prominent types of synthesis are:

* [Subtractive Synthesis](subtractive_synthesis)
* [FM Synthesis](FM_synthesis)
* [Additive Synthesis](additive_synthesis)
* [Sample-based Synthesis](sample-based_synthesis)
* [Granular Synthesis](granular_synthesis)

There are more ways to synthesis sounds:

* [Stochastically](stochastic_synthesis) [1](#footnotes)
* [Karplus-Strong synthesis](karplus-strong_synthesis)

Generally, these different types have some overlapping properties. We can probably find the common properties, and then point out which method uses which of those properties.

## Components

A synth can have multiple components which makes up the final sound. Some synthesis techniques above are possible with only one component, but to craft a sound for musical use, synthesizers usually accompany them with other components.

A synthesizer which has already wired or set-up the components and how they interact with each other is called... a (pre-patched) synthesizer.
A synthesizer which has some wired components, but leave room for you to wire the rest is called a semi-modular synthesizer.
A synthesizer which makes you do all the hard-work, i.e. not having any components wired, is a modular synthesizer.

The common components are:

### Generators

A **Generator** in a synthesizer generates source of an audible. It can have different names like **operator** (in FM synthesis), or **oscillator** (in subtractive, analogue synthesis), although there are reasons why they hold different names and we shouldn't use them so interchangeably. 

If your synthesizer only had generators, it can still make sound. 

### Filter

With simplest explanations, a **filter** lets certain parts of the sound through, while quieting down the others. There are different kinds of filters: the low-pass filters let only the low-end of the sound through, high-pass lets the high-end through, a band-pass is both low-pass and high-pass which lets _some_ sound through.

Playing with filters will perhaps acquaint you with a sense of how it works. I will add demos at some point.

Filters are a great gateway for you to understand sound as there are many ways of representing sound. You can represent it with:

```
^ intensity
|  _      _            /
| / \    / \      _   /
-/---\--/---\----/-\_/----> time
|     \/     \  /
|             \/
v
```

Intensity (of air pressure) Over Time, which is how computers conventionally store audio data, or how you would model how your ear drum vibrates. On the other hand, you can also represent sound with:
```
^ intensity
|        k                  Let's say k is at 440 hertz
|        |                            and it's x units loud.
|        | |
|   |    | ||
|___|_|__||||_____frequency
```

Intensity Over Frequency, which is analogous to a single slice in sheet music notation.

Surprise! Any piece of sound you hear can be made up of smaller fundamental sounds called "sinusoidal waves". These sinusoidal waves can have different frequencies and different intensities. The higher frequencies, the higher in pitch; the higher the intensity, the louder it is. In the diagram above, there's a sinusoidal wave at 440Hz and it's x units loud!

Why is this helpful? Well... 

The characteristic of a filter is usually represented in Intensity Over Frequency graphs, called **frequency response** of a filter. Here is an example of a frequency response of a low-pass filter:
```
 ^ intensity
 |       k
1|--------
 |        \
 |         \
 |__________\______frequency
```

What this graph says is: For whatever sounds that is lower than k hertz, the filter doesn't do anything to it; otherwise, make the sound quieter.

Here's yet another analogy: You are instructed to play a chord on a xylophone and have to play all notes as loud as each other. You play it incorrectly by playing the higher notes quieter. That is exactly what a low-pass filter does.

There are more characteristics of a filter such as the roll-off slope, the Q factor, and so on., which I won't bother explaining until this gets moved to its own section.


### Envelope

An **Envelope** (or Envelope Generator, EG) is a definition of a signal which has one or more stages, and optionally two trigger points and looping stages. A stage are two points of intensity separated by an amount of time in the signal. 

You can then apply the envelope to modulate (or change) a property of another component in your synthesizer. For example, you can apply the envelope to the pitch or the amplitude of the generators, or the cut-off of a filter.

Here is a typical 4-stage envelope shown below:

```
        • B                      // 1 : Attack
       / \
      /   \ 2                    // 2 : Decay
   1 /     \    3  D
    /       •------•             // 3 : Sustain
   /        C       \
  /                  \ 4         // 4 : Release
 /                    \
• A                    • E       
```

The diagram above is usually associated with the ADSR (Attack-Decay-Sustain-Release) which is prevalent in most synthesizers on the market. Note that the ADSR is a 4-stage envelope, but not all 4-stage envelopes are necessarily ADSR. 

The [Yamaha DX7](dx7) has 5 stages, with 4 out of 6 points allowed to change levels, 4 stage lengths changeable.

An ADSR envelope defines point A and D as trigger points. Specifically, the envelope will start at A when it is triggered with a key-on event, and start at D when it's triggered with a key-off event. Stage 3 (between point C and D) is the looping stage. The values (intensity/level) at points at A and E are not allowed to change in most common synthesizers (because they are ADSR). They however still allow you to change the length of the stages as well as.

Okay. But what does it sound like? Suppose I have generator which generates square wave, and I have an envelope which modulates the square generator's amplitude (~ loudness). Suppose I set the attack length to 1 sec, decay to 0.5 sec and release stage to have length 3 seconds. The sustain stage (looping stage) will have 25% its maximum amplitude. You should hear a sound fading in when I hold down the key, reaching to its maximum loudness in 1 second, taking 0.5 seconds to reach 25% of its volume, then when I release the key, it fades out within 3 seconds.

<audio controls src="assets/adsr-sample.mp3">Your browser does not support audio.</audio>

Another aspect of envelopes is how you interpolate between the points. In the example above, it's interpolated linearly, which is not ideal when you're modulating loudness, which us humans perceive logarithmically. I won't discuss this matter until I separate this section into its own entry.


## References

1. [ext](https://youtu.be/AQqXRSV8msA?t=4m51s) Jim Singh, YouTube.