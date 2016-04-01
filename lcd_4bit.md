# lcd\_4bit() #

## Description ##
Set CIKU IO to be connected to LCD pins for 4 bit mode.

## Syntax ##
lcd\_4bit(rs, enable, d4, d5, d6, d7)

## Parameters ##
rs: the number of the CIKU pin that is connected to the RS pin on the LCD.<br>
enable: the number of the CIKU pin that is connected to the enable pin on the LCD.<br>
d4, d5, d6, d7: the numbers of the CIKU pins that are connected to the corresponding data pins on the LCD.<br>
<br>
<h2>Returns</h2>
None.<br>
<br>
<h2>Example</h2>
<pre><code>#include "LiquidCrystal.h"<br>
<br>
void setup()<br>
{<br>
  lcd_4bit(8, 9, 4, 5, 6, 7);<br>
  lcd_begin(16, 2);<br>
  lcd_printString("Hello World!");<br>
}<br>
<br>
void loop()<br>
{<br>
<br>
}<br>
</code></pre>