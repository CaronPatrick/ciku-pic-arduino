# digitalRead() #

## Description ##
Reads the value from a specified digital pin, either HIGH or LOW.

## Syntax ##
digitalRead(pin)

## Parameters ##
pin: the number of the digital pin you want to read (int)

## Returns ##
HIGH or LOW.

## Example ##
```
int inPin = 7; // pushbutton connected to digital pin 7
int val = 0;   // variable to store the read value

void setup()
{
  pinMode(LED, OUTPUT);  // sets the LED as output
  pinMode(inPin, INPUT); // sets the digital pin 7 as input
}

void loop()
{
  val = digitalRead(inPin); // read the input pin
  digitalWrite(LED, val);   // sets the LED to the button's value
}
```