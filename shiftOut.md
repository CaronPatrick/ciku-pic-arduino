# shiftOut() #

## Description ##
Shifts out a byte of data one bit at a time. Starts from either the most (i.e. the leftmost) or least (rightmost) significant bit. Each bit is written in turn to a data pin, after which a clock pin is pulsed (taken high, then low) to indicate that the bit is available.<br>
Note: if you're interfacing with a device that's clocked by rising edges, you'll need to make sure that the clock pin is low before the call to shiftOut(), e.g. with a call to digitalWrite(clockPin, LOW).<br>
<br>
<h2>Syntax</h2>
shiftOut(dataPin, clockPin, bitOrder, value)<br>
<br>
<h2>Parameters</h2>
dataPin: the pin on which to output each bit.<br>
clockPin: the pin to toggle once the dataPin has been set to the correct value.<br>
bitOrder: which order to shift out the bits; either MSBFIRST or LSBFIRST.<br>
(Most Significant Bit First, or, Least Significant Bit First)<br>
value: the data to shift out. (BYTE)<br>
<br>
<h2>Returns</h2>
None.<br>
<br>
<h2>Note</h2>
The dataPin and clockPin must already be configured as outputs by a call to pinMode().<br>
shiftOut is currently written to output 1 byte (8 bits) so it requires a two step operation to output values larger than 255.<br>
<pre><code>// Do this for MSBFIRST serial<br>
int data = 500;<br>
// shift out highbyte<br>
shiftOut(dataPin, clock, MSBFIRST, (data &gt;&gt; 8));  <br>
// shift out lowbyte<br>
shiftOut(dataPin, clock, MSBFIRST, data);<br>
<br>
// Or do this for LSBFIRST serial<br>
data = 500;<br>
// shift out lowbyte<br>
shiftOut(dataPin, clock, LSBFIRST, data);  <br>
// shift out highbyte <br>
shiftOut(dataPin, clock, LSBFIRST, (data &gt;&gt; 8)); <br>
</code></pre>