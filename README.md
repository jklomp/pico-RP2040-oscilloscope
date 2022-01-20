# pico-RP2040-oscilloscope

This project shows how a Raspberry Pi Pico board can be used as a low frequency oscilloscope. The RP2040 sampling speed is limited to 500ks/s. The board communicates via an USB serial interface with an user program written in HTML / Javascript that uses the Web Serial API for communication. At the moment of writing this API is only supported by Chrome, Edge and Opera. <br>
The program for the Pico is written in C and requires the Pico SDK for compiling. An .uf2 file is available for programming the board without use of the SDK.<br>
The user interface is simple: adjust the position of the vertical green line to change the default 50% trigger position and adjust the horizontal green line to set the trigger level. Other settings are done with checkboxes and sliders.<br>
One of the PWM's on the Pico is programmed as pulse generator with frequency and duty cycle setting in the user interface.<br>

The connections on the Pico board are: <br>
GP26 : analog input for channel 1, input range 0-3.3 V <br>
GP27 : analog input for channel 2, input range 0-3.3 V <br>
GP22 : digital output PWM pulse generator <br>


