# digitalWrite() #

## Description ##
Write a HIGH or a LOW value to a digital pin.<br>
If the pin has been configured as an OUTPUT with pinMode(), its voltage will be set to the corresponding value: 5V for HIGH, 0V (ground) for LOW.<br>
<br>
<h2>Syntax</h2>
digitalWrite(pin, value)<br>
<br>
<h2>Parameters</h2>
pin: the pin number.<br>
value: HIGH or LOW.<br>
<br>
<h2>Returns</h2>
None.<br>
<br>
<h2>Example</h2>
<pre><code>void setup()<br>
{<br>
  pinMode(LED, OUTPUT); // sets the LED as output<br>
}<br>
<br>
void loop()<br>
{<br>
  digitalWrite(LED, HIGH); // sets the LED on<br>
  delay(1000);             // waits for a second<br>
  digitalWrite(LED, LOW);  // sets the LED off<br>
  delay(1000);             // waits for a second<br>
}<br>
</code></pre>