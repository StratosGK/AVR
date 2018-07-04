NEC IR Protocol for ATMega32A
	by Stratos Gkagkanis

Hardware
Fcpu = 16MHz
PA.0 = Button
PD.5 = IR LED

Software
The code presented here creates pulse bursts in order to drive an IR LED.
The IR Protocol used is "NEC Infared Transmission Protocol"
The procedure is not hardcoded to send only a specific command.
On/Off command of an LG TV is used as an example but it can send anything
and with some modifications the program could send more than one commands.

Tasks:
1)Lead code transmission.
  Pulse burst duration is 9ms and it is followed by 4.5ms of LOW signal.
2)Data transmission, starting with the LSB.
3)End code transmission.
  Pulse burst duration is 564μs.
