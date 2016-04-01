# Serial\_printFloat() #

## Description ##
Prints data to the serial port as human-readable ASCII text.

## Syntax ##
Serial\_printFloat(number, point)

## Parameters ##
number: the floating number to be print - double.<br>
point: number of decimal point.<br>
<br>
<h2>Returns</h2>
None.<br>
<br>
<h2>Example</h2>
<pre><code>void setup()<br>
{<br>
  Serial_begin(9600); // opens serial port, sets data rate to 9600 bps<br>
  Serial_printFloat(34.567, 2); // result display 34.57<br>
}<br>
<br>
void loop()<br>
{<br>
  <br>
}<br>
</code></pre>