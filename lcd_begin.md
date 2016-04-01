# lcd\_begin() #

## Description ##
Initializes the interface to the LCD screen, and specifies the dimensions (width and height) of the display. lcd\_begin() needs to be called before any other LCD library commands.

## Syntax ##
lcd\_begin(cols, rows)

## Parameters ##
cols: the number of columns that the display has.<br>
rows: the number of rows that the display has.<br>
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