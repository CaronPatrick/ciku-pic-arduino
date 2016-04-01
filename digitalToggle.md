# digitalToggle() #

## Description ##
Toggle state of the output digital pin.

## Syntax ##
digitalToggle(pin)

## Parameters ##
pin: the pin number.

## Returns ##
None.

## Example ##
```
void setup()
{
  pinMode(LED, OUTPUT); // sets the LED as output
}

void loop()
{
  digitalToggle(LED, HIGH); // toggle the LED state
  delay(1000);              // waits for a second
}
```