I Mainly made use of Gemini 2.5 Pro version and I also used ChatGPT -5 and 5 mini to a lesser extent. 
Some of the prompts I used were- 

"According to the PDF calculate all the load parameters."

"How should I go about implementing the TT&C load  considering its a timed thing. Keep in mind i can only use pwl in control sources."

"Can you show me where i Need to place the VCVS and The MOSFET with the load in my circuit with a VERY SIMPLE IMAGE."

"What should my A,B,V+ and V- be connected to in the vcvs?"

"The current seems to be flowing back into the VCCS. is it fine? how do i stop it from going back."

"for me its showing 7.437 V when charging and 7.37 V when not charging, how big would the dropoff be?"

"Currently for OBC LOAD : I=135 mA, vd=7.4V, R=55 ohm, p=1.016 W... i think this should be fine right??"

"The issue is even if the gate is off. The Current flows straight from the 7.4v bus battery through the resistor and then from the mosfet... WHY"




The AI's have a hard time generating proper circuit diagrams. The AI also seemed to be using some different version of CIRCUITJS which could not properly generate the Netlist so it was not possible to simply copy and paste the code generated. However the AI is able to theoretically describe how the connections need to be made and is also able to draw simple ASCII sketches of the circuit. It was also able to generate the image of the circuit diagram once which was helpful in understanding how to connect the systems. Different models of AI also generate different load values for the same constraints as well. So it is important to double check them. The Main issue faced by me was the AI referring to some other version of Circuit JS which did not include many of the stuff it was suggesting, for example a timed switch or a simple 2 terminal source with pwl function. Different solutions had to be found for different suggestions like using a vcvs operated mosfet which acted  like a timed switch. The AI also could not visually describe the MOSFEt connections needed, However it was able to theoretically explain it pretty well. 
