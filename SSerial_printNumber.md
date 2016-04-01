# SSerial\_printNumber() #

## Description ##
Prints data to the transmit pin of the software serial port (pin 3).

## Syntax ##
SSerial\_printNumber(number, base)

## Parameters ##
number: the number to be print - long.<br>
base: specifies the base of the number to be printed (BIN, OCT, DEC, HEX).<br>
<br>
<h2>Returns</h2>
None.<br>
<br>
<h2>Example</h2>
<pre><code>void setup()<br>
{<br>
  SSerial_begin(9600); // opens serial port, sets data rate to 9600 bps<br>
  SSerial_printNumber(1234, DEC);<br>
}<br>
<br>
void loop()<br>
{<br>
  <br>
}<br>
</code></pre>