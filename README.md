# SRam
Static Random Access Memory (Static RAM or SRAM) is a type of RAM that holds data in a static form.
SRAM stores a bit of data by using two cross-coupled inverters.
it doesn't required refreshing like DRAM.
it is used in cache memory.
Overall View 
![overall view](https://github.com/swayamswroopojha/SRam/assets/130309091/b9ccd5e9-0d44-4ce3-bab4-d19fe9b89321)


6T-SRam
Here two cross-coupled inverter connected with two access transistor.
The two access transistor we take nmos.so that overall size should be less. 

![6t sram](https://github.com/swayamswroopojha/SRam/assets/130309091/ac92d55f-e6a1-4757-b0ab-fa48dc483ba4)

PRECHARGE
Here we take two pmos.so that we charge the two node upto vdd=1.8v.
![PRECHARGE](https://github.com/swayamswroopojha/SRam/assets/130309091/1fbfcb33-9d2e-45a0-8dc7-313519576117)

SENSE AMP
when their is 10% less voltage in BL OR BLB.the sense amp  can predict the data.
by which we efficiently manage our speed of operation. 
![SENSE AMP](https://github.com/swayamswroopojha/SRam/assets/130309091/34bce98d-a572-44de-b37b-809e3d95040f)

 ROW DECODER
when the control signal is active then the decoder selects any of row accoding to the address bit.
![decoder](https://github.com/swayamswroopojha/SRam/assets/130309091/cff1b779-d423-4bdd-8dff-9f5f0a2d1e0f)

OUTPUT WRITE-READ
Here we aasigned two different resistor with different data.then we read the data from the first resistor.
![OUTPUT WRITE -READ](https://github.com/swayamswroopojha/SRam/assets/130309091/a7b3a7ba-799e-484f-9ca4-3b1c9bd7f5d1)

 AT WS TEMP=85
 AT worst speed and high temp the mobility of electron is less .
 so that the delay is more.
![MAXIMUM DELAY](https://github.com/swayamswroopojha/SRam/assets/130309091/153f7c65-d4ea-4f20-970f-a3ba419bb1c0)

WP TEMP=-40
AT worst power and low temp the mobility is more 
so that the delay is less.

![WP -40](https://github.com/swayamswroopojha/SRam/assets/130309091/c7c970d9-2401-492a-a800-4557ba00a41e)

 TM TEMP=27
![TM TEMP=27](https://github.com/swayamswroopojha/SRam/assets/130309091/a39f9881-ed2a-4328-94e2-2b7aceccec51)
