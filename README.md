# Minimal-EPS-Circuit
Icarus Project Phase 2

I used CIRCUITJS which is an open source browser based circuit simulation tool as the tool to make this small circuit.

Our objective is to demonstrate a Charge and discharge cycle of the battery during an orbit of the satellite(60 mins sunlight 30 mins darkness). 
We first start by identifying what all components would be needed to make this circuit. for example- a Solar Source, a 7.4V voltage source, 3 different kinds of loads.
Next we calculate the parameters of these loads and of the Solar Source.
Since a simple voltage source with pwl function capability wasn't present I had to use a VCCS with pwl function to model the Solar power Source(60 minutes ON and 30 minutes OFF) It is  providing approx 6W of power. I used a 0.1 ohm resistance as EPL loss. 
I also had to add a diode to prevent any current from falling back into the VCCS during the eclipse phase. I used a 7.4V voltage source as our battery with a small internal resistance of 0.1 ohms.
We then add our loads. The Sun only payload(27.4 ohms)  which will pull a power of approx 2W.
The OBC load of 55 ohms pulling a power of approx 1W.
And The TT&C load(13.7 ohms) which must be open for short bursts and pulling a power of approx 4W. Since A timed switch functionality wasn't present I had to use A VCVS connected to a NMOS gate which in turn is connected to the TT&C load. The VCVS has a PWL function which will simulate the short burst every 33 mins per orbit  during which the gate will be open. else it will be closed.
The circuit was complete and I then ran the simulation over a few cycles.



HOW TO USE---->
             Download the file and import it into Circuit JS. Choose a time step of 1sec or 0.5sec to simulate the waveforms easier.
             Choose a suitable current and simulation speed. 
             During the Start The Solar Source will be providing the power and charging the battery. You can see the battery charging visually as well as if you check the current waveform                of the 7.4 V battery(a -ve current will be observed) . A short spike will be observed in the current waveform (approx 33 mins after starting and then over and over again for                 each 90 minute orbit), this is due to the TT&C load being turned on. This lasts for approx 5 mins(which is the operating time of the TT&C load).
             After 60 mins the Solar Source stops and the battery starts providing 
             the power for the loads. You can see this both visually and in the  waveform as well ( the curent waveform is now +ve).
             You can also observe the MOSFET gate being turned on after 33 mins per 90 minute orbit which simulates the short timed burst of the TT&C load.


Tools Used ---->
             CHATGPT,GEMINI 2.5 PRO, COPILOT, CircuitJS,YOUTUBE,DEEPSEEK.

LINKS------->        https://www.falstad.com/circuit/doc/
                     https://youtu.be/_pQoccbOK1c























             
