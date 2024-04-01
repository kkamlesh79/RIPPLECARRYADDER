![image](https://github.com/abiramipitchaimani/RIPPLECARRYADDER/assets/163704307/4c918008-8a83-40b5-8858-18b932753a78)![image](https://github.com/abiramipitchaimani/RIPPLECARRYADDER/assets/163704307/1c55ceba-639e-42e8-9ac1-5045463bfcfd)# RIPPLECARRYADDER

# Aim
   To simulate and synthesis of ripplecarryadder using vivado 2023.2
# Software required REQUIRED
   Vivado 2023.2
# Procedure
STEP:1 Start the vivado software, Select and Name the New project.

STEP:2 Select the device family, device, package and speed.

STEP:3 Select new source in the New Project and select Verilog Module as the Source type.

STEP:4 Type the File Name and module name and Click Next and then finish button.

Type the code and save it.

STEP:5 Select the run simulation and then run Behavioral Simulation in the Source Window and click the check syntax.

STEP:6 Click the simulation to simulate the program and give the inputs and verify the outputs as per the truth table.

STEP:7 compare the output with truth table.
![image](https://github.com/RESMIRNAIR/RIPPLECARRYADDER/assets/154305926/62459000-90cb-4c43-a221-7b8cf1d419b0)
![image](https://github.com/RESMIRNAIR/RIPPLECARRYADDER/assets/154305926/24ea1940-0b55-4f8a-be6a-a7ac5daf2919)
# Full Adder
![image](https://github.com/RESMIRNAIR/RIPPLECARRYADDER/assets/154305926/3208d46f-2fd4-4d6a-987f-63102c173ca0)
# Program
```
Developed by: P.Abirami
Register number: 212222060006
```
```
module fa(a,b,c,sum,carry);
input a,b,c;
output sum,carry;
assign sum = a^b^c;
assign carry=(a&b)|(b&c)|(c&a);
endmodule
module rca(a,b,cin,sum,cout);
input [3:0]a,b;
input cin;
output [3:0]sum;
output cout;
wire c1,c2,c3;
fa fa1(a[0],b[0],cin,sum[0],c1);
fa fa2(a[1],b[1],c1,sum[1],c2);
fa fa3(a[2],b[2],c2,sum[2],c3);
fa fa4(a[3],b[3],c3,sum[3],cout);
endmodule
```
# Output:
![image](https://github.com/abiramipitchaimani/RIPPLECARRYADDER/assets/163704307/9af94ac1-b08b-4e49-bed7-6f350252e28c)

# Result
Thus the simulation and synthesis of Ripplecarryadder using vivado 2023.2 is successfully executed and verified.
