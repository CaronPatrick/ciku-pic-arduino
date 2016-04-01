# Serial\_begin() #

## Description ##
Sets the data rate in bits per second (baud) for UART (pin RX and TX) serial data transmission. For communicating with the computer, use one of these rates: 1200, 2400, 4800, 9600, 19200, 38400, 57600, or 115200. You can, however, specify other rates - for example, to communicate over pins 0 and 1 with a component that requires a particular baud rate.

## Syntax ##
Serial\_begin(speed)

## Parameters ##
speed: in bits per second (baud) - long.

## Returns ##
None.

## Example ##
```
void setup()
{
  Serial_begin(9600); // opens serial port, sets data rate to 9600 bps
  Serial_printString("Hello World!");
}

void loop()
{
  
}
```