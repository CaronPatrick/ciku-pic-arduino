# pinMode() #

## Description ##
Configures the specified pin to behave either as an input or an output.

## Syntax ##
pinMode(pin, mode)

## Parameters ##
pin: the number of the pin whose mode you wish to set.<br>
mode: INPUT, OUTPUT.<br>
<br>
<h2>Returns</h2>
None.<br>
<br>
<h2>Example</h2>
<pre><code>void setup()<br>
{<br>
  pinMode(LED, OUTPUT);      // sets the digital pin as output<br>
}<br>
<br>
void loop()<br>
{<br>
  digitalWrite(LED, HIGH);   // sets the LED on<br>
  delay(1000);                  // waits for a second<br>
  digitalWrite(LED, LOW);    // sets the LED off<br>
  delay(1000);                  // waits for a second<br>
}<br>
</code></pre>