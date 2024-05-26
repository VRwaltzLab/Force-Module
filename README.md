# Force-Module
Bottom Layer of the Drone project from a code perspective.
Goal: Get a single motor to make the appropriate force.

Like with many projects, I am going to attempt to build a large thing by a sequence of adjustments, and many layeres.
Planned Sequence:
## Layer Force-Module Speed to controller effort
0.  Just send pwm to the motor controller and get a reliable %Battery voltage output.
1.  Measure Battery voltage and get a reliable voltage output or do max voltage.
2.  Measure Battery Voltage and get a reliable speed by calculating motor equation.
3.  Measure Battery Voltage and get a reliable speed output via PF loop
4.  Version 2 but add ID terms.
## layer Force-Module Force to Speed
0.  %Force -> %Speed^2
1.  Force ->CONSTANT * Speed^2 ; Compute a constant for my testroom pressure and temperature, and a specific rotors.
2.  Force ->CONSTANT * Speed^2 ; Use a formula for the constant in terms of general pressure and temperature.
3.  Force ->CONSTANT * Speed^2 ; Read those values at setuptime (possibly from off robot)
