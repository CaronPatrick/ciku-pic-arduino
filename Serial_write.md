# Serial\_write() #

## Description ##
Writes binary data to the serial port. This data is sent as a byte.

## Syntax ##
Serial\_write(val)

## Parameters ##
val = a value to send as a single byte.

## Returns ##
1.

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