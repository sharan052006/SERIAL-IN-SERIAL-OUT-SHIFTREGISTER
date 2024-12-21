# SERIAL-IN-SERIAL-OUT-SHIFTREGISTER

**AIM:**

To implement  SISO Shift Register using verilog and validating their functionality using their functional tables

**SOFTWARE REQUIRED:**

Quartus prime

**THEORY**

**SISO shift Register**

A Serial-In Serial-Out shift register is a sequential logic circuit that allows data to be shifted in and out one bit at a time in a serial manner. It consists of a cascade of flip-flops connected in series, forming a chain. The input data is applied to the first flip-flop in the chain, and as the clock pulses, the data propagates through the flip-flops, ultimately appearing at the output.

The logic circuit provided below demonstrates a serial-in serial-out (SISO) shift register. It comprises four D flip-flops that are interconnected in a sequential manner. These flip-flops operate synchronously with one another, as they all receive the same clock signal.

![image](https://github.com/naavaneetha/SERIAL-IN-SERIAL-OUT-SHIFTREGISTER/assets/154305477/e81c4072-37f9-46c6-8145-566764b74c3a)

Figure 01 4 Bit SISO Register

The synchronous nature of the flip-flops ensures that the shifting of data occurs in a coordinated manner. When the clock signal rises, the input data is sampled and stored in the first flip-flop. On subsequent clock pulses, the stored data propagates through the flip-flops, moving from one flip-flop to the next.
Each D flip-flop in the circuit has a Data (D) input, a Clock (CLK) input, and an output (Q). The D input represents the data to be loaded into the flip-flop, while the CLK input is connected to the common clock signal. The output (Q) of each flip-flop is connected to the D input of the next flip-flop, forming a cascade.

**Procedure**

/* write all the steps invloved */

**PROGRAM**

/* Program for flipflops and verify its truth table in quartus using Verilog programming.

Developed by:sharan I 
RegisterNumber: 24010956
```
module ex10(a, b, clk, rst, acc); 
input [7:0] a; 
input [7:0] b; 
input clk; 
input rst; 
output [15:0] acc; 
reg [15:0] acc; 
reg [15:0] pd; 
reg [15:0] adder; 
always @ (posedge(clk) or posedge(rst)) 
begin 
if (rst==1'b1) 
  begin 
  adder=8'b00000000; 
  end 
  else 
  begin 
  pd=a*b; 
  adder=adder+pd; 
  end 
  acc=adder; 
  end 
  endmodule
```


*/

**RTL LOGIC FOR SISO Shift Register**
![ex-10-d](https://github.com/user-attachments/assets/7e3e00c1-8ae7-499e-9583-642f350b56a9)

**TIMING DIGRAMS FOR SISO Shift Register**
![ex-10-w](https://github.com/user-attachments/assets/e1c108c9-847d-4787-9e5b-e62bbb68447e)

**RESULTS**
SISO Shift Register is implimented and their functionality is verified
