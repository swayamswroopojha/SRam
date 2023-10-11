# Design and Development of 16-byte SRAM Circuit using 180nm Teachnology
Static Random Access Memory (Static RAM or SRAM) is a type of RAM that holds data in a static form.

SRAM stores a bit of data by using two cross-coupled inverters.

it doesn't required refreshing like DRAM.

it is used in cache memory.


Overall View 
![overall view_page-0001](https://github.com/swayamswroopojha/SRam/assets/130309091/ff7abd9f-c829-4a87-a6e2-251a11e0cbce)


![overall view](https://github.com/swayamswroopojha/SRam/assets/130309091/b9ccd5e9-0d44-4ce3-bab4-d19fe9b89321)







# 6T-SRAM:


Here two cross-coupled inverter connected with two access transistor.

The two access transistor we take nmos.so that overall size should be less.

The two access transistor is connected to precharge circuit. 

when we read the data then the access transistor is ON.so that one node of precharge circuit connected to ground.

And another node is connected to vdd.by which we read the data.


![6tt_page-0001](https://github.com/swayamswroopojha/SRam/assets/130309091/751cf073-dd2c-4d1e-bf3f-bd84638c1825)



![6t sram](https://github.com/swayamswroopojha/SRam/assets/130309091/ac92d55f-e6a1-4757-b0ab-fa48dc483ba4)


# PRECHARGE:


Here we take two pmos.so that we charge the two node BL ,BLB  upto vdd=1.8v.

when ever their is read or write operation before that we must be ON the pc signal.

 To charge the node of access transistor quick.we take the width of the transistor high.

 
![pre_page-0001](https://github.com/swayamswroopojha/SRam/assets/130309091/b6635918-5b73-4151-96de-a77b5e8c4632)



![PRECHARGE](https://github.com/swayamswroopojha/SRam/assets/130309091/1fbfcb33-9d2e-45a0-8dc7-313519576117)


# SENSE AMP:


when their is 10% less voltage in BL OR BLB.the sense amp  can predict the data.
by which we efficiently manage our speed of operation.

CURRENT MIRROR AND DIFFERENTIAL AMP:

TO make the current mirror the  two transistor to be in saturation region.

so that we short-circuit the drain-gate terminal. And size the transistor according to  gm/id = 7.5-9.

And set the output of the differential amp to  the middle value of vdd. according to that we make the sizing of differential amp.

when ever their is any change in BL,BLB  then vgs of nmos is different .so that the current flow of two nmos will be different .

according to that we findout weather 1 is stored or 0 is stored.

Let assume BL is less than vdd .BLB is equal to vdd. so that the vgs value of nmos connected to the BL is less.

so that current is less.to make the kcl satisfy the  BLB is more .so the currrent is flowing from the inverter side to the nmos.

we designed the first inverter in such a way that when ever their is any small change in the middle value .then the output is largely vary.

after that we connected to another inverter to take the output. 



![SENSE AMP](https://github.com/swayamswroopojha/SRam/assets/130309091/34bce98d-a572-44de-b37b-809e3d95040f)


![SEN1_page-0001](https://github.com/swayamswroopojha/SRam/assets/130309091/1cb3a61c-fcee-4783-a059-04d3a9177f3e)


 # ROW DECODER:
 
when the control signal is active then the decoder selects any of row accoding to the address bit.


![decoder](https://github.com/swayamswroopojha/SRam/assets/130309091/cff1b779-d423-4bdd-8dff-9f5f0a2d1e0f) 



# OUTPUT WRITE-READ:

Here we assigned two different resistor with different data.then we read the data from the first resistor.

 first we make the pc off so that BL AND BLB charge upto 1.8v.
 
 Then  we make the control signal on.according to the address any of the row will be selected in this period of time.
 
 And make the R=0 to write the data to the resistor.

 when we read the data from the resistor then make the control signal on and make R to 1.
 


![OUTPUT WRITE -READ](https://github.com/swayamswroopojha/SRam/assets/130309091/a7b3a7ba-799e-484f-9ca4-3b1c9bd7f5d1)

 AT WS TEMP=85:
 
 AT worst speed and high temp the mobility of electron is less .
 
 so that the delay is more.
 
![MAXIMUM DELAY](https://github.com/swayamswroopojha/SRam/assets/130309091/153f7c65-d4ea-4f20-970f-a3ba419bb1c0)

WP TEMP=-40

AT worst power and low temp the mobility is more 

so that the delay is less.

![WP -40](https://github.com/swayamswroopojha/SRam/assets/130309091/c7c970d9-2401-492a-a800-4557ba00a41e)


 TM TEMP=27

 
![TM TEMP=27](https://github.com/swayamswroopojha/SRam/assets/130309091/a39f9881-ed2a-4328-94e2-2b7aceccec51)

