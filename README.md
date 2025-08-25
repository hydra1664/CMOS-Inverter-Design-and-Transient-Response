# CMOS Inverter Design and Transient Response

## Project overview
I designed and simulated a CMOS inverter using 180 nm process models to study its transient switching behavior. The aim was to build a simple inverter and verify its logic-level switching when driven by a pulse input.

## Components and setup
- Transistors: PMOS and NMOS (SOI7336ADP models)
- Supply: Vdd = 2 V
- Input: Vin = pulse (0 V to 2 V), Ton = 10 ns, Period = 20 ns
- Technology: 180 nm SPICE model file (included)
- Device geometry: L = 180 nm for both devices; Wp = 900 nm, Wn = 360 nm
- Simulation: Transient analysis, stop time = 100 ns
- Tool used: LTSpice

## Circuit description
The inverter is a standard CMOS configuration:
- PMOS source tied to Vdd, drain connected to output.
- NMOS drain also connected to output, source grounded.
- Both gates driven by the same input pulse source.
- SPICE directive included to import the 180 nm model file.

## How to run the simulation
1. Open the schematic from the folder Circuit Files in LTSpice.
2. Make sure the 180 nm model file is available in the same folder.
3. Run a transient analysis for 100 ns.
4. Plot Vin, Vout, and I(Vdd) to observe switching and power behavior.

## Observations
<img width="1920" height="1080" alt="CMOS_Invertor" src="https://github.com/user-attachments/assets/bc427e02-66ab-4690-aa12-d3587d00fa8f" />

- The output cleanly inverts the input with sharp transitions.
- Switching is consistent with expected digital logic.
- The current through Vdd shows activity during switching events, as expected for a CMOS inverter.

## Conclusion
The CMOS inverter performed as expected under simulation. Proper transistor sizing (Wp = 900 nm, Wn = 360 nm) and a clean supply enabled predictable digital operation with sharp edges and correct inversion.

## Files included
- All circuit files are available in the folder named Circuit Files.  
- The image containing both the circuit schematic and waveform plots (Vin, Vout, and I(Vdd)) is available in the folder named Images.
