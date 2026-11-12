# ee186-lab4

**Written Deliverables for Part 2 - ADC:**

(1) You can set the ADC bit resolution to 6, 8, 10, or 12 bits. The maximum sampling rate of each of thse resolutions is as follows:
- For 6 bits: 8.88 Msps for fast channels, 6.15 Msps for slow channels
- For 8 bits: 7.27 Msps for fast channels, 5.33 Msps for slow channels
- For 10 bits: 6.15 Msps for fast channels, 4.71 Msps for slow channels
- For 12 bits: 5.33 Msps for fast channels, 4.21 Msps for slow channels

I found this information in “Table 81. ADC characteristics” under Section “6.3.21 Analog-to-digital converter characteristics” in the datasheet.


(2) Why do you need a voltage divider circuit? What would happen if the photodiode is directly connected to the board?
We need a voltage divider circuit so that the photoresistor’s changing resistance produces a changing voltage that the ADC can then measure. If the photoresistor is directly connected to the board (between the supply and the ADC input without the fixed resistor), the input would remain near the supply voltage the whole time rather than changing with light intensity!

**Written Deliverables for Part 3 - DAC:**

(1)

(2)
