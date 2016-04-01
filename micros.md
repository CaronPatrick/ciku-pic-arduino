# micros() #

## Description ##
Returns the number of microseconds since the CIKU board began running the current program. This number will overflow (go back to zero), after approximately 70 minutes.<br>
Note: there are 1,000 microseconds in a millisecond and 1,000,000 microseconds in a second.<br>
<br>
<h2>Syntax</h2>
micros()<br>
<br>
<h2>Parameters</h2>
None.<br>
<br>
<h2>Returns</h2>
Number of microseconds since the program started (unsigned long).<br>
<br>
<h2>Example</h2>
<pre><code>unsigned long currentMicros = 0;<br>
int interval = 100000;<br>
<br>
void setup()<br>
{<br>
  pinMode(LED, OUTPUT); // sets the digital pin as output<br>
}<br>
<br>
void loop()<br>
{<br>
  unsigned long currentMicros = micros(); // read current millis<br>
  if(currentMicros - currentMicros &gt; interval) // after 100ms<br>
  {<br>
    currentMicros = currentMicros;<br>
    digitalToggle(LED); // toggle LED state<br>
  }<br>
}<br>
</code></pre>