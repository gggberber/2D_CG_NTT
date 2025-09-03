
We provide two sets of experimental code, including one 16-bit and one 32-bit NTT implementation. Both utilize 2D CG architectures with a BFU array of size 8×2.

For example, “32bit_2DCG_8R2C_NTT” contains three folders: the Python-based NTT implementation “32bit_ntt_python”, the FPGA-based NTT simulation ‘32bit_ntt_FPGA_simulation’, and the FPGA-based implementation “32bit_ntt_FPGA_implementation”.

If readers wish to deploy 2DCG on an FPGA, please refer to “32bit_ntt_FPGA_implementation”, and please note the following points:
1. The FPGA platform is “Xilinx Zynq7035”;
2. The synthesis tool used is “Vivado 2021.1”;
3. Import the rotation factors into the ROM IP (the required .coe files are located in “32bit_ntt_FPGA_implementation->ROM”); 
4. Add clock signals, maximum frequency of 240 MHz. 
5. Add constraint files (constraint files located in “32bit_ntt_FPGA_implementation->Constraints”). 
For other FPGAs, users can debug independently by simply re-pinning.
