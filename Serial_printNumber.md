# Serial\_printNumber() #

## Description ##
Prints data to the serial port as human-readable ASCII text.

## Syntax ##
Serial\_printNumber(number, base)

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
  Serial_begin(9600); // opens serial port, sets data rate to 9600 bps<br>
  Serial_printNumber(1234, DEC);<br>
}<br>
<br>
void loop()<br>
{<br>
  <br>
}<br>
</code></pre>