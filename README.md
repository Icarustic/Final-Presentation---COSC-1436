## Final-Presentation Project: PID System for a Simulated Drone.
---
### Overveiw:
- What is a Pid System?
- **PID System**: Tries to correct the difference between the current value and the desired value using a formula. In the case of drones this helps maintain its orientation.
-  Structured by `Error = Setpoint - Measurement or Change = DesiredPosition - CurrentPosition.`
> Formula: `Total Correction = (Proportional_Intensity * Error) + (Integral_Intensity * Sum {Error * Time}) + (Derivative_Intensity * ((CurrentError - LastError) / Time))`
>> Description: Amount of Error to fix + Error amount times how long it has happened (helps correct persistent error overtime) + All Changes in Error divided by the time they occur (This Smoothens the change between the corrections to make it more gradualy transition between states/positions.) (Helps remove oscillation since the program doesn't overshoot the setpoint.)


- Regulate Pitch, Yaw, Roll, Altitude/Height, each require their own PID system to manage.
- Create the translations between simulated engines and the PID systems (i.e. digital value to rotational speed). Along with additional logic for vehicles with multiple propellors.
- Helicopter PID System: Changes propellor speed and directional tilt (for traditional versions). Airplane PID System: Changes throttle, aileron and flap angles.

