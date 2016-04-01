# lcd\_write() #

## Description ##
Write a character to the LCD.

## Syntax ##
lcd\_write(data)

## Parameters ##
data: the character to write to the display.

## Returns ##
None.
## Examples ##
```
#include "LiquidCrystal.h"

void setup()
{
  lcd_4bit(8, 9, 4, 5, 6, 7);
  lcd_begin(16, 2);
  Serial_begin(9600);
}

void loop()
{
  if(Serial_available())
  {
    lcd_write(Serial_read());
  }
}
```