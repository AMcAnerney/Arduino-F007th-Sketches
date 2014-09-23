Arduino-F007th-Sketches
=======================

F007th Ambient F007th Thermo-Hygrometer

What this code does:

Captures Ambient F007th Thermo-Hygrometer data packets by identifying a header of at least 10 rising edges (manchester encoding binary 1s), synching the data within byte boundaries, and distinguishing between F007th data packets and other 434Mhz signals with equivalent header by checking value of sensor ID byte.
   
Correctly identifies positive and negative temperature values for up to 8 channels.
   
Correctly identifies humidity values for up to 8 channels.

Error checks data by rejecting humidity value outside the range 1 to 100%, humidity changes of more than 5% per minute and temperature changes of 1.5C per minute or greater.

Sends the data by wifi to Xively / prints to Serial every 5 minutes.
