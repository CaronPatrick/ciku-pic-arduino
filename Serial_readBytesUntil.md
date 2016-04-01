# Serial\_readBytesUntil() #

## Description ##
Serial\_readBytesUntil() reads characters from the serial buffer into an array. The function terminates if the terminator character is detected, the determined length has been read, or it times out.<br>
Serial_readBytesUntil() returns the number of characters read into the buffer. A 0 means no valid data was found.<br>
<br>
<h2>Syntax</h2>
Serial_readBytesUntil(character, buffer, length)<br>
<br>
<h2>Parameters</h2>
character: the character to search for - char.<br>
buffer: the buffer to store the bytes in - char<a href='.md'>.md</a>.<br>
length: the number of bytes to read - int.<br>
<br>
<h2>Returns</h2>
The number of characters read into the buffer.