# Timer2 CTC Example
This is an example program for AVR microcontroller that uses Timer2 in CTC mode to toggle an LED on and off every specified time interval using the Timer2 compare match interrupt.

## Getting Started
### Prerequisites
To run this example, you will need the following:

* An AVR microcontroller with Timer2
* AVR programming software (e.g. Atmel Studio, Arduino IDE)
* A LED connected to PB5 pin (or any other available digital output pin)
### Installing
1. Connect the LED to PB5 pin (or any other available digital output pin) on the microcontroller.
2. Load the program onto the microcontroller using AVR programming software.
### Running the Example
Once the program is loaded onto the microcontroller, the LED should start to blink on and off every specified time interval (in this case, 125 clock cycles).

### Code Explanation
The program sets up Timer2 in CTC mode with a specified TOP value, and then enables the Timer2 compare match interrupt. The ISR increments a timerCount variable on every interrupt and toggles the LED when the variable reaches the specified TOP value. The main program loop is empty as all timing and pin toggling is handled by the Timer2 compare match interrupt.

The program can be customized by changing the TOP value to adjust the time interval between LED toggles, and by changing the pin number for the LED output.
