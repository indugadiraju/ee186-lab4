# ee186-lab4

**Written Deliverables for Part 2 - ADC:**

(1) You can set the ADC bit resolution to 6, 8, 10, or 12 bits. The maximum sampling rate of each of thse resolutions is as follows:
- For 6 bits: 8.88 Msps for fast channels, 6.15 Msps for slow channels
- For 8 bits: 7.27 Msps for fast channels, 5.33 Msps for slow channels
- For 10 bits: 6.15 Msps for fast channels, 4.71 Msps for slow channels
- For 12 bits: 5.33 Msps for fast channels, 4.21 Msps for slow channels

I found this information in “Table 81. ADC characteristics” under Section “6.3.21 Analog-to-digital converter characteristics” in the datasheet.


(2) We need a voltage divider circuit so that the photoresistor’s changing resistance produces a changing voltage that the ADC can then measure. If the photoresistor is directly connected to the board (between the supply and the ADC input without the fixed resistor), the input would remain near the supply voltage the whole time rather than changing with light intensity!

(3) Link to video demonstrating ADC changes: https://drive.google.com/file/d/182xTJdUZlmXmEki7EWtkNlWn0s0vcFpn/view?usp=sharing

**Written Deliverables for Part 3 - DAC:**

(1) If B = 9, then Vout = (9 / (2^12)) = (9 / 4096) Vref, using the best resolution of 12-bits available on the MCU.

(2) The sampling rate of the DAC affects the quality of the waveform by determining how often the output voltage is updated. At a fixed waveform frequency, a higher sampling rate allows more samples per cycle, which produces a finer approximation/rendering of the intended waveform. Having too few samples would produce a coarser output and potentially distortion. With a fixed-length table, changing the sampling rate also changes the pitch because outputting samples faster makes the waveform repeat more times per second, increasing its frequency. Regarding the differences in sound perception between sine, square, and sawtooth waves:
- A sine wave sounds “smooth” because its voltage rises and falls gradually, producing a more pure, steady tone
- A square wave sounds “hollow”/buzzy because its voltage switches abruptly between two levels, producing a sharper sound than a sine wave
- A sawtooth wave sounds “brighter”/buzzier because its voltage steadily rises and then abruptly drops, repeating this pattern to produce a sharper, raspier tone.

We need a capacitor in the signal path when sending an audio signal to a speaker or earphones because it blocks the DAC’s constant voltage offset while passing the changing audio signal. The constant offset could cause steady current through the speaker or earphones, wasting energy as heat without producing useful sound. The capacitor blocks this steady current while allowing the changing signal that produces sound to pass through.

**Written Deliverables for Part 4 - Theremin:**

(1) Link to video demonstrating theremin working: https://drive.google.com/file/d/1e_rM8w7iBb32ELAN_YLySw6pDMQJilaZ/view?usp=sharing
