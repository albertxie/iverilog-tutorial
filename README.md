# Icarus Verilog & GTKWave

### Installation 
The two pieces of software we need are [Icarus Verilog](http://iverilog.icarus.com/) and [GTKwave](http://gtkwave.sourceforge.net/) both of which are open source and publicly available. 
```bash
sudo apt-get install iverilog
sudo apt-get install gtkwave
```

### Compilation
```bash
iverilog -o simple.vvp simple.v simple_tb.v
```
In this specific example, we are testing a Verilog module called `simple.v`. The test cases are contained in the file `simple_tb.v`, it can be named arbitrarily; although it is called `modulename_tb.v` by convention. We specify our output file to be `simple.vvp`

### Running the Simulation
```bash
vvp simple.vvp
```
You should have something output in the form of 
```
VCD info: dumpfile simple.vcd opened for output.
A is 1010, B is 0011.
A is 1100, B is 0101.
```

### Viewing in Graph Form
```bash
gtkwave simple.vcd
```
Once GTKWave has launched
  1. locate the `SST` tab top-left of the screen and expand all
  2. Locate the desired test case and click
  3. Bottom-left of the screen should display a chart with Type and Signal. Drag whichever one you'd like to analyse over to the Signals tab

![gtkwave annotated screenshot](gtkwave-annotated.png)

