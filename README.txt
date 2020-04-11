#systems consists of three ECUs.
-The ECUs are connected by a CAN bus.
-Test PC is connected to the same CAN Bus.



#The Seat Belt Manager shows the driver of a car by an LED if a seat
is occupied (somebody is sitting on the seat) and the seat belt is not plugged.
Additionally if the car goes more than 15 km/h a sound informs the driver
that the seat belt should be plugged.



#ECU1:
-Sends the sensor values to the bus.



#ECU2:
-Contain switches on/off LED.
-Decides if sound should be played.  



#ECU3:
-Contain switches on/off sound.
-Decides if functions should be activated.




#Signal Description:   
-The possible values for each signal is defined in square brackets.
-Each signal is represented on the CAN bus by a CAN message:
1-seatbelt (ID 3): [0,1] – 0 means seat belt not plugged, 1 means seat belt plugged.
2-seatoccupied (ID 2): [0,1] – 0 means seat is not occupied, 1 means seat is occupied.
3-currentspeed (ID 1): has the value of the current speed of the car in km/h. 
4-playsound (ID 4): [0,1] – 0 means sound should not be played, 1 means sound should 
be played.
5-lightassist (ID 5): [0,1] – 0 means deactivate function, 1 means activate function.
6-tvfunction (ID 6): [0,1] – 0 means deactivate function, 1 means activate function.
7-parkpilot (ID 7): [0,1] – 0 means deactivate function, 1 means activate function.
8-doorlocking (ID 8): [0,1] – 0 means do not lock doors, 1 means lock doors 
