# lcd\_printString() #

## Description ##
Prints text to the LCD.

## Syntax ##
lcd\_printString(string)

## Parameters ##
string: the string to be printed.

## Returns ##
None.

## Examples ##
```
#include "LiquidCrystal.h"

void setup()
{
  lcd_4bit(8, 9, 4, 5, 6, 7);
  lcd_begin(16, 2);
  Serial_printString("Hello World!");
}

void loop()
{
  
}
```