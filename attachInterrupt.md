# attachInterrupt() #

## Description ##
Specifies a named Interrupt Service Routine (ISR) to call when an interrupt occurs. Replaces any previous function that was attached to the interrupt. CIKU board have 3 external interrupt: number 0 (SDA), number 1 (SCL) and number 2 (pin 2).

## Note ##
Inside the attached function, delay() won't work and the value returned by millis() will not increment. Serial data received while in the function may be lost. You should declare as volatile any variables that you modify within the attached function. See the section on ISRs below for more information.

## Using Interrupt ##
Interrupts are useful for making things happen automatically in microcontroller programs, and can help solve timing problems. Good tasks for using an interrupt may include reading a rotary encoder, or monitoring user input.<br>
If you wanted to insure that a program always caught the pulses from a rotary encoder, so that it never misses a pulse, it would make it very tricky to write a program to do anything else, because the program would need to constantly poll the sensor lines for the encoder, in order to catch pulses when they occurred. Other sensors have a similar interface dynamic too, such as trying to read a sound sensor that is trying to catch a click, or an infrared slot sensor (photo-interrupter) trying to catch a coin drop. In all of these situations, using an interrupt can free the microcontroller to get some other work done while not missing the input.<br>
<br>
<h2>About Interrupt Service Routine</h2>
ISRs are special kinds of functions that have some unique limitations most other functions do not have. An ISR cannot have any parameters, and they shouldn't return anything.<br>
Generally, an ISR should be as short and fast as possible. If your sketch uses multiple ISRs, only one can run at a time, other interrupts will be ignored (turned off) until the current one is finished. as delay() and millis() both rely on interrupts, they will not work while an ISR is running. delayMicroseconds(), which does not rely on interrupts, will work as expected.<br>
Typically global variables are used to pass data between an ISR and the main program. To make sure variables used in an ISR are updated correctly, declare them as volatile.<br>
<br>
<h2>Syntax</h2>
attachInterrupt(interrupt, ISR, mode)<br>
<br>
<h2>Parameters</h2>
interrupt: the number of the interrupt (EXTERNAL_INT_0 or EXTERNAL_INT_1 or EXTERNAL_INT_2).<br>
ISR: the ISR to call when the interrupt occurs; this function must take no parameters and return nothing. This function is sometimes referred to as an interrupt service routine. Must put the function prototype too.<br>
mode: defines when the interrupt should be triggered. Two constants are predefined as valid values:<br>
RISING to trigger when the pin goes from low to high,<br>
FALLING for when the pin goes from high to low.<br>
<br>
<h2>Returns</h2>
None.<br>
<br>
<h2>Example</h2>
<pre><code>void blink();<br>
<br>
volatile int state = LOW;<br>
<br>
void setup()<br>
{<br>
  pinMode(pin, OUTPUT);<br>
  attachInterrupt(EXTERNAL_INT_0, blink, RISING);<br>
}<br>
<br>
void loop()<br>
{<br>
  digitalWrite(LED, state);<br>
}<br>
<br>
void blink()<br>
{<br>
  state = !state;<br>
}<br>
</code></pre>