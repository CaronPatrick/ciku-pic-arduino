# Serial\_printString() #

## Description ##
Prints data to the serial port as human-readable ASCII text.

## Syntax ##
Serial\_printString(string)

## Parameters ##
The string to be print - const char.

## Returns ##
None.

## Example ##
```
int incomingByte = 0;

void setup()
{
  Serial_begin(9600); // opens serial port, sets data rate to 9600 bps
}

void loop()
{
  if(Serial_available() > 0)
  {
    incomingByte = Serial_read();
    Serial_printString("I received: ");
    Serial_write(incomingByte);
  }
}
```