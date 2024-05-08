
     
# DIGITAL VLSI SoC Design and planning

A Physical design project using opensource tools like Openlane/Sky130 PDK. 




## Contents

Day 1
-Inception of open-source EDA, OpenLANE and sky130 PDK

## Day 1
### Inception of open-source EDA, OpenLANE and sky130 PDK

   - How to talk to computers?
     - Introduction to QFN-48 Package, chip, pads, core, die and IPs

     The QFN48 package is a type of surface-mount integrated circuit package, which is commonly used for various electronic components such as microcontrollers, microprocessors, and other integrated circuits. 

     The "QFN" stands for Quad Flat No-leads, indicating that the package has a flat bottom with no leads protruding from the sides. The number "48" refers to the number of pins in the package.

     QFN packages offer several advantages, including small size, good thermal performance, and suitability for automated assembly processes such as pick-and-place machines. They are often used in applications where space is limited and heat dissipation is important, such as in mobile devices, automotive electronics, and consumer electronics.
     
     "Pads" in the context of an integrated circuit (IC) typically refer to the metalized areas on the IC where electrical connections are made. These pads serve as points for soldering or wire bonding to connect the IC to a printed circuit board (PCB) or another electronic component.

     The pads on an IC are usually made of metal (such as aluminum or copper) and are typically arranged around the periphery of the IC die. Each pad corresponds to a specific electrical signal or function of the IC.

     During the manufacturing process, the IC die is typically attached to a lead frame or substrate, and wires or bond pads are used to connect the internal circuitry of the IC to the external pads. These pads are then connected to the PCB or other components through soldering or bonding processes.

     The core of an integrated circuit typically refers to the central processing unit (CPU) or the main computational unit of the chip. It contains the primary logic, arithmetic, and control circuitry responsible for executing instructions and performing calculations. In more complex ICs, such as system-on-chip (SoC) designs, the core may include additional components like caches, memory controllers, and input/output interfaces. The core is often the most crucial part of the IC, determining its performance and functionality.

     The term "die" refers to the individual silicon wafer that contains the integrated circuitry. During the manufacturing process, multiple copies of the IC are fabricated on a single silicon wafer.

     Intellectual Property (IP) refers to pre-designed and pre-verified functional blocks or components that are licensed or purchased from third-party vendors. These IP blocks can include components such as CPU cores, memory controllers, interface controllers, digital signal processing (DSP) cores, and other specialized circuitry. 



     
![Screenshot 2024-04-26 22 56 04](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/cfa5f632-a02e-4740-b6a7-a1b420bd9c52)

     
![Screenshot 2024-04-26 22 58 28](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/eb37b401-5716-47e5-b286-a5ce2fafa477)

![Screenshot 2024-04-26 22 59 58](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/72ad3e25-1a4b-4824-9131-bc54da2d2e24)

- Introduction to RISCV
  
  RISC-V is an open-source instruction set architecture (ISA) based on the Reduced Instruction Set Computing (RISC) principles.RISC-V offers a flexible, open-source alternative to proprietary instruction set architectures, enabling innovation, collaboration, and customization in the design of hardware and software systems.

  A compiler is a software tool that translates high-level programming languages, such as C, C++, Java, or Python, into machine code or assembly language.Assembly language is a low-level programming language that closely resembles the binary machine code instructions of a particular computer architecture.Unlike compilers, which translate high-level source code into machine code, assemblers work directly with assembly language instructions and produce machine code that corresponds directly to those instructions.

  ![Screenshot 2024-04-27 13 09 51](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/693a4202-e495-4c8a-8280-3f0da372d7eb)

  - Soc design and OpenLANE
    - Introduction to all components of open-source digital asic design
   
      ![Screenshot 2024-04-27 13 49 11](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/7eb28597-31d4-4cab-8d50-ef66192d5e27)

      Opensource ASIC design includes EDA tools, PDK data and RTL designs.Electronic Design Automation (EDA) tools are software tools used by engineers and designers to design, analyze, and simulate electronic systems and integrated circuits (ICs). These tools facilitate the entire electronic design process, from concept and specification to implementation and verification. Various EDA tools are Qflow, OpenRoad, Openlane.

      A Process Design Kit (PDK) is a set of files, models, and documentation provided by semiconductor foundries to enable the design and simulation of integrated circuits (ICs) using their fabrication processes. These kits are essential for designers to create IC layouts, simulate circuit performance, and verify designs before manufacturing.

- Simplified RTL2GDS flow
  
  ![Screenshot 2024-04-27 14 16 07](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/d3622a2e-fe21-40f5-b6e2-b4e74dc7f974)

  **Synthesis** It is the process in this RTL is converted to a circuit out of components from the standard cell library(SCL).
  **Chip floor planning** Partition the chip die between different system building blocks and place the I/O pads.
                           Power planning is the construction of power network.
  **Placement** Place the cells on the floorplan rows,aligned with the sites.

  It is usually done in two steps
  1.Global
  2.Detailed

  **Clock Tree Synthesis** To deliver clock to all sequential elements.
  **Routing** Implement the interconnect using the available metal layers.
  **Sign off** Physical Verifications
                 - Design Rule Checking
                 - Layout vs Schematic
  
                 Timing Verification
                 - Static Timing Analysis

  **Get familiar to open-source EDA tools**

  - OpenLANE Directory structure in detail
 
    **Openlane**OpenLANE is an open-source software toolflow for automated RTL-to-GDSII (Register Transfer Level to Graphic Data System II) design and implementation of digital integrated circuits. Developed by Efabless Corporation in collaboration with Google and SkyWater Technology Foundry, OpenLANE aims to democratize access to ASIC (Application-Specific Integrated Circuit) design by providing a free and open-source toolflow that leverages open-source EDA tools and PDKs.

    ![Screenshot 2024-04-27 17 07 27](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/ce657753-7f7d-45ef-8338-e9739ae03005)

Inorder to open the Openlane, run the ubuntu os in the virtual machine.
![WhatsApp Image 2024-04-27 at 5 19 26 PM (1)](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/190fac3f-b0c8-4d40-a586-4f2bf3dc7b82)

`Desktop/work/tools/openlane_working_dir/openlane`

![WhatsApp Image 2024-04-27 at 5 19 26 PM (1)](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/ae3b1bda-fabb-40bb-9a77-92214fba2b46)

invoke the openlane using the command `docker ./flow.tcl -interactive`

![WhatsApp Image 2024-04-27 at 9 12 10 PM](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/93aebce3-07c9-4418-9543-255a88ae9fd3)

import all the pakages `package require openlane0.9`

Prepare design setup stage `prep -design picrv32a`
![WhatsApp Image 2024-04-27 at 9 12 10 PM (1)](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/0ca2eb79-e043-4e46-a646-e8d8eae6444f)

`run_synthesis`
![WhatsApp Image 2024-04-27 at 9 12 10 PM (2)](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/6e13a31e-0ccc-4e96-b163-55a3feb1a6a5)

Statistics after synthesis

![WhatsApp Image 2024-04-27 at 9 12 11 PM](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/c9ba42f4-85d6-4bb2-9d24-c96946ec1c84)

```
28. Printing statistics.

=== picorv32a ===

   Number of wires:              14596
   Number of wire bits:          14978
   Number of public wires:        1565
   Number of public wire bits:    1947
   Number of memories:               0
   Number of memory bits:            0
   Number of processes:              0
   Number of cells:              14876
     sky130_fd_sc_hd__a2111o_2       1
     sky130_fd_sc_hd__a211o_2       35
     sky130_fd_sc_hd__a211oi_2      60
     sky130_fd_sc_hd__a21bo_2      149
     sky130_fd_sc_hd__a21boi_2       8
     sky130_fd_sc_hd__a21o_2        57
     sky130_fd_sc_hd__a21oi_2      244
     sky130_fd_sc_hd__a221o_2       86
     sky130_fd_sc_hd__a22o_2      1013
     sky130_fd_sc_hd__a2bb2o_2    1748
     sky130_fd_sc_hd__a2bb2oi_2     81
     sky130_fd_sc_hd__a311o_2        2
     sky130_fd_sc_hd__a31o_2        49
     sky130_fd_sc_hd__a31oi_2        7
     sky130_fd_sc_hd__a32o_2        46
     sky130_fd_sc_hd__a41o_2         1
     sky130_fd_sc_hd__and2_2       157
     sky130_fd_sc_hd__and3_2        58
     sky130_fd_sc_hd__and4_2       345
     sky130_fd_sc_hd__and4b_2        1
     sky130_fd_sc_hd__buf_1       1656
     sky130_fd_sc_hd__buf_2          8
     sky130_fd_sc_hd__conb_1        42
     sky130_fd_sc_hd__dfxtp_2     1613
     sky130_fd_sc_hd__inv_2       1615
     sky130_fd_sc_hd__mux2_1      1224
     sky130_fd_sc_hd__mux2_2         2
     sky130_fd_sc_hd__mux4_1       221
     sky130_fd_sc_hd__nand2_2       78
     sky130_fd_sc_hd__nor2_2       524
     sky130_fd_sc_hd__nor2b_2        1
     sky130_fd_sc_hd__nor3_2        42
     sky130_fd_sc_hd__nor4_2         1
     sky130_fd_sc_hd__o2111a_2       2
     sky130_fd_sc_hd__o211a_2       69
     sky130_fd_sc_hd__o211ai_2       6
     sky130_fd_sc_hd__o21a_2        54
     sky130_fd_sc_hd__o21ai_2      141
     sky130_fd_sc_hd__o21ba_2      209
     sky130_fd_sc_hd__o21bai_2       1
     sky130_fd_sc_hd__o221a_2      204
     sky130_fd_sc_hd__o221ai_2       7
     sky130_fd_sc_hd__o22a_2      1312
     sky130_fd_sc_hd__o22ai_2       59
     sky130_fd_sc_hd__o2bb2a_2     119
     sky130_fd_sc_hd__o2bb2ai_2     92
     sky130_fd_sc_hd__o311a_2        8
     sky130_fd_sc_hd__o31a_2        19
     sky130_fd_sc_hd__o31ai_2        1
     sky130_fd_sc_hd__o32a_2       109
     sky130_fd_sc_hd__o41a_2         2
     sky130_fd_sc_hd__or2_2       1088
     sky130_fd_sc_hd__or2b_2        25
     sky130_fd_sc_hd__or3_2         68
     sky130_fd_sc_hd__or3b_2         5
     sky130_fd_sc_hd__or4_2         93
     sky130_fd_sc_hd__or4b_2         6
     sky130_fd_sc_hd__or4bb_2        2

   Chip area for module '\picorv32a': 147712.918400
```
 flipflop ratio = 1613/14876 = 0.108 = 10.8%.

 ## Day 2

 `run_floorplan`
 ![WhatsApp Image 2024-04-28 at 11 00 34 PM](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/df50a5ca-ac44-4063-892d-9cd06047f24b)

 invoke the magic tool

 ![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/e5406887-af90-4ad7-86d6-ae702f3ba79d)

 ![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/9f086f8b-81f5-406b-9c52-e2a8293befd0)

 `run_placement`
 ![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/313495ad-5429-42a2-9ce4-7f37e40056b6)

 ![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/7ea6d7b4-a96f-47d1-91dc-d38365eae724)


**Timing Characterization**
 ![Screenshot 2024-04-29 20 23 58](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/4480e78c-73b1-4f79-a4dc-dc1e695088dd)

 ## Day 3 Design library cell using Magic Layout and ngspice characterization
 
`set ::env(FP_IO_MODE) 2`
 ![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/9d979223-d9d3-46f0-8580-0242976ca9e9)

  `clone the vsdstandardcell` repository
 ![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/1502107a-764a-40b4-b263-1d9149fe42d6)
 
inverter characteristics using ngspice
 ![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/442b6dcc-553e-4bfa-b164-63568f948fc2)

transient analysis of inverter using ngspice
![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/f6ea6ce0-0858-4a4d-a57b-8f317d3fdd41)

## Day 4 Pre-layout timing analysis and importance of good clock tree

Next step is to extract the '.lef' file from the '.mag' file to place it into the picorv32a flow.
![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/f09a48e2-1248-4c46-815f-439f04ae944b)

![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/95b68d6d-bfa0-42ac-9c81-de5d076a7519)

edit the `config.tcl` file

![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/79441dd3-5450-4386-b34c-d046be98403a)

prepare the design again using the following commands
```
./flow.tcl -interactive
package require openlane 0.9
prep -design picorv32a
set lefs [glob $::env(DESIGN_DIR)/src/*.lef]      
add_lefs -src $lefs
run_synthesis
```

The results after synthesis is as shown below

![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/59f272e0-6c2d-47ae-9a8b-c5e228124861)
Thre are slack timings

wns(worst negative slack)= -24.89

tns(total negative slack)= -759.46

Steps to configure synthesis settings to fix slack and include vsdinv
```
prep -design picorv32a -tag 01-04_12-54 -overwrite

set lefs [glob $::env(DESIGN_DIR)/src/*.lef]

add_lefs -src $lefs

echo $::env(SYNTH_STRATEGY)

set ::env(SYNTH_STRATEGY) "DELAY 3"

echo $::env(SYNTH_BUFFERING)

echo $::env(SYNTH_SIZING)

set ::env(SYNTH_SIZING) 1

echo $::env(SYNTH_DRIVING_CELL)

run_synthesis
```
After the synthesis the chip area is increased and slack timings become 0
![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/1bc0916f-b977-4b54-a295-dd521464f290)

![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/11f83e5b-fbd1-4097-946c-42f67d5f97fe)

Run floor planning using the commands
```
init_floorplan

place_io

tap_decap_or
```
`run_placement`
![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/e1fa4335-bdec-417c-9089-f496d030b194)

invoke the magic to see the placement result

![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/e9ba185f-3918-44f0-8635-7a0fb3859f44)
![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/f8c045b8-5b1d-4406-8633-60a0b1f7cda1)

while extending the image we can see that sky130_vsdinv we have created is included in picorv32a
![image](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/1d3aa78f-01bb-4214-8115-2cafb354b824)

**Timing analysis with ideal clocks using openSTA**

![WhatsApp Image 2024-05-08 at 2 10 18 AM](https://github.com/ASIFMUHAMMED756/physical_design/assets/95519417/22c00d7a-74a6-42f7-998e-7514bb6da823)

## Day 5





























    




    


  

