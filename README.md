This is an AXI testbench. It uses UVM so unfortunately iverilog isn't sufficient. (I hope this changes soon.)

 * Dual-top testbench
 * Slave responder, no BFM (currently)
 * Supports AXI3 and AXI4
 * Supports all AXI data widths (8,16,32,64,128,256,512 and 1024)
 * Supports 32-bit and 64-bit address widths
 * Supports full and partial transfers.
 * Supports aligned and unaligned transfers.
 * Testbench side is event driven.  No #'delays, no @clock, etc
 * Emulator friendly (TB side is event driven. no @clock)
 * Pipelined AXI driver
 * Polymorphic interface
 * params_pkg.sv contains all dut parameters
 * A master driver - acts as an AXI master
 * A slave driver  - acts as an AXI slave
 * Coverage collector
 * Scoreboard (counts address packets and response packets)
    
Good whitepaper on slave sequences: 
http://www.verilab.com/files/reactive_slaves_presentation.pdf
http://www.verilab.com/files/litterick_uvm_slaves2_paper.pdf

Parallel/pipelined driver:
https://www.quora.com/What-is-the-best-way-to-model-an-out-of-order-transaction-driver-in-UVM
               
Monitors
https://verificationacademy.com/verification-horizons/june-2013-volume-9-issue-2/Monitors-Monitors-Everywhere-Who-Is-Monitoring-the-Monitors


