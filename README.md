# Icarus Verilog & GTKWave
This tutorial is intended for those taking CSC258 who want to compile and test Verilog code on their personal machines without having to use Quartus. The provided commands are intended for Linux and should serve only as reference material. 

### Instalation 
The two pieces of software we need are [Icarus Verilog](http://iverilog.icarus.com/) and [GTKwave](http://gtkwave.sourceforge.net/) both of which are open source and publy available. 
```bash
sudo apt-get install iverilog
sudo apt-get install gtkwave
```

### Compilation
```bash
iverilog -o simple.vvp simple.v simple_tb.v
```
In this specific example, we are testing a Verilog module called `simple.v`. The test cases are contained in the file `simpe_tb.v`, it can be named arbitrarily although it is called `moduldename_tb.v` by convention. We specify our output file to be named `simple.vvp`

### Running the Simulation
```bash
vvp simple.vvp
```
You should have something stdout in the form of 
```
VCD info: dumpfile simple.vcd opened for output.
A is 1010, B is 0011.
A is 1100, B is 0101.
```

### Viewing in Graph Form
```bash
gtkwave simple.vcd
```
___
> This is by no means a comprehensive guide, feel free to add/correct anything in this tutorial.
