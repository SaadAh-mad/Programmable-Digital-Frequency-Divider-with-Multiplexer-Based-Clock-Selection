# Programmable-Digital-Frequency-Divider-with-Multiplexer-Based-Clock-Selection
Digital Frequency Divider with MUX-Based Clock Selection : Designed a clock divider using a 555 timer and JK flip-flops to generate f/2, f/3, and f/4. Implemented a MOD-3 counter and used a 4×1 multiplexer for real-time frequency selection via switches. Demonstrates sequential logic and clock scaling.

🔧Components Used

NE555 Timer IC
IC 7476 (JK Flip-Flop)
2× D Flip-Flop ICs ( 74LS74)
IC 7408 (AND Gate)
IC 7432 (OR Gate)
IC 74153 (4×1 Multiplexer)
2× SPDT switches
Capacitors: 220 µF, 0.1 µF, 0.01 µF
Resistors:
2× 1 kΩ
2× 220 Ω
3× 330 Ω
LEDs
Breadboard and connecting wires
Arduino UNO (used as 5 V power supply)

⚙️Working

A master clock signal is generated using the NE555 timer in astable mode by selecting appropriate resistor and capacitor values. Small decoupling capacitors (0.01 µF and 0.1 µF) are used to stabilize the supply and reduce voltage spikes.
The generated clock is then passed through sequential circuits for frequency division. JK flip-flops configured in toggle mode are used to obtain 𝑓/2 and 𝑓/4. A MOD-3 counter is implemented using D flip-flops and logic gates to generate 𝑓/3
All divided outputs are produced simultaneously and fed into a 4×1 multiplexer (74153). Using SPDT switches as select inputs, the desired output frequency is chosen and observed through LEDs.

⚠️Challenges Faced

Incorrect wiring of flip-flop pins (especially power and control pins) caused outputs to remain constant.
LEDs initially did not blink due to high clock frequency from improper R–C selection in the 555 timer.
Debugging was required to ensure proper connections of preset/clear pins and correct logic levels for stable operation.

📈Results

The circuit successfully generates divided frequencies f, f/2, f/3, and f/4.
The difference in frequency is clearly visible through varying LED blinking rates.
The output can also be verified using an oscilloscope for accurate frequency measurement.

##🚀Future Improvements

Replace 555 timer with a crystal oscillator for improved accuracy and stability
Implement synchronous counters to reduce propagation delay
Add a 7-segment display to visualize frequency/counting behavior
Integrate microcontroller-based measurement for precise frequency readout
