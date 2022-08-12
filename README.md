# REU_2022_FINN
This is a repository to save the work Justin So and Emily Namm did during their time in Rice University's REU Program.

Justin and Emily's files are located in Atlas. There are two FINN frameworks running in Atlas. Thomas's FINN is in the rffi folder and Emily and Justin's FINN is in the Documents folder.

To access/run the files in Justin and Emily's FINN:
1. Go into Terminal
2. Type "cd Documents"
3. Type "cd finn"
4. Type "./run-docker.sh notebook"
5. Justin's XOR Network file is "XOR NETWORK.ipynb"
6. Emily's Quantized XOR Network is "Quant XOR NETWORK.ipynb"
7. The Quantized XOR Network can be found in end2nd_example/cybersecurity

For Emily's Quant XOR Network:
Emily's model results in a loss stuck at 0.25 from the first 1000 epochs. This may be due to setting the weight_bit_width = 2, which is in line 134-136.
