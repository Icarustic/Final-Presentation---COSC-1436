## Final-Presentation Project: PID System for Simulated Vehicles.
---
### Blueprint:
1. **PID System**: Automatically stabilize and balance contraptions, Structured by `Error = Setpoint - Measurement or Change = DesiredPosition - CurrentPosition.`
> Formula: Total Correction = (Proportional_Intensity * Error) + (Integral_Intensity * Sum {Error * Time}) + (Derivative_Intensity * ((CurrentError - LastError) / Time))
>> Description: Amount of Error to fix + Error amount times how long it has happened (helps correct persistent error overtime) + All Changes in Error divided by the time they occur (This Smoothens the change between the corrections to make it more gradualy transition between states/positions.) (Helps remove oscillation since the program doesn't overshoot the setpoint.)
3. Regulate Pitch, Yaw, Roll, Altitude/Height, each require their own PID system to manage.
4. 

