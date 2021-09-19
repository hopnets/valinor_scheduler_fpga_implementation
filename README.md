# Valinor scheduler FPGA implementation

This repository provides the FPGA implementation of the scheduler that supports the functionalities that Valinor requires. Valinor's deflection process might require extracting a packet from the tail of the queue. Accordingly, we modified [PIEO's Code](https://github.com/vishal1303/PIEO-Scheduler) to support this without requiring more cycles than PIEO's supported functionalities. We installed [Quartus Prime 20.1 Lite and Modelsim softwares](https://fpgasoftware.intel.com/) on [Windows 10](https://www.microsoft.com/en-us/software-download/windows10) to compile, synthesize, and simulate our code. To use this code you should:
* Clone this repository
* Compile, Synthesize, and simulate the project

## Cloning the repository 

We assume that you have the software, i.e., [Git Bash](https://git-scm.com/downloads), required for running the command to clone the repository. If you don't, you can simply use Github's GUI to clone the repository. To clone this repository in a directory, run git bash and use the following command: `git clone https://github.com/hopnets/valinor_scheduler_fpga_implementation.git`.

## Creating the project and importing the Verilog files

The Intel community provides [a guide](https://www.intel.com/content/www/us/en/programmable/documentation/aym1499789502823.html) on how to include the Verilog files in a project and how to synthesize and simulate a project. You should set "valinor.sv" as Top-Level Entity while compiling the modules. To test the modules, you should create a testbench file to initialize and change the inputs of the scheduler over time. [This tutorial](https://verilogguide.readthedocs.io/en/latest/verilog/testbench.html) provides good introductions on how to create testbench files for a project.
