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
. Coherency between the two sensors should be checked and if coherency error exist the system should enter total fault state.

# GasPedal Simulink Model:<br>
![GasPedal](https://user-images.githubusercontent.com/79062550/168006338-b49a07b2-ebcf-42d0-a589-0129e37819f7.PNG)

# ADC1 Subsystem:<br>
![ADC1](https://user-images.githubusercontent.com/79062550/168006562-52040a32-d8a0-4319-b426-f786b2a40db2.PNG)
# ADC2 Subsystem:<br>
![ADC2](https://user-images.githubusercontent.com/79062550/168006616-19012946-00c0-4be0-9d1e-1350118f9e14.PNG)
# ConditionS1,S2 Subsystems:<br>
![ConditionS1](https://user-images.githubusercontent.com/79062550/168007069-d7febe80-b501-42f1-a813-718307e99578.PNG)
# Coh_check Subsystem:<br>
![coh_check](https://user-images.githubusercontent.com/79062550/168007409-fb1139c3-38bf-47c1-9425-0af96f6ce531.PNG)
# State_machine chart:<br>
![state_machine](https://user-images.githubusercontent.com/79062550/168007723-7a5b9d89-f0a3-40c8-8850-569b9fbd7828.PNG)

