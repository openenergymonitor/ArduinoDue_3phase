ArduinoDue_3phase
=================

Arduino Due (Arm Cortex M3, 12-bit ADC) 3-Phase Example Library

Arduino Energy Monitoring Library - compatible with Arduino 1.0 
part of openenergymonitor.org project
*****************************************************************

Based on emonLib: https://github.com/openenergymonitor/EmonLib
Modifed for Arduino Due and 3 Phase by icboredman (boredman@boredomprojects.net) - Jan 2014

Download to Arduino IDE 'libraries' folder. Restart of IDE required.


* added 3-phase buffer-delay algorithm, when CT sensors connected to different line phases.
* also includes support for 12-bit ADC resolution on Arduino Due.
* Since it makes sense to keep main EmonLib library single phase, these files were renamed to "EmonLib_3PH.cpp" and "EmonLib_3PH.h"

Includes example sketch "ArduinoDue_3phase.ino" showing how to use Due as an EmonTx:

* There are 10 CT inputs connected to various household lines (after circuit breakers) and 1 AC-AC voltage adapter connected to one of these lines, used to measure voltage.
* 10 lines are connected to different phases, therefore, an extra parameter was added to functions voltage() and voltageTX() indicating a particular phase number.
* The AC-AC line voltage adapter must be connected to phase 1.

See blog post on using Arduino Due as energy monitor: http://boredomprojects.net/index.php/projects/home-energy-monitor
