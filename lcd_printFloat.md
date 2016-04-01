# lcd\_printFloat() #

## Description ##
Prints floating number to the LCD.

## Syntax ##
lcd\_printFloat(number, point)

## Parameters ##
number: the floating number to be printed - double.<br>
point: number of decimal point.<br>
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
  Serial_printFloat(34.567, 2); // result display 34.57<br>
}<br>
<br>
void loop()<br>
{<br>
  <br>
}<br>
</code></pre>