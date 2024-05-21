# DEMULTIPLEXER1TO4
# AIM
To simulate and synthesis demultiplexer 1 TO 4 using Vivado software.
# APPARATUS REQUIRE
Vivado 2023.1 software.
# PROCEDURE
STEP:1 Start the Xilinx navigator, Select and Name the New project.

STEP:2 Select the device family, device, package and speed.

STEP:3 Select new source in the New Project and select Verilog Module as the Source type.

STEP:4 Type the File Name and Click Next and then finish button. Type the code and save it.

STEP:5 Select the Behavioral Simulation in the Source Window and click the check syntax.

STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.

STEP:7 Select the Implementation in the Sources Window and select the required file in the Processes Window.

STEP:8 Select Check Syntax from the Synthesize XST Process. Double Click in the Floorplan Area/IO/Logic-Post Synthesis process in the User Constraints process group. UCF(User constraint File) is obtained.
STEP:9 In the Design Object List Window, enter the pin location for each pin in the Loc column Select save from the File menu.

STEP:10 Double click on the Implement Design and double click on the Generate Programming File to create a bitstream of the design.(.v) file is converted into .bit file here.

STEP:11 Load the Bit file into the SPARTAN 6 FPGA

STEP:12 On the board, by giving required input, the LEDs starts to glow light, indicating the output.

# Truth Table
![image](https://github.com/kanipakajeevana/DEMULTIPLEXER1TO4/assets/170450203/fa0423ce-026d-45b2-a3ee-d43fb34d6c77)

# Circuit Diagram
![image](https://github.com/kanipakajeevana/DEMULTIPLEXER1TO4/assets/170450203/42690cd2-d073-46ec-99a6-cb067a8c901d)
![image](https://github.com/kanipakajeevana/DEMULTIPLEXER1TO4/assets/170450203/5520c986-dd8f-4330-aac9-533f91ea05e2)
![image](https://github.com/kanipakajeevana/DEMULTIPLEXER1TO4/assets/170450203/d995b0f9-653f-431e-a866-64f6cc9e3518)
![image](https://github.com/kanipakajeevana/DEMULTIPLEXER1TO4/assets/170450203/b15f814f-a6f9-4bef-ba62-4a1c893470d9)
![image](https://github.com/kanipakajeevana/DEMULTIPLEXER1TO4/assets/170450203/cd5414ee-6fbd-4851-8985-5957af395f7b)
# VERILOG PROGRAM
module demux(y0,y1,y2,y3,s1,s0,I);
 input I,s0,s1;
 output y0,y1,y2,y3;
     assign s1n = ~ s1;
     assign s0n = ~ s0;
     assign y0 = I & s0n & s1n;
     assign y1 = I & s0 & s1n;
     assign y2 = I & s0n & s1;
     assign y3 = I & s0 & s1;
 endmodule
 # OUTPUT
 ![image](https://github.com/kanipakajeevana/DEMULTIPLEXER1TO4/assets/170450203/5477d162-0e69-4ee6-9472-00337f205f30)
 # RESULT
 Thus the simulate and synthesis of demultiplexer 1 TO 4 is verified successfully by using Vivado software.





