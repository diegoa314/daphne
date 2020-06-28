To build the Vivado project and run simulation:
Run Xilinx/Vivado/2019.2/settings64.sh 
Run full_mode_sim.py 
The initialization of RX channel takes like 1.3 us in simulation time. 
Right after this initilization the transmision starts (see the testbench)

In full_mode_sim.py are defined the top module, the testbench and some functions 
to build the project and run simulation. In this top module are instantiated the 
submodules: QuadPLL (defined in gtp.py), which has the GTPE2_COMMON primitive module;
GTP (defined in gtp.py), which has GTPE2_CHANNEL primitive and a PLLE2_BASE primitive 
to provide clocks for the interfaces; TX (defined in tx.py), which contains all the 
logic and operations required for the protocol; a asynchronous FIFO; 
a memory where the data and data types are written.


