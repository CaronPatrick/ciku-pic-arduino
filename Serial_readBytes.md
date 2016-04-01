# Serial\_readBytes() #

## Description ##
Serial\_readBytes() reads characters from the serial port into a buffer. The function terminates if the determined length has been read.<br>
Serial_readBytes() returns the number of characters placed in the buffer. A 0 means no valid data was found.<br>
<br>
<h2>Syntax</h2>
Serial_readBytes(buffer, length)<br>
<br>
<h2>Parameters</h2>
buffer: the buffer to store the bytes in - char<a href='.md'>.md</a>.<br>
length: the number of bytes to read - int.<br>
<br>
<h2>Returns</h2>
The number of characters placed in the buffer.