# analogReference() #

## Description ##
Configures the reference voltage used for analog input (i.e. the value used as the top of the input range). The options are:<br>
<ul><li>DEFAULT: the default analog reference is equal to VDD (5 volts).<br>
</li><li>EXTERNAL: the voltage applied to the AREF pin (3V to 5V only) is used as the reference.</li></ul>

<h2>Syntax</h2>
analogReference(type)<br>
<br>
<h2>Parameters</h2>
type: DEFAULT or EXTERNAL.<br>
<br>
<h2>Returns</h2>
None.