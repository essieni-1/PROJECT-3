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
Wecome message                | Driver sits in their seat                        |  Screen shows "Welcome to enhanced alarm system model 218-W26" 
Ready-to-start indication    | Occupy both seats and buckle both belts  |    Green LED lit up once all 4 conditions were met
Driver seatbelt detection     | Simulated belt fastened and unfastened states via button            |           Pass
Passenger seatbelt detection  | Simulated belt fastened and unfastened states via button            |           Pass
Ready-to-start indication     | Checked green LED when all safety conditions were met     |           Pass
Ignition inhibited when unsafe| Pressed ignition button with missing safety conditions    |           Pass
Error message when unsafe     | Read terminal after pressing any combination of buttons plus ignition | Pass
Engine start when safe        | Pressed ignition button with all conditions met           |           Pass
Engine-on indication          | Checked red and green LEDs when ignition button pressed   | Pass
Engine stop                   | Pressed ignition button while engine was running          |           Pass




Ready-to-start indication	
Occupy both seats and buckle both belts 

Green LED turns on 

Green LED lit up once all 4 conditions were met
Ignition inhibited when unsafe	
Press start button while a belt is unbuckled 

Alarm buzzer sounds 

Buzzer sounded as intended
Error messages when unsafe	
Press start button while a belt is unbuckled 

Screen shows "Ignition inhibited" and reasons 

Display correctly listed specific missing safety steps
Engine start when safe	
Press start button with green LED on 

Green LED turns off; Blue LED turns on 

Lights switched correctly upon successful start
Engine-on indication	
Press start button with all conditions met 

Screen displays "Engine started" 

"Engine started" appeared on the display
Engine stop	Press start button while engine is running	Blue LED turns off and system resets	System returned to standby mode and turned off lights
