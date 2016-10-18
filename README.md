# Sanctus
Sanctus Rover

==========Introduction==========
The Sanctus rover is a Arduino-based prototype platform for research and experiments fit within a modular frame. This is a testbed for the Explorator rover, which will operate using the same drive code and similar control code, but with a much larger frame to accommodate more experiment and research packages as well as offering 4 regulated voltage bus' - 3.3v, 5v, 12v, and 24v. 

Please note that this is the prototype based on a 8.4v Traxxas RC Vehicle - this is not the final rover, but rather a testbed for the final rover. 

==========SYSTEMS==========
----------Master----------
This is the main control system that controls navigation, propulsion, onboard user input, the rear LCD screen, status LED’s, and serial communication. 
The master has control over two subsystems, the NAVSEN package which allows it to navigate terrain and avoid obstacles and the SERIAL package that allows it to communicate with the Slave board. 

----------Slave----------
This is the secondary control system that controls sensor packages, communication, onboard memory storage, and any tertiary boards through I2C.
The Slave has control over multiple subsystems and is designed to be highly expandable. The primary subsystems it controls is LRCOM for long range communications, MEMS for memory storage and onboard clock, and EXIO for additional input/output for subsystems (not additional boards).

----------Subsystems----------
NAVSEN - Sensors used for detecting obstacles, direction, orientation, and acceleration. 
SERIAL- Serial bus used for communication between master and slave boards.
LRCOM - Long range communication package
MEMS - Memory and onboard clock for storing and retrieving data and timestamps.
EXIO - External Input/Output for communicating with additional sensors. 
