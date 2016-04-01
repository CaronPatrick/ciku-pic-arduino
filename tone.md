# tone() #

## Description ##
Generates a square wave of the specified frequency (and 50% duty cycle) on a pin. A duration can be specified, otherwise the wave continues until a call to noTone(). The pin can be connected to a piezo buzzer or other speaker to play tones.<br>
Only one tone can be generated at a time.<br>
<br>
<h2>Syntax</h2>
tone(pin, frequency, duration)<br>
<br>
<h2>Parameters</h2>
pin: the pin on which to generate the tone.<br>
frequency: the frequency of the tone in hertz - unsigned int.<br>
duration: the duration of the tone in milliseconds - unsigned long.<br>
<br>
<h2>Returns</h2>
None.