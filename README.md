# fpga-serial-mem-tester-2

FPGA Serial Mem Tester Version 2

Note that this project is deprecated. The most recent project, with wider
hardware support and occasional updates, is Version 3 and is located at:
[fpga-serial-mem-tester-3](https://github.com/timothystotts/fpga-serial-mem-tester-3)

## Description
A small AP SoC project of Zynq-7000 implementation for testing a N25Q Serial Flash.
The design targets the Digilent Inc. Zybo-Z7-20 FPGA development board containing a
Xilinx Zynq-7000 FPGA.
Two peripherals are used: Digilent Inc. Pmod SF3, Digilent Inc. Pmod CLS.

The folder SF-Tester-Design-Zynq contains a Xilinx Vivado IP Integrator plus
Xilinx Vitis design. The Zynq hard ARM CPU #0 is configured to talk with board
components,
a SPI Flash peripheral, and
a 16x2 character LCD peripheral.

Sources to be incorporated into a Xilinx Vitis project contain
a very small FreeRTOS program in C; drivers
for the peripherals, a real-time task to operate the flash chip,
two real-time tasks to display data, and a real-time task to color-mix RGB LEDs.

### Project information document:

./Serial Flash Sector Tester - Zynq.pdf

[Serial Flash Sector Tester for Zynq info](https://github.com/timothystotts/fpga-serial-mem-tester-2/blob/master/Serial%20Flash%20Sector%20Tester%20-%20Zynq.pdf)

#### Target device assembly: Zybo-Z7-20 with Pmod SF3, Pmod CLS on extension cable
![Target device assembly](https://github.com/timothystotts/fpga-serial-mem-tester-2/blob/master/img_serial-flash-tester-zynq-assembled-20200730.jpg)
