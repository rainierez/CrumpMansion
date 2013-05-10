CrumpMansion
============

Personal Home Automation project. Evolving daily...

-HVAC, Montioring/Logging:
  Current:
    -Currently logging to a DB every minute with the status of the HVAC system, this keeps track of the (heat, cool, fan) cycles, their run duration and times.
  Future:
    -Fix the web page front end for charting and data display
  
-HVAC, Fan Circulation:
  Current: 
    -I have a script that turns the fan on, on the hour and another that turns the fan back off 20 minutes later. These are set as cron jobs for now.
  Future: 
    -Run a script ever minute that checks the DB for the last HVAC cycle, be that Heat, Cool, or even a manual (at the thermostat or via some other human controled even) then if after XX time (probably something like 45 minutes) of no HVAC cycles to turn the fan on.
    -This script should also be checking to see if the fan has ben running on it's own for XX amount of time and then shut it off.

-HVAC, Zoning
  Future:
    -Automate registers with servos
    -PWM breakout board
    -Wiring to the registers
    -Temp, Humitidy, and light sensors (1wire?) upstairs
    -Code, control and interface
    
-Security:
  Future:
    -Reading on all door sensors (4x reed switches NC)
    -Code, for alerts (email, text, etc.)
    -Smoke detectors?

-X10:
  Current:
    -Working but no automation of any sort yet, not sure what I want to do.
    
Interface:
  Keypad:
    Current:
      -Code done for general display control over I2C to the MCP23017 chip.
      -Code done for 3x4 matrix keypad polling
    Future:
      -Code for directional, select, arm buttons
      -Menu system design and coding
  Web:
    Current:
      -Nothing :(
    Future:
      -Main page with summary of HVAC system, Security system, and Weather
