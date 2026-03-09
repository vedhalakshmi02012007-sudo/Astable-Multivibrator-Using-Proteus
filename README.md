## Experiment No: 5
ASTABLE MULTIVIBRATOR USING 555 TIMER Using Proteus
## Aim
To design and simulate an Astable Multivibrator using NE555 in Proteus Design Suite and observe the continuous square wave output.
## Apparatus Required
•	NE555 Timer IC
•	Resistor R1 = 10 kΩ
•	Resistor R2 = 100 kΩ
•	Capacitor C = 0.01 µF
•	DC Power Supply (5V or 9V)
•	CRO / Oscilloscope
•	Connecting wires
## Circuit Diagram
<img width="1919" height="1142" alt="Screenshot 2026-02-13 091103" src="https://github.com/user-attachments/assets/e64c8f53-22bd-4375-a3ec-7dc6f4b73f97" />

Pin Configuration of 555 Timer:
•	Pin 1 → Ground
•	Pin 2 → Trigger
•	Pin 3 → Output
•	Pin 4 → Reset (Connected to Vcc)
•	Pin 5 → Control Voltage (Bypass with 0.01 µF capacitor optional)
•	Pin 6 → Threshold
•	Pin 7 → Discharge
•	Pin 8 → Vcc
## Connections:
•	R1 → Between Vcc and Pin 7
•	R2 → Between Pin 7 and Pins 2 & 6
•	C → Between Pins 2 & 6 and Ground
•	Output → Pin 3
## Theory
•	The NE555 timer is a widely used integrated circuit for generating precise time delays and oscillations. When operated in astable mode, it functions as a free-running oscillator that continuously produces a square wave without any external triggering signal. In this mode, a capacitor connected to the circuit charges through resistors R1 and R2 and discharges through R2 repeatedly. The internal voltage divider of the 555 timer creates two reference levels at 1/3 Vcc and 2/3 Vcc. 
•	When the capacitor voltage reaches 2/3 Vcc, the upper comparator resets the flip-flop and turns ON the discharge transistor, causing the capacitor to discharge. When the voltage falls to 1/3 Vcc, the lower comparator sets the flip-flop, turning OFF the discharge transistor and allowing the capacitor to charge again. This continuous charging and discharging process generates a square wave at the output (Pin 3) and an exponential waveform across the capacitor. The time period of oscillation is given by T=0.693(R1+2R2)CT = 0.693 (R1 + 2R2) CT=0.693(R1+2R2)C, and the frequency depends on the values of R1, R2, and C. Thus, the 555 timer in astable mode acts as a simple and reliable square wave generator used in clock circuits, LED flashers, and pulse generation applications.
## Procedure
1.	Open Proteus software.
2.	Select NE555 IC, resistors, capacitor, and CRO.
3.	Connect circuit in astable configuration.
4.	Apply 5V supply.
5.	Run simulation.
6.	Observe square wave output at Pin 3.
7.	Measure time period and frequency.
## Tabulation
| S.No | R1 (kΩ) | R2 (kΩ) | C (µF) | Theoretical Frequency (Hz) | Practical Frequency (Hz) |
| ---- | ------- | ------- | ------ | -------------------------- | ------------------------ |
| 1    | 7.2     | 7.2     | 0.1    | 666.7                      | 660                      |
| 2    | 5       | 5       | 0.1    | 960                        | 950                      |
| 3    | 10      | 10      | 0.1    | 480                        | 470                      |
| 4    | 7.2     | 7.2     | 0.22   | 303                        | 295                      |
| 5    | 15      | 15      | 0.1    | 320                        | 310                      |

## Waveforms
<img width="1372" height="879" alt="Screenshot 2026-02-13 091527" src="https://github.com/user-attachments/assets/1c4a7edb-d57c-433c-a97c-9fa09f78b144" />

•	Output (Pin 3) → Square wave
•	Capacitor voltage → Exponential charging & discharging waveform
## Result
The Astable Multivibrator using NE555 Timer IC was successfully designed and simulated in Proteus.
A continuous square wave output was obtained.
The practical frequency closely matches the theoretical frequency.
## Conclusion
•	The 555 timer works as a free-running oscillator in astable mode.
•	Frequency depends on R1, R2, and C values.
•	Increasing R or C decreases frequency.
•	Used in clock generation, LED flashing, and tone generation.
## Viva Questions
1.	What are the operating modes of 555 timer?
The three operating modes of a 555 timer IC are:

Monostable mode – Produces one stable output pulse when triggered (one-shot).

Astable mode – Produces a continuous square wave without external triggering.

Bistable mode – Works as a flip-flop with two stable states (SET and RESET).

2.	What are the threshold levels in astable mode?
In astable mode, the capacitor voltage oscillates between:

Lower threshold = 1/3 Vcc

Upper threshold = 2/3 Vcc

When the voltage reaches 2/3 Vcc, the capacitor starts discharging.
When it falls to 1/3 Vcc, the capacitor starts charging again.

3.	Write the frequency formula.
3. Write the frequency formula.

Frequency of a 555 timer in astable mode:
​
<img width="304" height="92" alt="image" src="https://github.com/user-attachments/assets/596e8b21-cbd6-4886-9ec4-d2a9b8b32530" />


Where:

R1 = Resistor 1

R2 = Resistor 2

C = Capacitor

f = Output frequency

4.	What is duty cycle?
<img width="812" height="250" alt="image" src="https://github.com/user-attachments/assets/7a0c5ef9-6f0a-4f40-84d4-f1f845fead1d" />


5.	What happens if R2 increases?
If R2 increases:

Charging time increases

Discharging time increases

Total time period increases

Frequency decreases

Duty cycle increases
