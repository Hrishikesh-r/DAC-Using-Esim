# DAC-Using-Esim
DAC is a circuit that takes digital signal as input and covert it to analog signal in the form of current or voltage.
In this project we have used  Potentiometric DAC based on voltage divider principle.
It is made up of switches and resistor as shown in the figure
![1_DACArchitecture](https://user-images.githubusercontent.com/91750776/135659175-1317291c-0af1-440e-826d-aad2c43f08e1.png)

The switches are Implemented using CMOS transistors. A schematic of which is shown below using E Sim
![Capture1](https://user-images.githubusercontent.com/91750776/135659939-4b82038f-3465-443b-be6f-34e6f7ff9a68.JPG)
The switch design is done with the help of eeschema editor. The transistor are placed and interconnected as per design with the help of tools on the right side. Once the circuit is ready an eletrical rule check is performed in order to check for any missconnection or unconnection.
Once the eletrical rule check is done successfully, the netlist is generated in default format for  pre layout simulation using ngspice.
the simulation is done with the sky130_fd_pr library and the obatined result is shown below
![f1](https://user-images.githubusercontent.com/91750776/135660782-a39e5805-2bfa-4226-818c-18df04ef3383.JPG)

After verifying the functional working of the switches, A symbol is created for the switches with required I/O ports to use the switch as a subcircuit to a new circuit.

![s1](https://user-images.githubusercontent.com/91750776/135663596-8dd718df-a79b-46f4-a0cd-a8145885d76d.JPG)

A two bit DAC is implemented using 3 switches, 4 resistors as shown below.
![glj,hbkjbui;un](https://user-images.githubusercontent.com/91750776/135662048-28de521d-e4d6-4590-a438-6cf4884cd622.JPG)

Again the eletrical rule check is done, netlist is generated and pre-layout simulation is done with ngspice. Obatined result is shown below
![d1](https://user-images.githubusercontent.com/91750776/135663234-8db7bc27-fced-4d3d-818e-bcb0d5e9ff60.JPG)

# FUTURE WORK
The hierarchy of designing DAC can be extended to 10 bit from 2bit. So In general N-bit DAC can be Implemeted using (N-1)bit DAC and Switch as shown below:

![image](https://user-images.githubusercontent.com/91750776/135664363-e53ca484-03ea-44d8-a71a-fe4be8778b91.png)
