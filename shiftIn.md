# shiftIn() #

## Description ##
Shifts in a byte of data one bit at a time. Starts from either the most (i.e. the leftmost) or least (rightmost) significant bit. For each bit, the clock pin is pulled high, the next bit is read from the data line, and then the clock pin is taken low.<br>
If you're interfacing with a device that's clocked by rising edges, you'll need to make sure that the clock pin is low before the first call to shiftIn(), e.g. with a call to digitalWrite(clockPin, LOW).<br>
<br>
<h2>Syntax</h2>
shiftIn(dataPin, clockPin, bitOrder)<br>
<br>
<h2>Parameters</h2>
dataPin: the pin on which to input each bit.<br>
clockPin: the pin to toggle to signal a read from dataPin.<br>
bitOrder: which order to shift in the bits; either MSBFIRST or LSBFIRST.<br>
(Most Significant Bit First, or, Least Significant Bit First)<br>
<br>
<h2>Returns</h2>
the value read (BYTE).