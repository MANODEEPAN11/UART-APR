## AIM:

To implement and design synthesis and simulation for uart using cadence - genus and innovus.

## TOOLS REQUIRED:

Functional Simulation: Incisive Simulator (ncvlog, ncelab, ncsim) Synthesis: Genus Floorplanning: Innovus

## PROCEDURE:

Step 1: Synthesis requires the following files as follows: ◦ Liberty Files (.lib) ◦ VerilogFiles (.v )

### Add Verilog  (.v ) file

### Add Testbench file

### Add run.tcl file

SDC (Synopsis Design Constraint) File (.sdc)

In your terminal type “gedit input_constraints.sdc” to create an SDC File if you do not have one.

The SDC File must contain the following commands; 

### Add SDC file

i→ Creates a Clock named “clk” with Time Period 2ns and On Time from t=0 to t=1. 

ii, iii → Sets Clock Rise and Fall time to 100ps. 

iv → Sets Clock Uncertainty to 10ps. 

v, vi → Sets the maximum limit for I/O port delay to 1ps.

•	The Liberty files are present in the library path,

•	The Available technology nodes are 180nm ,90nm and 45nm.

•	In the terminal, initialise the tools with the following commands if a new terminal is being used. ◦ csh ◦ source /cadence/install/cshrc

•	The tool used for Synthesis is “Genus”. Hence, type “genus -gui” to open the tool.

•	Genus Script file with .tcl file Extension commands are executed one by one to synthesize the netlist. Step 2 : Creating an SDC File Step 3 : Performing Synthesis

### Fig 1: RTL Simulation:
<img width="1920" height="1020" alt="Screenshot 2026-09-05 144132" src="https://github.com/user-attachments/assets/1a637b82-ba68-42ee-97ff-bd1425876d33" />

### Fig 2: Synthesis RTL Schematic:
<img width="1920" height="1020" alt="image (6)" src="https://github.com/user-attachments/assets/cab21b22-7f15-45f0-8b64-5ece6bcc107c" />


### Fig 3: Area Report:
<img width="1906" height="1042" alt="image" src="https://github.com/user-attachments/assets/a55c8461-9821-4246-b0ed-67f501f0b0d2" />

### Fig 4: Power Report:
<img width="1905" height="1037" alt="image" src="https://github.com/user-attachments/assets/2ad5fb9a-6140-4307-8528-b03a2756f24e" />


### Fig 5: Timing Report:
<img width="1906" height="1042" alt="image" src="https://github.com/user-attachments/assets/30aabc0d-f00b-477b-91f2-ad33fb39ea03" />

### Fig 6: UART APR:
<img width="1920" height="1020" alt="image (7)" src="https://github.com/user-attachments/assets/f2acf8c6-5f5f-492a-a8f6-8680d6bd74d8" />

<img width="1920" height="1020" alt="image (8)" src="https://github.com/user-attachments/assets/a7a72cb5-d3c8-49d3-95c4-3fa440b7566b" />

<img width="1920" height="1020" alt="image (9)" src="https://github.com/user-attachments/assets/317fa9a8-672a-4362-8b84-bc6847ee0b68" />

<img width="1920" height="1020" alt="image (10)" src="https://github.com/user-attachments/assets/803c1bfd-7f94-4e10-88db-cbe2468dc530" />

<img width="1920" height="1020" alt="image (11)" src="https://github.com/user-attachments/assets/8d3b36dc-d465-4fca-a42e-aee2e5c76ba9" />

## RESULT:

The functionality of the uart was successfully verified using a testbench and simulated with the nclaunch tool and genus and for innovus creating the physical design.
