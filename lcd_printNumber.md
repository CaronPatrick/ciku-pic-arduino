# lcd\_printNumber() #

## Description ##
Prints number to the LCD.

## Syntax ##
lcd\_printNumber(number, base)

## Parameters ##
number: the number to be printed - long.<br>
base: specifies the base of the number (BIN, OCT, DEC, HEX).<br>
<br>
<h2>Returns</h2>
None.<br>
<br>
<h2>Examples</h2>
<pre><code>#include "LiquidCrystal.h"<br>
<br>
void setup()<br>
{<br>
  lcd_4bit(8, 9, 4, 5, 6, 7);<br>
  lcd_begin(16, 2);<br>
  Serial_printNumber(1234, DEC);<br>
}<br>
<br>
void loop()<br>
{<br>
  <br>
}<br>
</code></pre>