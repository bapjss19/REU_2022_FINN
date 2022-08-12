# REU_2022_FINN
This is a repository to save the work Justin So and Emily Namm did during their time in Rice University's REU Program.

Justin and Emily's files are located in Atlas. There are two FINN frameworks running in Atlas. Thomas's FINN is in the rffi folder and Justin and Emily's FINN is in the Documents folder.

To access/run the files in Justin and Emily's FINN:
1. Go into Terminal
2. Type "cd Documents"
3. Type "cd finn"
4. Type "./run-docker.sh notebook"
5. Justin's XOR Network file is "XOR NETWORK.ipynb"
6. Emily's Quantized XOR Network is "Quant XOR NETWORK.ipynb"
7. The Quantized XOR Network can be found in end2end_example/cybersecurity

For Emily's Quant XOR Network:

1. Emily's model results in a loss stuck at 0.25 from the first 1000 epochs. This may be due to setting the weight_bit_width = 2, which is in lines 134-136 in "Quant XOR NETWORK.ipynb". 
2. I believe that you can find some of the pynq-board functions in "3-build-accelerator-with-finn.ipynb" found in end2end_example/cybersecurity, which also include some other useful files such as "1-train-mlp-with-brevitas.ipynb" and "2-import-into-finn-and-verify.ipynb".

For Justin's XOR Network:

There seems to be a few issues here:
1. The ONNX model reads the model input as a (0x2) input. Consequently, it produces a (0x1) output.
2. The Netron Model shows that the HLS Layer Conversion functions did not change the model.
3. This may explain why the StreamingDataflowPartition node is not created, which is needed for the Dataflow Partition step.
4. Since the Dataflow Partition step was skipped, the folding step (shown in the last cell in the XOR Network file) cannot be completed correctly.
