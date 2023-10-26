# Si5351-with-FM
Modified library for FM modulation. It is verified in the Arduino IDE.
Forked from grate etherkit/Si5351Arduino library. Modified library contains aditional functions which allow  fast writings to specific Si5351 registers, so that new output frequency is achieved in 150us.
By this it is necessary to setClock for the wire communication to 800000Hz.
Deviation of frequency is achieved by fast updating a CORRECTION provided in original library. This can be done in MCU interrupt or frequently in main loop. With an interrupt interval of 200us therefore changes are provided with speed of 5kHz. FM for an Audio bandwith of 2.5kHz can be generated. Such bandwith is sufficent for communication devices such as Radio HAM transmitters. An example of using this for making a Remote controlled VFO acting as a low power transmitter with FM and AM for in lab and close to house surroinding experiments is going to be given in my repository.
When using this for some increased radio frequency power you have to respect Communication and EMC regulatives for your country and internationally!
