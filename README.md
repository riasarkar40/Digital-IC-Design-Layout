# Digital-IC-Design-Layout
This repository is intended to capture step by step method to create schematic and layout for Digital ICs.
Special thanks to : Prof. Janakiraman Viraraghavan, TAs : Balaji / 


**Module 0** : **Familirization with Tool for Schematic and Layout**
          Tools to be used : LTSpice XVII and Electric
          Links for installing the tools and integrating schematic and layout - http://cmosedu.com/cmos1/ltspice/ltspice_electric.htm
	  
   **0.1 Steps to create Schematic for inverter circuit** -
   	
    1. Create new library -> Demo2
	2. Create new cell (inverter) within the library.
	3. Go to Components -> Select VDD and GND and place it { these 2 symbols do not need to be named specifically}
	4. Plan is to construct basic inverter circuit.
	5. Components -> NMOS & PMOS
	6. Connect the G, S and D of MOSFET
	7. Add Input and Output pins and gate to Gate and Drain.
	8. Now exporting it -> Ctrl + E (Shortcut)
	9. Export char -> Input
	Export name -> INP
	10. Repeat previous step considering char as Output & OUT.
	11. Now we need to set the spice model. Shift + S (shortcut) or Tools -> Simulation(Spice)->> Set Spice Model
	12. Click of PMOS and Shift + S to open spice model. A line connecting shows component is getting set with spice model.  Note : Click somewhere at the left side of component
	13. Repeat the same process for nmos.
      Consider the exact name given in the model file.
	14. Now we will write the spice code : 
			§ Including the model file in the first line.
			§ 2nd line defining VDD and GND voltages (as these params need not be exported)
			§ 3rd line -> We are giving input as PWL { waveform where we can define time instance -> Time followed by voltage. }
			§ 4th line -> . Tran used to perform transient analysis. { I/Ps which has changing voltage with time. }
			§ Apply the settings.
	15. Write spice deck -> W + S (Shortcut) or Tools -> Simulation (Spice) ->> Write spice deck
      Now we need to add traces ->right click in the plot- >> V(inp) , V(out) , Vdd![image](https://github.com/user-attachments/assets/4ebe9557-ea28-4647-a903-0aca4a36b237)
