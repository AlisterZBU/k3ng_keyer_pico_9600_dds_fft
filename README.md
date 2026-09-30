This a a fork of K3NG's excellent Winkeyer for the Arduino IDE, and runs with an R-Pi Pico.
I have built many K3NG Winkeyers in the past, using Arduinos, but the small memory capacity
means that many functions cannot be used. The Pico has much more memory and can be programmed via the
Arduino IDE.

I have made some small changes to allow the Pico to be used.

It converts ASCII characters sent via USB serial comms at 9,600Bd into CW. 

Normally the Winkeyer default speed is 1,200Bd, but anything sent at that speed will
automatically reset the Pico. 

I have a SerialDiverter to convert between those two speeds, and that allows bog-standard
loggers such as SD.EXE by EI5DI to work.

The output pin energises an opto-coupler so there is no need to get unwanted earth currents. I use 4N35 devices.
There are two opto-couplers for the iambic DOT and DASH inputs, but that is also optional.
Finally I have a 10k ohm pot as speed control.
I have added an optional DDS for experimental purposes, but that may be left out.
There is also a display, optional!
