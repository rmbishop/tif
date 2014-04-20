tif - a tiny FPGA board
=======================

This branch fixes issues with the default code that
prevented that code from working.

It has been tested with on Windows 7 64x with
python 2.7.6 (32 bit).

Examples.  Type the following in your cmd.exe shell:

1) python tiffind.py

2) python tifload.py ../firmware/4000/flashctl/syn/tif_flashctl.jed

Use tifweb.py once you load tif_flashctl.jed

3) python tifweb.py 



Default branch text:


This is the software for Bugblat's *tiny FPGA* board - the *tif* board.

What is a tif board?
--------------------

A tif board is a small USB dongle which carries a non-volatile Lattice Semiconductor MachXO2 FPGA.

To program the FPGA, you start by writing a firmware program, usually in VHDL or Verilog though there are other options. The firmware program can be  simulated and compiled to a JEDEC bitstream with Lattice's free
*[Diamond](http://www.latticesemi.com/en/Products/DesignSoftwareAndIP/FPGAandLDS/LatticeDiamond.aspx)*
software.

Then you have to inject the bitstream into the tif's FPGA, and that's the job of the software in this repo. Primarily in Python, there are programs to

- program the onboard FPGA with a compiled bitstream
- control the FPGA firmware from a PC

Example FPGA firmware programs are also included,
plus an example of controlling the FPGA from a web application.

More Information
----------------

The tif product pages, including links to the full documentation, are
[here](http://bugblat.com/products/tif).
