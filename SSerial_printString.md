# SSerial\_printString() #

## Description ##
Prints data to the transmit pin of the software serial port (pin 3).

## Syntax ##
SSerial\_printString(string)

## Parameters ##
The string to be print - const char.

## Returns ##
None.

## Example ##
```
int incomingByte = 0;

void setup()
{
  SSerial_begin(9600); // opens serial port, sets data rate to 9600 bps
}

void loop()
{
  if(SSerial_available() > 0)
  {
    incomingByte = SSerial_read();
    SSerial_printString("I received: ");
    SSerial_write(incomingByte);
  }
}
```