## PROJECT-3: Enhanced Vehicle Alarm & Wiper Control System
# Team Members: Iyene Essien & Heidi Garcia

# System Behavior
This project is an upgrade for Driver's Education vehicles to ensure student drivers are following safety rules. The system basically acts like a smart key. It will not let you start the car unless the driver ans passenger are both sitting in their seats and have their seatbelts buckled.
Once the car has safely started, the system enables the windshield wipers. These wipers work just like a real car with four settings: Off, Low speed, High speed and Intermittent (where the wipers pause for 1, 3, or 5 seconds before wiping again). All of this information—like "Engine Started" or the current wiper speed—is shown on a small screen for the driver to see.

# Design Alternatives
1. Two Tasks in One

Choice: We told the computer to watch the safety sensors and move the wipers.
Reasoning: If the computer only did one thing at a time then it might get stuck moving the wipers and forget to check if someone unbuckled their seatbelt.

2. Smooth Wiper Movement

Choice: Instead of making the wiper move from one side to the other, we programmed it to take many tiny steps.
Reasoning: This copies a real car's wiper motor. We used math to make sure the "Low" setting moves at a relaxed pace (10 rotations per minute) while "High" moves much faster (25 rotations per minute).

3. Clear Warnings

Choice: If the car won't start, the system doesn't just stay quiet. It sounds a buzzer and writes the reason for why the the car won't start (exmaple: "Driver seat not occupied.")
Reasoning: This helps a student driver quickly understand what they did wrong so they can fix it and try again. 


Summary of Testing Results:
---------------------------------------------------------------------------------------------------------------------------

### Subsystem 1: Safety & Ignition Control

| Behavior | Test Process | Result |
| --- | --- | --- |
Driver seat detection         | Press the driver seat button     |           Terminal prints "Welcome to enhanced alarm system model 218-W26"
Passenger seat detection      | Press the passenger seat button |         One condition for ready to start is met 
Driver seatbelt detection     | Press the driver seatbelt button           |             One condition for ready to start is met
Passenger seatbelt detection  | Press the passenger seat button           |           One condition for ready to start is met 
Ready-to-start indication     | Press all four buttons (driver seat, passenger seat, driver seatblet and passenger seatbelt)    |       Green LED lights up
Ignition inhibited when unsafe| Pressed ignition button with missing safety conditions    |        Buzzer sounds 
Error message when unsafe     | Pressed ignition button with missing safety conditions | Screen shows "Ignition inhibited" and reasons
Engine start when safe and its indication        | Pressed ignition button with all conditions met           |         Red LED lights up
Engine stop                   | Press ignition button again when engine is already running         |    Red LED turns off, system resets and terminal prints "Engine stop"
