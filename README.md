# How-TO Guide on Getting VCDS working on your Porsche Cayenne 955

I couldn't find any concrete documentation online around using VCDS (VAGCOM) to reset the service now warning for a 955. I would like to share with you a guide on how to make VCDS work with your car and then reset the service warning. 

# Creating a VCDS OBD2 adapter

First off, your VCDS cable will not work with your car out of the box because the Porsche OBD2 port is wired up differently to VAG cars even though they use the same modules and architecture. 
The best way to do this is to buy an OBD2 extension cable, cut it open and bridge wires belonging to pins 3, 7 and 15 together. All the data from the different controllers in the car run down these wires. 
All other wires (if you had to cut yours completely open like me) can be rejoined as they previously were. I used some heat shrink which has solder in them and used a hot air gun to melt them. (See photos of the finished product). 

![image](https://github.com/RichardODonoghue/porsche_cayenne_955_VCDS/assets/1446236/28d99587-71bf-4abe-8807-a5d3688714d1)

After this, test the cable with a multimeter in continuity mode to insure that the pins on one side are connected to the right pin on the other side. 
Now you can plug in the extension cable and VCDS cable into your car and computer, turn the key to the ignition position (but do not turn the car on). 

# Resetting the Service Reminder
You can then open up VCDS and select controller 17 - instruments
A window will pop up where you can click 10 - adaption 
Another window will pop up, You will need to change the following channels: 
channel 40 - insp. in 1: Change the value to 0
channel 41 - insp. in 1: change the value to 0
channel 43 - oil in 1: change the value to 100
channel 44 - insp. in 1: change the value to 365
On each channel in order to save the change you will first need to click "test" and then "save" 
After this that pesky warning will be gone till your next service is due. 
