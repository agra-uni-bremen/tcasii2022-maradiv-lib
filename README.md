# tcasii2022-maradiv-lib

Artifacts of the paper: "MARADIV: Library of MAGIC based Approximate Restoring Array Divider Benchmark Circuits for In-Memory Computing Using Memristors"

## Folder Structure

This folder contains the Pareto-optimal designs of approximate restoring array dividers. For every combination of design and error metric the Pareto-optimal designs are present in each of the folders.

```
	|-> 2_aig: Contains the designs for the Type-II Approximation
	|-> 4_aig: Contains the designs for the Type-IV Approximation
	|-> 6_aig: Contains the designs for the Type-VI Approximation

```
### Sub Folder Structure

The design metrics used are Gate_Count and Total_Cycles.
The error metrics used are Mean Absolute Error (MAE), Mean Square Error (MSE), and Mean Square Log Error (MSLE). 
We have a folder for each of the design and error metric. 

#### File Information

All the Files are in AIGER (.aig) format.
The Port Mapping is as follows:
	
	INPUT:
	First 16 bits are the Dividend
 	Next 8 bits are the Divisor
	
	Output:
	Next 8 bits are the Quotient 
	Next 8 bits are the Remainder

Example :

	module top (a1,a2,......, a40)
	endmodule 

The ports need to be read as 
	
	Dividend = {a1,a2,...,a16}
	Divisor = {a17,a18,...,a24}
	Quotient = {a25,a26,...,a32}
	Remainder = {a33,a34,...,a40}
