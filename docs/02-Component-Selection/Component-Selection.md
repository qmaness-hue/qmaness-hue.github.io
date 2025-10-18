---
title: Component Selection
---

### Frequency Filter

*Table 1: Frequency Filter for Clap Light*

**Frequency Filter**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](ActiveFilter_qm.png)<br>Option 1.<br> Active Band-Pass Filter <br>$1-10/each<br>[Link to tutorial](https://www.electronics-tutorials.ws/filter/filter_7.html)                 | \* Highly adjustable<br>\* Better control over filter characterisitics<br>\* Can meet surface mount constraint of project                                               | \* Requires op-amp (or similar) system<br>\* More complex <br>\* Requires power supply |
| ![](BA3835F_qm.png)<br>\ Option 2. <br>\ BA3835F-E2 Active Band-Pass Filter<br>\* $5.34/each <br>\* [Link to product](https://www.mouser.com/ProductDetail/ROHM-Semiconductor/BA3835F-E2?qs=IsRgwgmxh69SW0igeBnrlg%3D%3D) | \* Easier to work with <br>\* Compact <br> \* Easily repeatable and understood | * More expensive <br>\* Has unadjustable attributes <br>\* Requires power supply |               
| ![](PassiveFilter_qm.png)<br>\ Option 3. <br>\ Passive Band-Pass Filter<br>\* $1-10/each <br>\* [Link to tutorial](https://www.electronics-tutorials.ws/filter/filter_4.html) | \* No power supply needed <br>\* Simple <br> \* Easily repeatable and understood | * Less adjustable <br>\* Would require more innovation to apply <br>\* Requires power supply <br>\* Could end up being large and/or clunky |

**Choice:** Option 2: BA3835F-E2 Active Band-Pass Filter

**Rationale:** A widely made and used active band-pass filter is better in this application not only because it's smaller and requires less (unnecessary) innovation, but also because--in a real life scenario--it would allow for cheaper, more widely spread manufacturing of the clap light and its hardware/software.

### Decibel Filter

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](One-Knob_NoiseGate.png)<br>Option 1.<br> One-Knob Noise Gate <br>$1-10/each<br>[Link to tutorial](https://effectslayouts.blogspot.com/2016/07/one-knob-noise-gate.html)                 | \* Highly adjustable<br>\* Better control over characterisitics <br>\* Can meet surface mount constraint of project         | \* Requires large number of parts <br>\* Very complex <br>\* Requires power supply <br>\* Likely to be relatively large |
| ![](AudioLimiterCircuit.png)<br>\ Option 2. <br>\ Audio Limiter <br>\* $1-10/each <br>\* [Link to product](https://www.edn.com/audio-limiter-circuit-schematic/) | \* Less complex <br>\* Smaller than alternatives <br> \* Highly Adjustable | * Requires op-amp system <br>\* Would require a lot of innovation <br>\* Requires power supply |               
| ![](PassiveFilter_qm.png)<br>\ Option 3. <br>\ Passive Band-Pass Filter<br>\* $1-10/each <br>\* [Link to tutorial](https://www.electronics-tutorials.ws/filter/filter_4.html) | \* No power supply needed <br>\* Simple <br> \* Easily repeatable and understood | * Less adjustable <br>\* Would require more innovation to apply <br>\* Requires power supply <br>\* Could end up being large and/or clunky |

**Choice:** Option 2: BA3835F-E2 Active Band-Pass Filter

**Rationale:** A widely made and used active band-pass filter is better in this application not only because it's smaller and requires less (unnecessary) innovation, but also because in a real life scenario, it would allow for cheaper, wider spread manufacturing of the clap light and its hardware/software.
