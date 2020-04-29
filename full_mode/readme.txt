##Full Mode aproach##
-Run full_mode_sim.py (top module)

Details:
- The simulation is done with a test bench that writes 8 bits values to 
transmit and their data types into the fifo with a 100 MHz writing clock (clk0).
- These signals values are connected to din a dtin pins of the daphne
platform. The link_ready and fifo write enable are also connected to other 
platform pins, just for simulation proposes.
- The GTP module contains the GTPQuadPLL and GTP class. The GTPQuadPLL class
contains the GTPE2_COMMON primitive module which uses a 300 MHz reference 
clock obtained from the top module. The GTP class contains the TX, fifo and 
GTPE2_CHANNEL modules. The TX module describes all the transmiting logic and 
the CRC encoding process. The fifo module is a asynchronous FIFO which reads 
values in the "tx" clock domain. In the GTPE2_COMMON module the TX buffer is
bypassed. 

