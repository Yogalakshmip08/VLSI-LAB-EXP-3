SIMULATION AND IMPLEMENTATION OF MULTIPLIER
**AIM: **
 To simulate and synthesis multiplier using Xilinx ISE.

**APPARATUS REQUIRED:**
Xilinx 14.7
Spartan6 FPGA
  
**PROCEDURE:**
STEP:1  Start  the Xilinx navigator, Select and Name the New project.
STEP:2  Select the device family, device, package and speed.       
STEP:3  Select new source in the New Project and select Verilog Module as the Source type.                       
STEP:4  Type the File Name and Click Next and then finish button. Type the code and save it.
STEP:5  Select the Behavioral Simulation in the Source Window and click the check syntax.                       
STEP:6  Click the simulation to simulate the program and  give the inputs and verify the outputs as per the truth table.               
STEP:7  Select the Implementation in the Sources Window and select the required file in the Processes Window.
STEP:8  Select Check Syntax from the Synthesize  XST Process. Double Click in the  FloorplanArea/IO/Logic-Post Synthesis process in the User Constraints process group. UCF(User constraint File) is obtained. 
STEP:9  In the Design Object List Window, enter the pin location for each pin in the Loc column Select save from the File menu.
STEP:10 Double click on the Implement Design and double click on the Generate Programming File to create a bitstream of the design.(.v) file is converted into .bit file here.
STEP:11  On the board, by giving required input, the LEDs starts to glow light, indicating the output.

**Logic Diagram**
2 bit Multiplier

![image](https://github.com/navaneethans/VLSI-LAB-EXP-3/assets/6987778/7713750f-65e6-41c0-8082-5005eac4031c)

**4 Bit Multiplier**

![image](https://github.com/navaneethans/VLSI-LAB-EXP-3/assets/6987778/d95215dd-8cf1-4e08-93cc-96adfdd7fbdc)


**Verilog code**
MULTIPLIER 2BIT:
```
module ha(a,b,sum,carry);
input a,b;
output sum,carry;
xor g1(sum,a,b);
and g2(carry,a,b);
endmodule
module bitmul(a,b,p,cout);
input [1:0]a,b;
output [2:0]p;
output cout;
wire w1,w2,w3,w4;
and (p[0],a[0],b[0]);
and (w1,a[0],b[1]);
and (w2,a[1],b[0]);
and (w3,a[1],b[1]);
ha adder1(w1,w2,p[1],w4);
endmodule
```
OUTPUT:
![WhatsApp Image 2024-04-22 at 14 53 50_49367b66](https://github.com/Yogalakshmip08/VLSI-LAB-EXP-3/assets/161303457/b14f08f2-96b1-450a-9b4f-005db24801c1)



**Output Waveform**

<<< Simulation output waveform paste it here >>>>>


**Result**



