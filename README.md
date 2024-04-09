# Digital VLSI-SOC DESIGN
## DAY-1 
### Inception of open-source EDA, OpenLANE and Sky130 PDK
#### Theory-

QFN-48 Package: It's a small package used for computer chips. The "48" indicates it has 48 connection points.

Chip: Also called as an integrated circuit (IC) or microchip, a chip is a small semiconductor device that contains electronic circuits etched onto a tiny piece of silicon.

Pads: These are metal spots on the chip that act as connection points to communicate with other parts of a device.

Core: The core of an integrated circuit typically refers to the central processing unit of the chip.

Die: The die is the individual part of the chip before it's installed into a device.

IPs: These are pre-designed blocks used in chip creation, similar to pre-made Lego pieces that help speed up the chip design process.

RISC-V: It is a free and open instruction set architecture (ISA) enabling a new era of processor innovation through open standard collaboration.

Application software to Hardware:
      ->Application software directly interacts with system software, including the operating system (OS), compilers, and assemblers, to access hardware resources 
      efficiently.
      
      ->The OS manages hardware resources and provides essential services, while compilers and assemblers translate high-level code into machine code i.e., it converts to binary codes and feeds to the hardware

![Uploading Screenshot (24).png…]()

we are using an open source platform for ASIC Design which was collabrated by google and skywater technology.

![Uploading Screenshot (25).png…]()

RTL2GDS Flow:

- Synthesis: Converting high-level design specifications into a gate-level representation for hardware implementation.
  
- Floorplanning: Strategically arranging functional blocks on a chip's surface to optimize performance, power, and area usage.
  
- Placement: Assigning physical positions to logic cells or functional blocks within the chip's area to optimize interconnections.
  
- Clock Tree Synthesis: Creating a network of clock distribution paths to ensure uniform clock signal delivery across the chip, minimizing timing discrepancies.
  
- Routing: Determining optimal paths for interconnecting logical elements on the chip to establish functional connectivity while meeting timing and power constraints.

  

![Screenshot (26)](https://github.com/Bhanu-c3/vsdworkshop/assets/165283408/cf701fa5-9ec3-413e-a85f-e4c8575df708)

OpenLANE ASIC Flow:


![Screenshot (27)](https://github.com/Bhanu-c3/vsdworkshop/assets/165283408/3d2827f0-cf17-44ea-8b46-43acb4f61ec7)

#### LABS(Using Virtual Box)-

OpenLANE is an environment which integrates the open source tools for each stage in RTL2GDS flow.
We enter into the OpenLANE by using the command 'docker' and './flow.tcl -interactive'
we also use a command to prepare design that is 'prep -design picorv32a'. where PicoRV32A is a type of processor core based on the RISC-V architecture.

![Screenshot 2024-04-02 195226](https://github.com/Bhanu-c3/vsdworkshop/assets/165283408/d8aea15f-861f-4703-a3fe-4a60b5657bd0)


![Screenshot 2024-04-02 195524](https://github.com/Bhanu-c3/vsdworkshop/assets/165283408/39ef21f1-d892-42df-9951-f3459cd785cb)

Next, we run a synthesis command that is 'run_synthesis'
Synthesis is the process of translating a high-level hardware description language (HDL) design, such as Verilog or VHDL, into a gate-level netlist that represents the logic components (e.g., AND gates, flip-flops) and their interconnections.

![Screenshot 2024-04-09 205826](https://github.com/Bhanu-c3/vsdworkshop/assets/165283408/1a388c8f-1a0c-4d3a-9187-3644de24b32f)

Listing the files created after the synthesis in a particular directory.

![Screenshot 2024-04-09 210233](https://github.com/Bhanu-c3/vsdworkshop/assets/165283408/d38ec7ab-d3ba-4e3a-8424-c72adb43e147)

Categorize Synthesis results:
From the data of synthesis, total number of counter D_flip-flops is 1613. and the number of cells is 14876.

![Screenshot 2024-04-09 210949](https://github.com/Bhanu-c3/vsdworkshop/assets/165283408/abc2eedf-38fc-4703-a17a-2547a6171a91)


Flop ratio = (number of flip flops)/(number of total cell).

Flop ratio = 10.84%.







