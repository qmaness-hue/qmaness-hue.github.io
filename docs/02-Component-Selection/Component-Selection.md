---
title: Component Selection
---

### Light Sensor

*Table 1: Light Sensor for Clap Light*

**Light Sensor**


| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](TEMT6000.png)<br> Option 1 <br> TEMT6000X01<br>$0.90/each<br>[Link to product](https://www.mouser.com/ProductDetail/Vishay-Semiconductors/TEMT6000X01?qs=%2Fjqivxn91ccZGXDwz0wGxg%3D%3D&srsltid=AfmBOooQdB74AbB3cmws8rrGCeFrnCZulZ_kDPwcyoM4WwAIF_F-DG09)                 | \* Simple analog output<br>\* Fast response and tiny footprint <br>\* Works directly with op-amp/ADC| \* Output is non-linear vs. lux<br>\* Requires biasing and calibration <br>\* Sensitive to angle/spectrum|
| ![](BH1750FVI.png)<br> Option 2 <br> BH1750FVI <br> $4.00/each <br> [Link to product](https://www.sunrom.com/p/digital-light-sensor-bh1750fvi?) | \* Reports lux directly via I²C <br>\* Minimal analog design | * Requires I²C + library <br>\* Fixed spectrum/transfer function <br>\* Module size > bare sensor                                                         |
| ![](VEML7700.png)<br> Option 3 <br> Adafruit VEML7700 Lux Sensor - I2C Light Sensor - STEMMA QT / Qwiic<br>$5.00/each<br>[Link to product](https://www.adafruit.com/product/4162?srsltid=AfmBOorBHSPB9NFLJcU5ez7-J4arau8XeTmrqw6rngzxuV2-He8xyOAv)                 | \* Wide 0–120 klux, 16-bit <br>\* adjustable gain/integration <br>\* 3.3/5 V friendly and accurate lux output                                               | \* I²C interface required|
| ![](PDV-P5003.png)<br> Option 4 <br> PDV-P5003 Photo-Resistor <br>$1.54/each<br>[Link to product](https://www.digikey.com/en/products/detail/advanced-photonix/PDV-P5003/480601?gclsrc=aw.ds&gad_source=1&gad_campaignid=20232005509&gbraid=0AAAAADrbLlhkYAWNMNTozepAbTv2ccVwy&gclid=Cj0KCQiAq7HIBhDoARIsAOATDxBoWV_Mcap_0-JiqJw5yr9BXxVhOUe6OAGBLrxOzEh_MJes9yKxfcEaAtMhEALw_wcB)                 | \* Very simple and easy to use <br>\* Small footprint <br>\* Works directly with op-amp (we had a lab using a photoresistor| \* Has no function aside from resistor and light sensor <br>\* Less complex usability|

**Choice:** Option 4: PDV-P5003 Photo-Resistor

**Rationale:** The PDV-P5003 Photo-Resistor keeps BOM cost and firmware complexity low while providing fast analog response. It doesn't need to be calibrated in the same way as a phototransistor as is extremely simple and easy to adjust/use.

### Op-Amp

*Table 2: Op-Amp for Light Sensor*

**Op-Amp**


| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](MCP6004.png)<br> Option 1 <br> MCP6004<br>$0.59/each<br>[Link to product](https://www.digikey.com/en/products/detail/microchip-technology/MCP6004-I-P/523060?gclsrc=aw.ds&gad_source=1&gad_campaignid=120565755&gbraid=0AAAAADrbLliPi33eoHc7gYS7GQQx_jXZT&gclid=Cj0KCQiA6NTJBhDEARIsAB7QHD2r7qV9vG9dFCA1AbAkpbMg6GXbUDlzRKTEmFrp_mVI_8Lx5aOBzAUaAsM5EALw_wcB)                 | \* Operates from 1.8V-6V<br>\* Extremely simple and easy <br>\* Can easily invert signal with minimal footprint | \* Requires manual testing with sensor <br>\* Requires varying resistors based on each sensor |
| ![](LM358N.png)<br> Option 2 <br> LM358N <br> $1.00/each <br> [Link to product](https://www.digikey.com/en/products/detail/texas-instruments/LM358N-NOPB/6264) | \* Easy to use <br>\* Operates from 3V-32V | * Larger footprint for inverted amplification <br>\* More expensive |                                                         |

**Choice:** Option 1: MCP6004

**Rationale:** The MCP6004 is a simple, easy to use Op-Amp that we have been using throughout the semester (meaning that we have good experience with it). It can easily and intuitively invert the signal from the sensor. This is something we want so as to make the signal more intuitive.



### Switch

*Table 3: Switch for Clap Light Sound Sensor Subsystem*

**Switch**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](CST10T2CR.png)<br>Option 1<br> CST10T2CR ON/OFF Switch <br>$2.65/each<br>[Link to Product](https://www.digikey.com/en/products/detail/cit-relay-and-switch/CST10T2CR/12503245)                 | \* Only on and off functions keep it simple <br>\* Characterisitics suit project <br>\* Durable and high speed         | \* Limited customization <br>\* Requires power supply|
| ![](ANT11SECQE.png)<br> Option 2 <br> 2449-ANT11SECQE-ND ON/ON Switch  <br>\* $1.94/each <br>\* [Link to product](https://www.digikey.com/en/products/detail/cit-relay-and-switch/ANT11SECQE/12503336) | \* Very compact <br>\* Versatile due to ON/ON function <br> \* Can offer two different on modes | \* Would require two different on modes to be created <br>\* More complex |              

**Choice:** Option 1: CST10T2CR ON/OFF Switch

**Rationale:** A simple ON/OFF switch like the one offered by the CST10T2CR is perfectly fine in this application. Seeing as a switch isn't even neccesary (it goes beyond expectations), just having the option itself is more than enough. 



### Voltage Regulator

*Table 4: Voltage Regulator for Sound Sensor Subsystem*

**Voltage Regulator**

| **Solution**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](LM7805.png)<br>Option 1<br> LM7805 <br>$0.50/each<br>[Link to product](https://www.digikey.com/en/products/detail/stmicroelectronics/L7805CV/585964)                 | \* Simple <br>\* Meets specifications for +5V voltage regulator <br>\* Typical current output is more than enough needed for system                                               | \* Can have problems with overheating <br>\* Might need heatsink system |
| ![](LD1086DT50TR.png)<br> Option 2 <br> LD1086DT50TR <br>\* $1.29/each <br>\* [Link to product](https://www.digikey.com/en/products/detail/stmicroelectronics/LD1086DT50TR/725468) | \* Current guaranteed until 1.5A (nearly 2 times what is needed) <br>\* Wide working temperature range <br> \* Very consistent voltage output | * Suffers from similar overheating issues as LM7805 <br>\* Only outputs +5V <br>\* More efficient options |               

**Choice:** Option 1: LM7805

**Rationale:** The LM7805--while not as efficient as others and lacking impressive specifications--is perfectly capable of doing what is required by the subsystem. Considering that only +5V and a current of ~750mA is necessitated by the system, the specifications given by the LM7805 is more than enough. It must also be pointed out that, as students, we already have easy access to this voltage regulator. It's a simple choice, and the subsystem doesn't need a complex voltage regulator.

### Final Selection

*Table 15: Light Sensor for Clap Light*

**Light Sensor**


| **Final Choice Summary**                                                                                                                                                                                      | **Pros**                                                                                                                                    | **Cons**                                                                                            |
| ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------- |
| ![](PDV-P5003.png)<br> Light Sensor <br> PDV-P5003 Photo-Resistor <br>$1.54/each<br>[Link to product](https://www.digikey.com/en/products/detail/advanced-photonix/PDV-P5003/480601?gclsrc=aw.ds&gad_source=1&gad_campaignid=20232005509&gbraid=0AAAAADrbLlhkYAWNMNTozepAbTv2ccVwy&gclid=Cj0KCQiAq7HIBhDoARIsAOATDxBoWV_Mcap_0-JiqJw5yr9BXxVhOUe6OAGBLrxOzEh_MJes9yKxfcEaAtMhEALw_wcB)                 | \* Very simple and easy to use <br>\* Small footprint <br>\* Works directly with op-amp (we had a lab using a photoresistor| \* Has no function aside from resistor and light sensor <br>\* Less complex usability|
| ![](MCP6004.png)<br> Op-Amp <br> MCP6004<br>$0.59/each<br>[Link to product](https://www.digikey.com/en/products/detail/microchip-technology/MCP6004-I-P/523060?gclsrc=aw.ds&gad_source=1&gad_campaignid=120565755&gbraid=0AAAAADrbLliPi33eoHc7gYS7GQQx_jXZT&gclid=Cj0KCQiA6NTJBhDEARIsAB7QHD2r7qV9vG9dFCA1AbAkpbMg6GXbUDlzRKTEmFrp_mVI_8Lx5aOBzAUaAsM5EALw_wcB)                 | \* Operates from 1.8V-6V<br>\* Extremely simple and easy <br>\* Can easily invert signal with minimal footprint | \* Requires manual testing with sensor <br>\* Requires varying resistors based on each sensor |                                                
| ![](CST10T2CR.png)<br>Switch<br> CST10T2CR ON/OFF Switch <br>$2.65/each<br>[Link to Product](https://www.digikey.com/en/products/detail/cit-relay-and-switch/CST10T2CR/12503245)                 | \* Only on and off functions keep it simple <br>\* Characterisitics suit project <br>\* Durable and high speed         | \* Limited customization <br>\* Requires power supply|
| ![](LM7805.png)<br>Voltage Regulator<br> LM7805 <br>$0.50/each<br>[Link to product](https://www.digikey.com/en/products/detail/stmicroelectronics/L7805CV/585964)                 | \* Simple <br>\* Meets specifications for +5V voltage regulator <br>\* Typical current output is more than enough needed for system                                               | \* Can have problems with overheating <br>\* Might need heatsink system |
