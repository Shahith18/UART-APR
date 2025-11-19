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
<img width="1920" height="1080" alt="Screenshot (132)" src="https://github.com/user-attachments/assets/28293982-5085-4d8e-9890-2cc437b70f05" />


### Fig 2: Synthesis RTL Schematic:
<img width="1920" height="1080" alt="Screenshot (137)" src="https://github.com/user-attachments/assets/28b9ef19-0fb2-4ebb-b992-cf2edb2d4b46" />

### Fig 3: Area Report:
<img width="1920" height="1080" alt="Screenshot (140)" src="https://github.com/user-attachments/assets/b08a17a4-290d-49a4-a8d3-3011bce86bab" />

### Fig 4: Power Report:
<img width="1920" height="1080" alt="Screenshot (139)" src="https://github.com/user-attachments/assets/bf9dd5fb-86e9-441f-bf86-3d230bc0f75d" />

### Fig 5: Timing Report:
<img width="1920" height="1080" alt="Screenshot (138)" src="https://github.com/user-attachments/assets/07e803d0-ab19-4fa6-b9a1-34489d29dcf1" />


## RESULT:

The functionality of the uart was successfully verified using a testbench and simulated with the nclaunch tool and genus and for innovus creating the physical design.
