## Final-Presentation Project: PID System for a Simulated Drone.
---
### Overveiw:
- What is a Pid System?
- ***PID System***: Tries to correct the difference between the current value and the desired value using a formula. In the case of drones this helps maintain its orientation.
-  Structured by `Error = Setpoint - Measurement or Change = DesiredPosition - CurrentPosition.`
> Formula: `Total Correction = (Proportional_Intensity * Error) + (Integral_Intensity * Sum {Error * Time}) + (Derivative_Intensity * ((CurrentError - LastError) / Time))`
>> Description: Amount of Error to fix + Error amount times how long it has happened (helps correct persistent error overtime) + All Changes in Error divided by the time they occur (This Smoothens the change between the corrections to make it more gradualy transition between states/positions.) (Helps remove oscillation since the program doesn't overshoot the setpoint.)
---
### Implementation
- ***PID Systems***: Each regulated value require their own PID system to manage.
> 1. Pitch
> 2. Roll
> 3. Yaw Note: Drones turn using CW and CCW spinning propellors, 2 for each diagonally, as CWW speeds up CW slows down leading to turning.
> 4. Altitude/Speed
- ***Translation/Communication***: How does the drone communicate its orientation with the program/computer.
> 1. Gimbal Sensor & Propellors Geardrive
> 2. Gimbal Sensor & Propellors Geardrive
> 3. Compass Sensor Add on & External Rotation Source
> 4. Altitude Sensor & Rotational Speed Controller
- ***Caveats***: Special considerations for the project.
> - Redstone has a maximum range of 0-15, as such when trying to communicate numerical values, they have to be translated to be accurately represented in game.
> - Simplified Physics, working both the benefit and determent of the drone.
> - Make a port of the Lua Script code in C++, to help in understanding the code.



