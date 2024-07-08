# Force-Module
Bottom Layer of the Drone project from a code perspective.
Goal: Get a single motor to make the appropriate force.
Deliverable: a Force vs Latency graph for at least one design with fixed electrical components.
Like with many projects, I am going to attempt to build a large thing by a sequence of adjustments, and many layers.
Planned Sequence:
## Layer Physical
0. Minimum TestBed: 2 batteries, 1 motor, 1 motor controller, 1 microcontroller.
## Layer Contoller Effort to PWM Signal
Read documentation on the motor controllers that I bought. Go from there.

## Layer Speed to controller effort
0.  Just send pwm to the motor controller and get a reliable %Battery voltage output.
1.  Measure Battery voltage and get a reliable voltage output or do max voltage.
2.  Measure Battery Voltage and get a reliable speed by calculating motor equation.
3.  Measure Battery Voltage and get a reliable speed output via PF loop
4.  Version 2 but add ID terms.
## Layer Force to Speed
0.  %Force -> %Speed^2
1.  Force ->CONSTANT * Speed^2 ; Compute a constant for my testroom pressure and temperature, and a specific rotors.
2.  Force ->CONSTANT * Speed^2 ; Use a formula for the constant in terms of general pressure and temperature.
3.  Force ->CONSTANT * Speed^2 ; Read those values at setuptime (possibly from off robot)
# Mulitple Rotors Decision Defense:
While trying to get the desired amount of force (8oz-5 lbs ) in the desired amount of lag (.5 frames at 120fps) might require more expensive motors or an array of rotors,
that extra complexity is far outside the minimum viable product which we want to make first.
Furthermore different designs of force arrangements will have different difficulties with adding more rotors.
