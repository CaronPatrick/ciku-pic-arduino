# millis() #

## Description ##
Returns the number of milliseconds since the CIKU board began running the current program. This number will overflow (go back to zero), after approximately 50 days.

## Syntax ##
millis()

## Parameters ##
None.

## Returns ##
Number of milliseconds since the program started (unsigned long).

## Example ##
```
unsigned long previousMillis = 0;
int interval = 1000;

void setup()
{
  pinMode(LED, OUTPUT); // sets the digital pin as output
}

void loop()
{
  unsigned long currentMillis = millis(); // read current millis
  if(currentMillis - previousMillis > interval) // after 1 seconds
  {
    previousMillis = currentMillis;
    digitalToggle(LED); // toggle LED state
  }
}
```