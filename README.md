## Final-Presentation Project: PID System for Simulated Vehicles.
---
### Blueprint:
1. **PID System**: Automatically stabilize and balance contraptions, Structured by `Error = Setpoint - Measurement or Change = DesiredPosition - CurrentPosition.`
> Formula: `Total Correction = (Proportional_Intensity * Error) + (Integral_Intensity * Sum {Error * Time}) + (Derivative_Intensity * ((CurrentError - LastError) / Time))`
>> Description: Amount of Error to fix + Error amount times how long it has happened (helps correct persistent error overtime) + All Changes in Error divided by the time they occur (This Smoothens the change between the corrections to make it more gradualy transition between states/positions.) (Helps remove oscillation since the program doesn't overshoot the setpoint.)
3. Regulate Pitch, Yaw, Roll, Altitude/Height, each require their own PID system to manage.
4. Create the translations between simulated engines and the PID systems (i.e. digital value to rotational speed). Along with additional logic for vehicles with multiple propellors.
5. Helicopter PID System: Changes propellor speed and directional tilt (for traditional versions). Airplane PID System: Changes throttle, aileron and flap angles.
6. Walker PID System: PID controls the stability of the torso, the legs follow a gait cycle which is modified by the PID system
> // Might need to reconsider because a lot of these systems are already built into the simulation so coding them would be unnecessary, at least for the walker since its joints already include a pid system.
> //Gait Cycle by itself would be its own project.

1. **Arm Functions**: Random pre coded movements that allow a mechanical arm to complete some tasks, such as throwing, picking and despositing, etc.
