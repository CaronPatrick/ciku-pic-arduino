# analogWrite() #

## Description ##
Writes an analog value (PWM wave) to a pin (5 and 6). Can be used to light a LED at varying brightnesses or drive a motor at various speeds. After a call to analogWrite(), the pin will generate a steady square wave of the specified duty cycle until the next call to analogWrite() (or a call to digitalRead() or digitalWrite() on the same pin). The frequency of the PWM signal on both pins is approximately 2.44kHz.<br>
You do not need to call pinMode() to set the pin as an output before calling analogWrite().<br>
The analogWrite function has nothing to do with the analog pins or the analogRead function.<br>
<br>
<h2>Syntax</h2>
analogWrite(pin, value)<br>
<br>
<h2>Parameters</h2>
pin: the pin to write to (only available on pin 5 and 6).<br>
value: the duty cycle: between 0 (always off) and 1023 (always on).<br>
<br>
<h2>Returns</h2>
None.<br>
<br>
<h2>Example</h2>
<pre><code>int analogPin = A0;<br>
int pwmPin = 5;<br>
<br>
void setup()<br>
{<br>
  pinMode(analogPin, INPUT); // sets analogPin as input<br>
  pinMode(pwmPin, OUTPUT);   // sets pwmPin as output<br>
}<br>
<br>
void loop()<br>
{<br>
  int adc = analogRead(A0); // read the voltage value on analog pin<br>
  analogWrite(pwmPin, adc); // control output pin using pwm base on adc value<br>
  delay(10); // waits for 10ms<br>
}<br>
</code></pre>