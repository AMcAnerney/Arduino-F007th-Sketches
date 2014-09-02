Arduino-F007th-Sketches
=======================

F007th Ambient F007th Thermo-Hygrometer

What this code does:

Captures Ambient F007th Thermo-Hygrometer data packets by;

Identifying a header of at least 10 rising edges (manchester encoding binary 1s),
Synching the data within byte boundaries
Distinguishes between F007th data packets and other 434Mhz signals with equivalent header by checking value of sensor ID byte 
   
Correctly identifies positive and negative temperature values for up to 8 channels
   
Correctly identifies humidity values for up to 8 channels 8 channels
   
Prints data for all channels to the serial port every 5 minutes
   
Error checks data by rejecting;
humidity value outside the range 1 to 100%
temperature changes of 10C per minute or greater

What it will do soon;

Send the data by wifi to a website
