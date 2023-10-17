# Design and Development of 16-byte SRAM Circuit using 180nm Technology
Static Random Access Memory (Static RAM or SRAM) is a type of RAM that holds data in a static form.SRAM stores a bit of data by using two cross-coupled inverters.
here we have designed 16-byte memory.at a time we read or write 8-bit of data.when we have read the data first we turn in the access transistor.
so their will be a potential difference between BL and BLB.According to that we read the data weather it is 1 or 0.To fast this sram we used 
sense amplifier by which we predict the data much faster manner.


Overall View 
![overall view_page-0001 (2)](https://github.com/swayamswroopojha/SRam/assets/130309091/30eb2d0f-3836-4ff3-b53d-7e338af2f9a3)


![overall view](https://github.com/swayamswroopojha/SRam/assets/130309091/b9ccd5e9-0d44-4ce3-bab4-d19fe9b89321)







# 6T-SRAM:


->Here two cross-coupled inverter connected with two access transistor.

->The two access transistor we take nmos.so that overall size should be less.

->The two access transistor is connected to precharge circuit. 

->when we read the data then the access transistor is ON.so that one node of precharge circuit connected to ground.

->And another node is connected to vdd.by which we read the data.

![6tt_page-0001](https://github.com/swayamswroopojha/SRam/assets/130309091/785b6f54-c2e8-413c-be23-ae37ce733d5e)


![6t sram](https://github.com/swayamswroopojha/SRam/assets/130309091/ac92d55f-e6a1-4757-b0ab-fa48dc483ba4)

# write

->When precharge is on then BL,BLB goes to 1.8v.

->Then we turn on the access transistor to write the data forcefully into the  sram .so we required proper sizing of transistor.

![273767982-f6b08e97-d7b7-4e97-850e-75970814fb40](https://github.com/swayamswroopojha/SRam/assets/130309091/3d315db1-f48b-462b-8147-8c1af02e0c21)

Here transistor m5 in saturation m3 is in linear.

![download (2)](https://github.com/swayamswroopojha/SRam/assets/130309091/b5b5f8bd-6787-4770-946d-f42fc999673c)
![download](https://github.com/swayamswroopojha/SRam/assets/130309091/8f9dd398-7ca0-4b07-b339-fe0db10d41da)
![download (1)](https://github.com/swayamswroopojha/SRam/assets/130309091/02cf01d6-b85c-47c1-9943-47a8a01b622f)


# read 

 -> When precharge is on then BL,BLB goes to 1.8v.
 
 -> when we turn on the access transistor then according to the data store in sram one node is goes down and another node is in 1.8v.
 
 -> According to that we read the data from sram.

![273768085-1874556d-4508-41e1-ae91-1c91b54084a2](https://github.com/swayamswroopojha/SRam/assets/130309091/b16a5a9c-391e-471c-878b-3dd77b246bfb)

Here m3 is in saturaion,m1 is in linear.

![download (5)](https://github.com/swayamswroopojha/SRam/assets/130309091/4d61ab50-0af1-4406-88d1-f1bb76dfc757)
![download (4)](https://github.com/swayamswroopojha/SRam/assets/130309091/3d14a859-1acf-4197-b5fb-d5d0d69cffa0)
![download (3)](https://github.com/swayamswroopojha/SRam/assets/130309091/7ed09c3e-24ef-429a-b72b-44aa5224ae3d)


# PRECHARGE:

-> Here we take two pmos.so that we charge the two node BL ,BLB  upto vdd=1.8v.

-> when ever their is read or write operation before that we must be ON the pc signal.

-> To charge the node of access transistor quick.we take the width of the transistor high.



![pre_page-0001 (2)](https://github.com/swayamswroopojha/SRam/assets/130309091/ad5ed771-5416-40c3-a5af-c55b77038dcf)



![Screenshot from 2023-10-12 11-13-10](https://github.com/swayamswroopojha/SRam/assets/130309091/4eecb39b-2d0c-448c-b092-ea57b3e628a1)

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



![SEN1_page-0001 (2)](https://github.com/swayamswroopojha/SRam/assets/130309091/28409acc-6ba1-473d-8923-602d774f9016)


![SENSE AMP](https://github.com/swayamswroopojha/SRam/assets/130309091/34bce98d-a572-44de-b37b-809e3d95040f)



 # ROW DECODER:


-> Here we have design 4:16 decoder using standard cell to select any of the row.


-> Here we have used control signal.


-> when the control signal is active then the decoder selects any of row accoding to the address bit.


-> like example if we make the address 4-bit to 0,then first row is activated or if we make the address 4-bit to 1 then 15th row will be selected.  



![decoder](https://github.com/swayamswroopojha/SRam/assets/130309091/cff1b779-d423-4bdd-8dff-9f5f0a2d1e0f) 



# OUTPUT WRITE-READ:

 -> Here we assigned two different resistor with different data.then we read the data from the first resistor.

 -> first we make the pc off so that BL AND BLB charge upto 1.8v.
 
 -> Then  we make the control signal on.according to the address any of the row will be selected in this period of time.
 
 -> And make the R=0 to write the data to the resistor.

 -> when we read the data from the resistor then make the control signal on and make R to 1.
 

 <img width="644" alt="Screenshot 2023-10-17 13 52 48" src="https://github.com/swayamswroopojha/SRam/assets/130309091/b5cd2451-6e56-4ebd-905e-890b76ee26b3">

 


![OUTPUT WRITE -READ](https://github.com/swayamswroopojha/SRam/assets/130309091/a7b3a7ba-799e-484f-9ca4-3b1c9bd7f5d1)

 AT WS TEMP=85:
 
 AT worst speed and high temp the mobility of electron is less .
 
 so that the delay is more.
 
![MAXIMUM DELAY](https://github.com/swayamswroopojha/SRam/assets/130309091/153f7c65-d4ea-4f20-970f-a3ba419bb1c0)


 TM TEMP=27:

 
![TM TEMP=27](https://github.com/swayamswroopojha/SRam/assets/130309091/a39f9881-ed2a-4328-94e2-2b7aceccec51)


WP TEMP=-40:

AT worst power and low temp the mobility is more 

so that the delay is less.

![WP -40](https://github.com/swayamswroopojha/SRam/assets/130309091/c7c970d9-2401-492a-a800-4557ba00a41e)


