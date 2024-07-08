# Bug Report
So when I went to go program the Turnigy plush 32 Motor Controllers.
I found out from their manual that they have "8-24 KHz PWM signal output"
This doesn't make sense as written. I suspect they meant input.
If the engineers meant input, then we have a problem because Arduino Controllers such as the Adafruit Metro I have on hand can't produce a PWM signal that fast.
Thus, I needed to buy Rasberry Pi controllers which I have done. 
I am worried that the hardware PWM signals will work from the PI,
but the software PWM signals might not work to control the controllers I have.
This could cause a larger problem of not being able to control all 8 motor controllers from 1 pi, but I'll cross that bridge later.
