# Gas-Pedal
Simulating a control logic of a gas pedal system using MATLAB/Simulink and Stateflow, after that generating a code with Embedded Coder, finally implementing the code in ARM (STM32) using Eclipse.


# Project Requirements:<br>
. Implement SW that output the gas pedal percentage (0-100%).<br>
. The pedal has two sensors (potentiometers) opposite to each other.<br>
. Each sensor outputs voltage based on pressed angle from 0 to 3.3V
  0.3V means 0% and 3V means 100%.<br>
. Voltage less than 0.3V and more than 3V means there is short circuit in the sensor. So the system should enter degraded mode.<br>
. If one sensor has short circuit the max output should be 20% <br>
. If two sensors have short circuit the system should enter total fault state and the output should 0%.<br>
