# SSerial\_available() #

## Description ##
Get the number of bytes (characters) available for reading from the software serial port (pin 2 and 3). This is data that's already arrived and stored in the serial receive buffer (which holds 64 bytes).

## Syntax ##
SSerial\_available()

## Parameters ##
None.

## Returns ##
The number of bytes available to be read.

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