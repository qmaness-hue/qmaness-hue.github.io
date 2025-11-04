---
title: Component Selection
---

### Light Sensor

*Table 1: Light Sensor for Clap Light*

**Light Sensor**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](ActiveFilter_qm.png)<br>Option 1<br> Active Band-Pass Filter <br>$1-10/each<br>[Link to tutorial](https://www.electronics-tutorials.ws/filter/filter_7.html)                 | \* Highly adjustable<br>\* Better control over filter characterisitics<br>\* Can meet surface mount constraint of project                                               | \* Requires op-amp (or similar) system<br>\* More complex <br>\* Requires power supply |
| ![](BA3835F_qm.png)<br> Option 2 <br> BA3835F-E2 Active Band-Pass Filter<br>\* $5.34/each <br>\* [Link to product](https://www.mouser.com/ProductDetail/ROHM-Semiconductor/BA3835F-E2?qs=IsRgwgmxh69SW0igeBnrlg%3D%3D) | \* Easier to work with <br>\* Compact <br> \* Easily repeatable and understood | * More expensive <br>\* Has unadjustable attributes <br>\* Requires power supply |               
| ![](PassiveFilter_qm.png)<br> Option 3 <br> Passive Band-Pass Filter<br>\* $1-10/each <br>\* [Link to tutorial](https://www.electronics-tutorials.ws/filter/filter_4.html) | \* No power supply needed <br>\* Simple <br> \* Easily repeatable and understood | * Less adjustable <br>\* Would require more innovation to apply <br>\* Could end up being large and/or clunky |

**Choice:** Option 2: BA3835F-E2 Active Band-Pass Filter

**Rationale:** A widely made and used active band-pass filter is better in this application not only because it's smaller and requires less (unnecessary) innovation, but also because--in a real life scenario--it would allow for cheaper, more widely spread manufacturing of the clap light and its hardware/software.


### Decibel Filter

*Table 2: Decibel Filter for Clap Light*

**Decibel Filter**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](One-Knob_NoiseGate.png)<br>Option 1<br> One-Knob Noise Gate <br>$1-10/each<br>[Link to tutorial](https://effectslayouts.blogspot.com/2016/07/one-knob-noise-gate.html)                 | \* Highly adjustable<br>\* Better control over characterisitics <br>\* Can meet surface mount constraint of project         | \* Requires large number of parts <br>\* Very complex <br>\* Requires power supply <br>\* Likely to be relatively large |
| ![](AudioLimiterCircuit.png)<br> Option 2 <br> Audio Limiter <br>\* $1-10/each <br>\* [Link to product](https://www.edn.com/audio-limiter-circuit-schematic/) | \* Less complex <br>\* Smaller than alternatives <br> \* Highly Adjustable | * Requires op-amp system <br>\* Would require a lot of innovation <br>\* Requires power supply |               
| ![](WindowComparator.png)<br> Option 3 <br> Window Comparator Circuit <br>\* $1-10/each <br>\* [Link to tutorial](https://www.electronics-tutorials.ws/opamp/op-amp-comparator.html) | \* Easily applied <br>\* Recieves easily adjustable (with software) range of voltages <br> \* Doesn't filter (uses 'switch' instead) | * Requires extra innovation for easy user adjustabiity <br>\* More specific voltage/decibel range than other comparators<br>\* Requires power supply <br>\* Requires op-amp <br>\* More complex than other comparators |
| ![](TLV6700DDCR.png)<br> Option 4 <br> TLV6700DDCR Window Comparator <br>\* $1.87/each <br>\* [Link to product](https://www.digikey.com/en/products/detail/texas-instruments/TLV6700DDCR/8635318) | \* Easily applied <br>\* Allows for adjustment of thresholds <br> \* Doesn't filter (uses 'switch' instead) <br>\* Wide range of voltage inputs| * Requires power supply <br>\* More complex than other comparators |

**Choice:** Option 4: TLV6700DDCR Window Comparator

**Rationale:** A window comparator is the best choice because it would allow for a more specific range of decibels in order to activate the switch--reducing accidental activation. It requires less innovation than a noise gate and limiter would, as neither of those are necessarily made for filtering decibel level in the same way that is required by a clap light. Although more complex than other comparators, it would allow for a more specific range of decibels to be the activation range, reducing accidental light activation. An already-created comparator system such as the TLV6700DDCR is also prefferable to a ciruit equivalent because it only necessitates 1 device, therefore streamlining creation and debugging.


### Voltage Regulator

*Table 3: Voltage Regulator for Filtering Subsystem*

**Voltage Regulator**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](LM7805.png)<br>Option 1<br> LM7805 <br>$0.50/each<br>[Link to product](https://www.digikey.com/en/products/detail/stmicroelectronics/L7805CV/585964)                 | \* Simple <br>\* Meets specifications for +5V voltage regulator <br>\* Typical current output is more than enough needed for system                                               | \* Can have problems with overheating <br>\* Might need heatsink system |
| ![](LD1086DT50TR.png)<br> Option 2 <br> LD1086DT50TR <br>\* $1.29/each <br>\* [Link to product](https://www.digikey.com/en/products/detail/stmicroelectronics/LD1086DT50TR/725468) | \* Current guaranteed until 1.5A (nearly 2 times what is needed) <br>\* Wide working temperature range <br> \* Very consistent voltage output | * Suffers from similar overheating issues as LM7805 <br>\* Only outputs +5V <br>\* More efficient options |               

**Choice:** Option 1: LM7805

**Rationale:** The LM7805--while not as efficient as others and lacking impressive specifications--is perfectly capable of doing what is required by the filter subsystem. Considering that only +5V and a current of ~750mA is necessitated by the system, the specifications given by the LM7805 is more than enough. It must also be pointed out that, as students, we already have easy access to this voltage regulator. It's a simple choice, and the subsystem doesn't need a complex voltage regulator.

