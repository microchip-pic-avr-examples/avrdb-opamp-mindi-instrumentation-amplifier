![Microchip logo](images/microchip.png)
# Getting started with Mindi™ simulation and AVR®DB microcontrollers
This guide will get you up and running with simulating the analog OPAMP module in AVR DB family devices using the Mindi simulation tool. For a larger overview, see ["Getting Started with Analog Signal Conditioning (OPAMP)"](https://github.com/search?q=topic%3Aavr-db+topic%3Agetting-started-with-opamp+org%3Amicrochip-pic-avr-examples).
## Configuration: Instrumentation Amplifier
The Instrumentation Amplifier op amp configuration amplifies a voltage across the input with high input impedance and presents it as a single-ended output voltage. The amplification can be configured by setting the feedback dividers.

![Instrumentation Amplifier](images/configuration.png)

### Mindi Simulation
![Mindi](images/mplab-mindi-analog-simulator.png)

Download and open the **Mindi schematic [here](https://github.com/microchip-pic-avr-examples/avrdb-opamp-mindi-instrumentation-amplifier/releases/latest)**

Press the _play_ button to simulate with an example stimulus source.

### Tweaking
The amplification of the Instrumentation Amplifier can be adjusted to any of 8 levels from 0.06 to 15 by changing the MUXWIP value in the control registers. The Mindi schematic contains a table detailing the levels of gain and their associated register and resistor values.

### Updating composer fields
Once the desired result has been verified with Mindi simulation, the corrected values should be moved back into MCC/Start by copying resistor configuration values across to the composer of your preference.

### Don't have Mindi?
You can download and install the [Mindi simulation tool](https://www.microchip.com/mplab/mplab-mindi), or use another SPICE simulator of your own preference. For use with different simulators, a plain spice model can be found in "Opamp_AVR_DB.txt" to replace the mindi-optimized ".lb" 
