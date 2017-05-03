This is an isolated power supply PCB for Texas Instrument's C2000 Launchpad (LAUNCHXL-F28027) Kit.

C2000 Launchpad is equipped with two ISO72XX chips for isolated JTAG and UART.
To achieve isolation, the MCU has to be powered up on it's side.

As I needed the Launchpad for fast prototyping of other projects (having a PWM generator, gathering some ADC data etc.), I've came up with this little plug-in board.
It will power up the MCU on it's side from the available USB debugger/programmer voltage and provide full isolation.

I find it really handy as one avoids ground loops, which might be a source of noise or other problems in the circuit.

I've used this PCB to get a simple isolated PWM generator as well as isolated ADC measurements (check out my other repositories).
The isolation is limited by the Launchpad itself and I would certainly not go with it above 1kV potential difference (look at the small clearance in the Launchpad PCB).

The isolated power supply board only takes 3.3V from the Launchpad and provides isolated 3.3V, so 5V is not available anymore on the MCU side (the jumper must be disconnected!).
The maximum output current of this supply is limited mainly by the transformer and transformer driver chip and is around 150mA.
However, I would not go above 100mA load, just for precaution.

The PCB was designed in KiCad 2013-07-07.
It's not prepared for mass production.
I did it without soldermask/silkscreen/paste layers. Just hand-soldered myself.

Those layers are available in the project, though.
If you want to order that PCB using the gerbers, look out for the clearance of the connector's pads (P1 and P2).
I've made the pads really small compared to the drill size on purpose!
You might need to change those depending on your choice of PCB manufacturer and their DRC.

Stawiski