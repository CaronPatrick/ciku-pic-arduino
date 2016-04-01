# Serial\_available() #

## Description ##
Get the number of bytes (characters) available for reading from the serial port. This is data that's already arrived and stored in the serial receive buffer (which holds 64 bytes).

## Syntax ##
Serial\_available()

## Parameters ##
None.

## Returns ##
The number of bytes available to be read.

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