# 4-Bit Ripple Carry Adder (Verilog)

A simple, functionally verified digital 4-bit adder built from four 1-bit full adders.

## Files
- `full_adder.v` — 1-bit full adder
- `four_bit_adder.v` — four stages connected as ripple carry
- `tb_four_bit_adder.v` — exhaustive testbench (512 combinations)

## Run (Windows PowerShell)
```powershell
iverilog -g2012 -o adder_sim full_adder.v four_bit_adder.v tb_four_bit_adder.v
vvp adder_sim
gtkwave four_bit_adder.vcd
```
Expected console message: `PASS: all 512 input combinations verified.`

**Scope:** This repository verifies the digital logic in Verilog. If your course requires transistor-level CMOS, you must additionally create Xschem schematics, Ngspice simulations, Magic layout, and Netgen LVS results. Verilog alone is not a transistor-level CMOS implementation.
