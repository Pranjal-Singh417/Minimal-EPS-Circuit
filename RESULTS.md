
VCCS(with PWL function) = Solar Source: It Represents the satellite's solar panel array and the Maximum Power Point Tracking (MPPT) system that provides power and charges battery  when satellite is NOT in Eclipse.

Series Resistance of 100 m ohm Immediately After the VCCS to simulate the EPS Loss.

Diode: Prevents the backward flow of current from the 7.4V source to the VCCS. 

Ideal 7.4V Source + Series Resistor = Battery Model : Represents the two-cell Li-ion cells  including a small internal resistance of 0.1 ohms to show  voltage droop under load.

On-Board Computer (OBC) Load [55 ohms]: Represents the satellite’s central flight computer managing command/telemetry and payload control.

Timed Switched Resistors (TT&C / Payload)[13.7 ohms]: Uses approximately 4 W of power to represent high-power subsystems that are switched on and off, such as the radio transmitter or a science instrument.

A VCVS source Connected to a MOSFET(n channel) = Simulates a timed switch which allows the current to pass through the TT&C load only for short bursts of time.

Payload sun‑only[27.4 ohms] = This is a payload which only turns on When the Sun is OUT.



The simulation shows  the charging and the discharging cycle of the satellite's power system in  90-minute orbit. 

The first 60 minutes the satellite is in a Sunrise phase so the VCCS which is imitating the SOlar source,

provides a constant current that powers all active loads while the surplus energy charges the battery, shown  by a negative battery current and a slightly increased  main bus voltage. 

We can observe a small but  noticeable spike in the battery current as power is temporarily diverted to power the VCVS 

which will in turn power the MOSFET(This is imitating a timed switch for our TT&C load).After 60 minutes we have a 30 minute eclipse phase where  the solar 

source deactivates and the battery begins to discharge to power the OBC and the TT&C load therefore we can see a positive battery current

and a small decrease in the main bus voltage as the Solar Source has stopped providing power. 







